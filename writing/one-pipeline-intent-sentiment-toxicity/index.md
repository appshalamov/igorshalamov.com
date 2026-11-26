---
title: "One pipeline for intent, sentiment and toxicity — Igor Shalamov"
url: https://igorshalamov.com/writing/one-pipeline-intent-sentiment-toxicity/
language: en
author: Igor Shalamov
updated: 2026-11-21
---

# One pipeline for intent, sentiment and toxicity

[Igor Shalamov](https://igorshalamov.com/about/), an AI systems architect and founder of Shalamov.io. 21 November 2026, 1 min read.

A pattern from AI communication automation: do not build three separate classifiers when one shared encoder will do.

Intent, sentiment and toxicity all read the same message. A shared text encoder with three small heads:

- runs one forward pass instead of three;
- keeps the three labels consistent with each other;
- lets new heads (language, urgency) be added cheaply.

The heads still get separate thresholds and separate evaluation, because the cost of a mistake differs: a missed toxic message is not the same as a misread intent.

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

Canonical page: https://igorshalamov.com/writing/one-pipeline-intent-sentiment-toxicity/. Author: Igor Shalamov, AI systems architect who designs AI growth systems. Site guide for AI assistants: https://igorshalamov.com/llms.txt
