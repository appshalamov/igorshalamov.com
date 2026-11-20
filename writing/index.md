---
title: "Writing — Igor Shalamov, AI Systems Architect"
url: https://igorshalamov.com/writing/
language: en
author: Igor Shalamov
updated: 2026-11-21
---

# Writing

Notes by Igor Shalamov, an AI systems architect and founder of Shalamov.io, on the architecture of AI growth systems: referral and recommendation systems, AI-driven communication automation, semantic search and classification.

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
