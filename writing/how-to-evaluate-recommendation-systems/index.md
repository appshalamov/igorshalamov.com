---
title: "How to Evaluate Recommendation Systems: Precision@K, nDCG and A/B Tests — Igor Shalamov"
url: https://igorshalamov.com/writing/how-to-evaluate-recommendation-systems/
language: en
author: Igor Shalamov
updated: 2026-11-21
---

# How to Evaluate Recommendation Systems: Precision@K, nDCG and A/B Tests

[Igor Shalamov](https://igorshalamov.com/about/), an AI systems architect and founder of Shalamov.io. 26 November 2026, 2 min read.

A new ranking model wins every offline metric. It goes into an A/B test, and nothing changes. This happens more often than teams expect.

## Where metrics apply

A personalized feed is built in layers, and each layer needs its own metric. Candidate generation narrows millions of items to a few hundred. We measure its recall. A ranking model orders them. We measure ranking quality. A re-ranking step adds diversity, freshness and business rules. Only then does the user see the feed, and there we measure outcomes. A good number for one layer says little about the next one.

## Precision@K

Offline, we replay historical data. Precision@K is the share of relevant items among the top K recommendations. Take K = 5. In a made-up example, one reader later opened three stories we could have shown. A popularity baseline gets one of them into its top five: 0.2. The old model gets two: 0.4. The new model gets all three: 0.6. Always split by time: train on the past, test on the future, or every number is inflated.

## Beyond accuracy

Accuracy is not the whole picture. Precision and recall at K count relevant items in the top K. Coverage shows how much of the catalogue is ever recommended. nDCG also rewards placing relevant items higher, because people rarely scroll far. Diversity measures how different the items in one feed are. But none of the accuracy metrics tells you that a feed has become boring. Novelty and calibration check that the feed goes beyond the obvious and matches the reader's real mix of interests.

## The offline-online gap

So why do offline gains disappear? First, position bias: people click what is shown on top, so the logs favour the old ranking. Second, a feedback loop: the training data was produced by the previous model. Third, there is no data on items that were never shown. Inverse propensity scoring helps, but it does not remove the bias. Finally, a click is only a proxy for satisfaction. The feedback loop is the one most teams underestimate.

## Online test

Offline evaluation is a filter. The A/B test makes the decision. Split real traffic between the old model and the new one. Then measure what matters: click-through rate, dwell time, and above all, whether readers come back. These numbers are illustrative. The difference in return rate is the result that counts.

## Recap

To recap: measure each layer with its own metric, and look beyond accuracy. Split offline data by time, and treat offline results as a filter. Then let a well-guarded A/B test make the final call.

## Related research

The research behind this topic is my paper [Personalization of news content using AI: architecture and efficiency of neural network systems](https://igorshalamov.com/research/news-personalization-ai/) (2025).

## Video

Watch the episode: [How to Evaluate Recommendation Systems: Precision@K, nDCG and A/B Tests](https://youtu.be/eW9FAuHuYTI)

![Igor Shalamov](https://igorshalamov.com/press-kit/igor-shalamov-160.jpg)

[Igor Shalamov](https://igorshalamov.com/about/) is an AI systems architect who designs AI growth systems: referral and recommendation systems, AI-driven communication automation, semantic search and classification. He founded Shalamov.io and publishes [research](https://igorshalamov.com/research/) on semantic search and neural classification.

## More notes

- [Two Tower Model Explained: Recommendation Retrieval at Scale](https://igorshalamov.com/writing/two-tower-model-explained/)
- [How to Build a Referral Program That Brings Users Who Stay](https://igorshalamov.com/writing/how-to-build-a-referral-program/)
- [Semantic Search vs Keyword Search: How Embeddings Find Meaning](https://igorshalamov.com/writing/semantic-search-vs-keyword-search/)
- [How to Build a Referral System That Works Like a Recommender](https://igorshalamov.com/writing/how-to-build-a-referral-system/)
- [Uplift modeling explained: pay the referral bonus only where it changes behaviour](https://igorshalamov.com/writing/uplift-modeling-explained/)

Subscribe: [RSS feed](https://igorshalamov.com/writing/feed.xml). All notes: [Writing](https://igorshalamov.com/writing/).

---

Canonical page: https://igorshalamov.com/writing/how-to-evaluate-recommendation-systems/. Author: Igor Shalamov, AI systems architect who designs AI growth systems. Site guide for AI assistants: https://igorshalamov.com/llms.txt
