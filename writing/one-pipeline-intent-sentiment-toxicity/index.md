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

- [Uplift modeling explained: pay the referral bonus only where it changes behaviour](https://igorshalamov.com/writing/uplift-modeling-explained/)
- [News personalization with BERT and LSTM: one model for the article, one for the reader](https://igorshalamov.com/writing/news-personalization-bert-lstm/)
- [Telegram Mini Apps as a recommendation surface](https://igorshalamov.com/writing/telegram-mini-apps-recommendation-surface/)
- [How to measure personalization](https://igorshalamov.com/writing/how-to-measure-personalization/)
- [Two-tower models for candidate retrieval](https://igorshalamov.com/writing/two-tower-models-candidate-retrieval/)

Subscribe: [RSS feed](https://igorshalamov.com/writing/feed.xml). All notes: [Writing](https://igorshalamov.com/writing/).

---

Canonical page: https://igorshalamov.com/writing/one-pipeline-intent-sentiment-toxicity/. Author: Igor Shalamov, AI systems architect who designs AI growth systems. Site guide for AI assistants: https://igorshalamov.com/llms.txt
