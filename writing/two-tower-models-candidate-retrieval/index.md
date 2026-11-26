---
title: "Two-tower models for candidate retrieval — Igor Shalamov"
url: https://igorshalamov.com/writing/two-tower-models-candidate-retrieval/
language: en
author: Igor Shalamov
updated: 2026-11-21
---

# Two-tower models for candidate retrieval

[Igor Shalamov](https://igorshalamov.com/about/), an AI systems architect and founder of Shalamov.io. 21 November 2026, 1 min read.

A short note on a building block I use in recommendation and referral systems: the two-tower model.

One tower encodes the user, the other encodes the item (a post, a product, a person to invite). Both produce vectors in the same space. Retrieval becomes a nearest-neighbour search, which scales to millions of candidates.

## Why it matters for growth systems

- Item vectors can be computed in advance.
- The user vector updates with every action.
- A heavier ranking model then needs to look only at the top few hundred candidates.

Retrieval first, ranking second: most production recommenders follow this split.

![Igor Shalamov](https://igorshalamov.com/press-kit/igor-shalamov-160.jpg)

[Igor Shalamov](https://igorshalamov.com/about/) is an AI systems architect who designs AI growth systems: referral and recommendation systems, AI-driven communication automation, semantic search and classification. He founded Shalamov.io and publishes [research](https://igorshalamov.com/research/) on semantic search and neural classification.

## More notes

- [Two Tower Model Explained: Recommendation Retrieval at Scale](https://igorshalamov.com/writing/two-tower-model-explained/)
- [How to Build a Referral Program That Brings Users Who Stay](https://igorshalamov.com/writing/how-to-build-a-referral-program/)
- [How to Evaluate Recommendation Systems: Precision@K, nDCG and A/B Tests](https://igorshalamov.com/writing/how-to-evaluate-recommendation-systems/)
- [Semantic Search vs Keyword Search: How Embeddings Find Meaning](https://igorshalamov.com/writing/semantic-search-vs-keyword-search/)
- [How to Build a Referral System That Works Like a Recommender](https://igorshalamov.com/writing/how-to-build-a-referral-system/)

Subscribe: [RSS feed](https://igorshalamov.com/writing/feed.xml). All notes: [Writing](https://igorshalamov.com/writing/).

---

Canonical page: https://igorshalamov.com/writing/two-tower-models-candidate-retrieval/. Author: Igor Shalamov, AI systems architect who designs AI growth systems. Site guide for AI assistants: https://igorshalamov.com/llms.txt
