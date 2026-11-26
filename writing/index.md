---
title: "Writing — Igor Shalamov, AI Systems Architect"
url: https://igorshalamov.com/writing/
language: en
author: Igor Shalamov
updated: 2026-11-21
---

# Writing

Notes by Igor Shalamov, an AI systems architect and founder of Shalamov.io, on the architecture of AI growth systems: referral and recommendation systems, AI-driven communication automation, semantic search and classification.

[Two Tower Model Explained: Recommendation Retrieval at Scale](https://igorshalamov.com/writing/two-tower-model-explained/)

29 November 2026. Why a recommender cannot rank its whole catalogue, and how the two tower model solves candidate retrieval: separate user and item towers, a shared vector space, training on clicks with in-batch negati

[How to Build a Referral Program That Brings Users Who Stay](https://igorshalamov.com/writing/how-to-build-a-referral-program/)

28 November 2026. How to build a referral program as a system: attribution of every invitation, reward rules tied to retention, fraud checks before payout, targeting the right users at the right moment, and measuring K

[How to Evaluate Recommendation Systems: Precision@K, nDCG and A/B Tests](https://igorshalamov.com/writing/how-to-evaluate-recommendation-systems/)

26 November 2026. How to measure a personalized feed: a metric for each layer, Precision@K with a worked example, beyond-accuracy metrics, why offline gains disappear online, and how an A/B test with guardrails makes t

[Semantic Search vs Keyword Search: How Embeddings Find Meaning](https://igorshalamov.com/writing/semantic-search-vs-keyword-search/)

25 November 2026. Semantic search compares meaning instead of words: how embeddings, nearest-neighbour indexes, hybrid retrieval with BM25 and cross-encoder re-ranking work together, and how to evaluate them.

[How to Build a Referral System That Works Like a Recommender](https://igorshalamov.com/writing/how-to-build-a-referral-system/)

25 November 2026. How to design a referral system as a learned recommender: who should invite whom, how candidates are retrieved and ranked, and how to measure the result.

[Uplift modeling explained: pay the referral bonus only where it changes behaviour](https://igorshalamov.com/writing/uplift-modeling-explained/)

30 November 2026. A response model pays users who would invite anyway. Uplift modeling ranks users by how much the bonus changes their behaviour, and the uplift curve checks it.

[News personalization with BERT and LSTM: one model for the article, one for the reader](https://igorshalamov.com/writing/news-personalization-bert-lstm/)

24 November 2026. BERT encodes the article, an LSTM reads the user history in order, a ranking layer picks the top five. Precision@5 0.78, CTR 6.3% on MIND.

[One pipeline for intent, sentiment and toxicity](https://igorshalamov.com/writing/one-pipeline-intent-sentiment-toxicity/)

21 November 2026. One shared text encoder, three small heads: one pass, consistent labels, cheap to extend; separate thresholds, because mistakes cost differently.

[Telegram Mini Apps as a recommendation surface](https://igorshalamov.com/writing/telegram-mini-apps-recommendation-surface/)

21 November 2026. The entry link is a feature, the first screen must be personal, the invitation flow is one tap away.

[How to measure personalization](https://igorshalamov.com/writing/how-to-measure-personalization/)

21 November 2026. Precision@5, CTR, coverage, freshness. Optimise CTR alone and you get clickbait; precision alone and you get repetition.

[Two-tower models for candidate retrieval](https://igorshalamov.com/writing/two-tower-models-candidate-retrieval/)

21 November 2026. One tower for the user, one for the item, the same vector space. Retrieval becomes nearest-neighbour search; a heavier ranker sees only the top candidates.

[Content filtering is a pipeline, not a blocklist](https://igorshalamov.com/writing/content-filtering-is-a-pipeline/)

21 November 2026. A blocklist checks words. A filtering pipeline checks language, spam, harmful categories and context, then decides with a confidence score.

[Real-time news classification: speed against accuracy](https://igorshalamov.com/writing/real-time-news-classification-speed-vs-accuracy/)

21 November 2026. A larger model classifies better but answers later. A fast first pass, a heavier model for uncertain cases, thresholds that decide.

[How a feedback system in a messenger works](https://igorshalamov.com/writing/feedback-system-in-a-messenger/)

21 November 2026. Intake, understanding, routing, generated reply, learning from every edit: the fifth step makes it a growth system.

[Semantic news search: from keywords to embeddings](https://igorshalamov.com/writing/semantic-news-search-keywords-to-embeddings/)

20 November 2026. Keyword search matches words, semantic search matches meaning. For news, the freshness of the index becomes the hard part.

[A referral system is a recommender system](https://igorshalamov.com/writing/referral-system-is-a-recommender-system/)

20 November 2026. Who invites, whom, and with which message: three ranking problems instead of an “invite a friend” button.

[What is an AI growth system](https://igorshalamov.com/writing/what-is-an-ai-growth-system/)

20 November 2026. The class of systems that help a product grow by learning from its users, and the three layers every such system has.

Subscribe: [RSS feed](https://igorshalamov.com/writing/feed.xml). Research articles behind these notes: [Research](https://igorshalamov.com/research/).

---

Canonical page: https://igorshalamov.com/writing/. Author: Igor Shalamov, AI systems architect who designs AI growth systems. Site guide for AI assistants: https://igorshalamov.com/llms.txt
