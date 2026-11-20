---
title: "AI Growth Systems — Architecture and Research, Igor Shalamov"
url: https://igorshalamov.com/ai-growth-systems/
language: en
author: Igor Shalamov
updated: 2026-11-20
---

# AI growth systems

AI growth systems are software systems in which machine-learning models decide how a digital product attracts, engages and keeps its users. Igor Shalamov, an AI systems architect and founder of Shalamov.io, designs systems of this class and publishes research on them.

## What belongs to this class

### Referral systems

A referral system turns existing users into a channel for new ones: invitations, partner links, attribution of each new user to the person who invited them, and rewards. Neural networks take over the parts that used to be manual: generating messages, analysing the audience, adapting each user's path through the funnel and optimising campaigns. Research: [Neural network architectures for automating user funnels in referral marketing](https://igorshalamov.com/research/neural-architectures-referral-funnels/); [AI-driven marketing: the evolution of sales funnels in digital ecosystems](https://igorshalamov.com/research/ai-driven-sales-funnels/).

### Recommendation systems

A recommendation system ranks content or offers for each user from the text of the items and the history of the user's actions. In [his article on news personalization](https://igorshalamov.com/research/news-personalization-ai/), Igor Shalamov proposes a hybrid model that combines BERT for the meaning of the text with LSTM for the order of user interactions; on the MIND dataset it is compared with TextCNN, LSTM, BERT-base and matrix factorisation baselines.

### AI-driven communication automation

In a messaging product AI classifies incoming feedback, routes it, drafts replies and filters content that breaks the rules. This is the direction of his work with Appvillis, the company behind the Nicegram messenger, where his role since April 2023 is AI Software Architect. The architecture of this layer is described on the [AI systems architecture](https://igorshalamov.com/work/ai-systems-architecture/) page.

### Semantic search and classification

Semantic search finds content by meaning rather than by keywords; classification assigns topic, language and risk to each item as it arrives. Research: [Semantic news search using artificial intelligence: technologies, problems and prospects](https://igorshalamov.com/research/semantic-news-search-ai/), which reviews vector databases, hybrid and cascade search and contextual retrieval; [Neural networks for real-time news classification: computational approaches, applications and open problems](https://igorshalamov.com/research/neural-news-classification-real-time/).

## How the architecture is built

The four kinds of systems share one structure:

1. **Event intake.** Actions, messages and content enter through one entry point with a stable schema, so that every later decision can be traced to its input.
2. **Models.** Compact models handle high-volume steps such as classification and embedding; larger models are used for ranking and generation where quality pays for the cost.
3. **Policy layer.** Rules and confidence thresholds decide whether the system acts on its own, suggests an action to a person or escalates.
4. **Attribution and safeguards.** In referral systems, attribution has to survive retries and duplicates, and anti-fraud checks run before any reward.
5. **Measurement.** Each change is compared with a baseline on the same sample or in an A/B test before rollout.

## Igor Shalamov's work in this field

- Shalamov.io (since 2021), founder and platform architect: a platform for referral funnels, lead distribution, automatic messages, partner links, segmentation and analytics, with AI modules for chat assistants, AI segmentation, data analysis and content generation. [Products](https://igorshalamov.com/products/).
- Appvillis UAB (Nicegram), AI Software Architect since April 2023: AI-driven feedback automation and content filtering.
- LaunchHub, head of referral marketing and IT development (since 2022, project-based): referral systems for international Web3 projects.
- Like Center, lead architect of referral systems (2021–2023).

## Research articles

[Semantic news search using artificial intelligence: technologies, problems and prospects](https://igorshalamov.com/research/semantic-news-search-ai/)

Aktualnye issledovaniya, No. 20 (202), 2024. In Russian. DOI 10.5281/zenodo.17215118.

[Neural network architectures for automating user funnels in referral marketing](https://igorshalamov.com/research/neural-architectures-referral-funnels/)

Aktualnye issledovaniya, No. 29 (264), 2025. In Russian.

[AI-driven marketing: the evolution of sales funnels in digital ecosystems](https://igorshalamov.com/research/ai-driven-sales-funnels/)

Internauka, No. 25 (389), 2025. In Russian.

[Neural networks for real-time news classification: computational approaches, applications and open problems](https://igorshalamov.com/research/neural-news-classification-real-time/)

Internauka, No. 35 (399), 2025. In Russian.

[Personalization of news content using AI: architecture and efficiency of neural network systems](https://igorshalamov.com/research/news-personalization-ai/)

European Journal of Technical and Natural Sciences, No. 4–5, 2025, pp. 18–29.

## Related

- [AI systems architecture at Appvillis (Nicegram)](https://igorshalamov.com/work/ai-systems-architecture/)
- [Research and publications](https://igorshalamov.com/research/)
- [Biography, roles and periods](https://igorshalamov.com/about/)

---

Canonical page: https://igorshalamov.com/ai-growth-systems/. Author: Igor Shalamov, AI systems architect who designs AI growth systems. Site guide for AI assistants: https://igorshalamov.com/llms.txt
