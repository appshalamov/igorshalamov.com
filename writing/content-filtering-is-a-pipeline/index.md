---
title: "Content filtering is a pipeline, not a blocklist — Igor Shalamov"
url: https://igorshalamov.com/writing/content-filtering-is-a-pipeline/
language: en
author: Igor Shalamov
updated: 2026-11-21
---

# Content filtering is a pipeline, not a blocklist

[Igor Shalamov](https://igorshalamov.com/about/), an AI systems architect and founder of Shalamov.io. 21 November 2026, 1 min read.

Content filtering is part of my work at Appvillis UAB on the Nicegram messenger, and the main lesson is architectural.

A blocklist answers one question: does this text contain a forbidden word? A filtering pipeline answers several, in order:

1. language and format;
2. spam and automation signals;
3. classification of harmful categories;
4. context: who sent it, where, in reply to what;
5. a decision with a confidence score, and a path for appeals.

Each stage can be measured and improved on its own. That is what makes the system maintainable.

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

Canonical page: https://igorshalamov.com/writing/content-filtering-is-a-pipeline/. Author: Igor Shalamov, AI systems architect who designs AI growth systems. Site guide for AI assistants: https://igorshalamov.com/llms.txt
