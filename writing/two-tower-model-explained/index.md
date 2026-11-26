---
title: "Two Tower Model Explained: Recommendation Retrieval at Scale — Igor Shalamov"
url: https://igorshalamov.com/writing/two-tower-model-explained/
language: en
author: Igor Shalamov
updated: 2026-11-21
---

# Two Tower Model Explained: Recommendation Retrieval at Scale

[Igor Shalamov](https://igorshalamov.com/about/), an AI systems architect and founder of Shalamov.io. 29 November 2026, 3 min read.

You have 10 million items, and 50 milliseconds to choose what one user sees. Your best ranking model cannot score them all in time. Every large recommender hits this wall, and most solve it the same way. With a two tower model.

## Two stages

Example numbers: a good ranking model needs about 10 microseconds per item. 10 million items times 10 microseconds is 100 seconds. The budget is 50 milliseconds, so we are 2,000 times too slow. So the work is split into two stages. Retrieval cheaply narrows 10 million items to about 1,000 candidates. Ranking scores those 1,000 with the heavy model, in 10 milliseconds. Only the top 20 reach the feed. Two towers are the standard design for retrieval.

## Two towers

The model has two separate neural networks, called towers. The user tower starts from a learned embedding of the user ID. The item tower does the same for the item. The user side adds history: recent clicks, watches and purchases. The item side adds content: text, category and creator. Both sides add more: context for the user, age and popularity for the item. Each tower outputs a vector of the same size, say 64 numbers.

## Scoring

Both towers write into one shared space. This is a two-dimensional sketch of it. The user vector lands somewhere in that space. The score of a user and an item is the dot product of their two vectors. Normalise both vectors, and the dot product becomes cosine similarity. Retrieval is then a nearest neighbour search around the user. The key constraint: the towers never see each other's inputs. That is why item vectors can be precomputed.

## Training

Training data: pairs of a user and an item they clicked. For each user in a batch, the other users' clicks serve as negatives. These are in-batch negatives: no extra sampling needed. The loss pushes the clicked item up and the others down. One catch: popular items appear in many batches, so they are punished as negatives too often. The fix, sampling bias correction: subtract the log of each item's sampling probability.

## Serving

The two towers run at different times. The item tower runs offline, in batch, over the whole catalogue. It produces one vector per item. Those vectors go into an approximate nearest neighbour index, for example HNSW. At request time, only the user tower runs: one forward pass, one vector. The index returns the top 1,000 items in a few milliseconds. Whenever the item tower changes, the index is rebuilt.

## Recall@K

Retrieval has one job: do not lose the good items. The ranker never sees what retrieval dropped. So we measure Recall@K: the share of all relevant items that reach the top K. Here K = 1,000, the candidate list size. In a made-up example, one user clicks 20 items in the test week. A popularity baseline retrieves six of them: 0.3. Two towers with ID features only find eleven: 0.55. Add content features, and they find fifteen: 0.75. Always split by time: train on the past, test on the next week.

## Pitfalls

First, cold start: a new item has no clicks, so its ID embedding is noise. Content features in the item tower give it a sensible vector from day one. Second, leakage: a feature computed after the click, like a total view count. Offline metrics look great, and production does not. Use point-in-time features. Third, version skew: the user tower is updated, but the index still holds old item vectors. The vectors stop sharing a space. Version both towers and the index together.

## Uses and recap

The pattern appears wherever a catalogue is too large to rank. Video, music and news feeds. Products for a shopper. Documents for a search query. And referral systems: who should a user invite? There, the inviter is the query, and possible invitees are the items. That is the retrieval step of the referral system from our first video. To recap: two towers, one space, items indexed offline, users encoded online, checked with Recall@K.

It covers neural network architectures for referral funnels.

## Video

Watch the episode: [Two Tower Model Explained: Recommendation Retrieval at Scale](https://youtu.be/ZJXA4Q7RtdQ)

![Igor Shalamov](https://igorshalamov.com/press-kit/igor-shalamov-160.jpg)

[Igor Shalamov](https://igorshalamov.com/about/) is an AI systems architect who designs AI growth systems: referral and recommendation systems, AI-driven communication automation, semantic search and classification. He founded Shalamov.io and publishes [research](https://igorshalamov.com/research/) on semantic search and neural classification.

## More notes

- [How to Build a Referral Program That Brings Users Who Stay](https://igorshalamov.com/writing/how-to-build-a-referral-program/)
- [How to Evaluate Recommendation Systems: Precision@K, nDCG and A/B Tests](https://igorshalamov.com/writing/how-to-evaluate-recommendation-systems/)
- [Semantic Search vs Keyword Search: How Embeddings Find Meaning](https://igorshalamov.com/writing/semantic-search-vs-keyword-search/)
- [How to Build a Referral System That Works Like a Recommender](https://igorshalamov.com/writing/how-to-build-a-referral-system/)
- [Uplift modeling explained: pay the referral bonus only where it changes behaviour](https://igorshalamov.com/writing/uplift-modeling-explained/)

Subscribe: [RSS feed](https://igorshalamov.com/writing/feed.xml). All notes: [Writing](https://igorshalamov.com/writing/).

---

Canonical page: https://igorshalamov.com/writing/two-tower-model-explained/. Author: Igor Shalamov, AI systems architect who designs AI growth systems. Site guide for AI assistants: https://igorshalamov.com/llms.txt
