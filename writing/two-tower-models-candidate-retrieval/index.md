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

- [One pipeline for intent, sentiment and toxicity](https://igorshalamov.com/writing/one-pipeline-intent-sentiment-toxicity/)
- [Telegram Mini Apps as a recommendation surface](https://igorshalamov.com/writing/telegram-mini-apps-recommendation-surface/)
- [How to measure personalization](https://igorshalamov.com/writing/how-to-measure-personalization/)
- [Content filtering is a pipeline, not a blocklist](https://igorshalamov.com/writing/content-filtering-is-a-pipeline/)
- [Real-time news classification: speed against accuracy](https://igorshalamov.com/writing/real-time-news-classification-speed-vs-accuracy/)

Subscribe: [RSS feed](https://igorshalamov.com/writing/feed.xml). All notes: [Writing](https://igorshalamov.com/writing/).

---

Canonical page: https://igorshalamov.com/writing/two-tower-models-candidate-retrieval/. Author: Igor Shalamov, AI systems architect who designs AI growth systems. Site guide for AI assistants: https://igorshalamov.com/llms.txt
