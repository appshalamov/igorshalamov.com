---
title: "Real-time news classification: speed against accuracy — Igor Shalamov"
url: https://igorshalamov.com/writing/real-time-news-classification-speed-vs-accuracy/
language: en
author: Igor Shalamov
updated: 2026-11-21
---

# Real-time news classification: speed against accuracy

[Igor Shalamov](https://igorshalamov.com/about/), an AI systems architect and founder of Shalamov.io. 21 November 2026, 1 min read.

My 2025 paper looks at [neural networks for real-time news classification](https://igorshalamov.com/research/neural-news-classification-real-time/). The central trade-off is easy to state and hard to tune.

A larger model classifies better but answers later. A news stream punishes lateness: a perfectly labelled story that arrives ten minutes late is worth less than a good label now.

## Common answers

- A fast first-pass classifier, with a heavier model for uncertain cases only.
- Distilled models that keep most of the accuracy at a fraction of the cost.
- Confidence thresholds that decide when to wait for the second opinion.

![Igor Shalamov](https://igorshalamov.com/press-kit/igor-shalamov-160.jpg)

[Igor Shalamov](https://igorshalamov.com/about/) is an AI systems architect who designs AI growth systems: referral and recommendation systems, AI-driven communication automation, semantic search and classification. He founded Shalamov.io and publishes [research](https://igorshalamov.com/research/) on semantic search and neural classification.

## More notes

- [News personalization with BERT and LSTM: one model for the article, one for the reader](https://igorshalamov.com/writing/news-personalization-bert-lstm/)
- [One pipeline for intent, sentiment and toxicity](https://igorshalamov.com/writing/one-pipeline-intent-sentiment-toxicity/)
- [Telegram Mini Apps as a recommendation surface](https://igorshalamov.com/writing/telegram-mini-apps-recommendation-surface/)
- [How to measure personalization](https://igorshalamov.com/writing/how-to-measure-personalization/)
- [Two-tower models for candidate retrieval](https://igorshalamov.com/writing/two-tower-models-candidate-retrieval/)

Subscribe: [RSS feed](https://igorshalamov.com/writing/feed.xml). All notes: [Writing](https://igorshalamov.com/writing/).

---

Canonical page: https://igorshalamov.com/writing/real-time-news-classification-speed-vs-accuracy/. Author: Igor Shalamov, AI systems architect who designs AI growth systems. Site guide for AI assistants: https://igorshalamov.com/llms.txt
