---
title: "Semantic Search vs Keyword Search: How Embeddings Find Meaning — Igor Shalamov"
url: https://igorshalamov.com/writing/semantic-search-vs-keyword-search/
language: en
author: Igor Shalamov
updated: 2026-11-21
---

# Semantic Search vs Keyword Search: How Embeddings Find Meaning

[Igor Shalamov](https://igorshalamov.com/about/), an AI systems architect and founder of Shalamov.io. 25 November 2026, 2 min read.

A user types a question, and the best answer does not share a single word with it. Keyword search misses it. Semantic search finds it, because it compares meaning, not words.

## Vocabulary mismatch

A reader searches for: central bank raises the cost of borrowing. The story that answers it says: interest rates go up by a quarter point. The two texts share almost no words. Keyword scoring counts overlapping terms, so this story ranks low. We need to compare meaning instead.

## Architecture

Every document is encoded offline into a vector, called an embedding. At query time, the same encoder turns the question into a vector. An approximate nearest neighbour index, for example HNSW, returns the closest documents in milliseconds. Then a re-ranker reads the top candidates more carefully. And it produces the final order. Follow one query through the system. The index is fast but approximate. The re-ranker is slow but precise.

## Nearest neighbours

Picture the embedding space as a map, where stories with similar meaning sit close together. This is a two-dimensional sketch. Real embeddings have hundreds of dimensions. The query lands on the same map. Search becomes a nearest neighbour lookup around it. We keep the five nearest stories, and none of them has to share a word with the query.

## Sparse vs dense

Keyword search is not obsolete. It simply fails in different places. Sparse retrieval, such as BM25, is precise on exact terms: names, numbers, product codes. Dense retrieval captures meaning and paraphrases. Sparse needs no training. Dense needs a trained encoder. Sparse misses paraphrases, while dense can miss rare names and codes. Because their errors differ, the strongest systems combine both.

## Hybrid and re-ranking

BM25 alone puts the story with the most matching words on top. Add dense retrieval and merge both lists, for example with reciprocal rank fusion. Then a cross-encoder reads the query and each story together, and scores them again. The rate hike story, which shared no words with the query, is now first. A cross-encoder is accurate but slow, so it only runs on the short list.

## Evaluation

Evaluate each stage on its own. For retrieval, use Recall@K: the share of all relevant documents that reach the top K. Here K = 100, the size of the short list. In a made-up example, the query has ten relevant stories. Sparse retrieval alone finds six of them: 0.6. Dense retrieval alone finds seven: 0.7. The hybrid finds nine: 0.9. For the final order, add nDCG@10, and track latency at the 95th percentile.

## News search

News adds four requirements. Freshness: relevance is blended with a time decay. Deduplication: many outlets publish near-identical stories, so results are clustered. Streaming: a new story must be searchable within seconds. And entities: names and places must stay exact, one more reason to keep sparse retrieval in the mix.

## Recap

To recap: encode documents and queries into one vector space. Retrieve with a hybrid of sparse and dense search, then re-rank the short list. Measure recall for retrieval, nDCG for the final order, and latency for the user.

## Related research

The research behind this topic is my paper [Semantic news search using artificial intelligence: technologies, problems and prospects](https://igorshalamov.com/research/semantic-news-search-ai/) (2024).

## Video

Watch the episode: [Semantic Search vs Keyword Search: How Embeddings Find Meaning](https://youtu.be/x8RKXt7atjw)

![Igor Shalamov](https://igorshalamov.com/press-kit/igor-shalamov-160.jpg)

[Igor Shalamov](https://igorshalamov.com/about/) is an AI systems architect who designs AI growth systems: referral and recommendation systems, AI-driven communication automation, semantic search and classification. He founded Shalamov.io and publishes [research](https://igorshalamov.com/research/) on semantic search and neural classification.

## More notes

- [Two Tower Model Explained: Recommendation Retrieval at Scale](https://igorshalamov.com/writing/two-tower-model-explained/)
- [How to Build a Referral Program That Brings Users Who Stay](https://igorshalamov.com/writing/how-to-build-a-referral-program/)
- [How to Evaluate Recommendation Systems: Precision@K, nDCG and A/B Tests](https://igorshalamov.com/writing/how-to-evaluate-recommendation-systems/)
- [How to Build a Referral System That Works Like a Recommender](https://igorshalamov.com/writing/how-to-build-a-referral-system/)
- [Uplift modeling explained: pay the referral bonus only where it changes behaviour](https://igorshalamov.com/writing/uplift-modeling-explained/)

Subscribe: [RSS feed](https://igorshalamov.com/writing/feed.xml). All notes: [Writing](https://igorshalamov.com/writing/).

---

Canonical page: https://igorshalamov.com/writing/semantic-search-vs-keyword-search/. Author: Igor Shalamov, AI systems architect who designs AI growth systems. Site guide for AI assistants: https://igorshalamov.com/llms.txt
