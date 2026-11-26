---
title: "News personalization with BERT and LSTM: one model for the article, one for the reader — Igor Shalamov"
url: https://igorshalamov.com/writing/news-personalization-bert-lstm/
language: en
author: Igor Shalamov
updated: 2026-11-21
---

# News personalization with BERT and LSTM: one model for the article, one for the reader

[Igor Shalamov](https://igorshalamov.com/about/), an AI systems architect and founder of Shalamov.io. 24 November 2026, 1 min read.

A news recommender has to read two things at once: the article and the reader's recent history. In my 2025 paper on [personalization of news content with AI](https://igorshalamov.com/research/news-personalization-ai/) I gave each of them its own model.

## The setup

1. **BERT** encodes the text of each article, so two stories about the same event end up close to each other even when they share few words.
2. **An LSTM** reads the articles a user opened, in order. A reader who moved from sport to markets last week gets a different state from one who did it a year ago.
3. **A ranking layer** scores candidate articles against that reader state and returns the top five.

## Results

The experiments used MIND, Microsoft's public news-recommendation dataset (Wu et al., ACL 2020). The hybrid reached Precision@5 of 0.78, Recall@5 of 0.75, F1 of 0.76 and a CTR of 6.3%. Against the TextCNN, LSTM, BERT-base and matrix-factorization baselines that is up to 43% higher F1 and 66% higher CTR. It also did better in cold-start cases, which fits the design: a new article can be ranked from its text before anyone has clicked it.

## The cost

Running BERT on every new article is heavy for a live feed, and MIND is English-only, so multilingual news stays an open problem. The next step the paper names is a lighter model that keeps most of the gain. How to read these metrics together is covered in [How to measure personalization](https://igorshalamov.com/writing/how-to-measure-personalization/).

## Video

Watch the episode: [Hybrid Recommendation System: BERT + LSTM News Recommender Explained](https://youtu.be/EkyC-8WAZ6g)

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

Canonical page: https://igorshalamov.com/writing/news-personalization-bert-lstm/. Author: Igor Shalamov, AI systems architect who designs AI growth systems. Site guide for AI assistants: https://igorshalamov.com/llms.txt
