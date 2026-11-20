---
title: "AI Systems Architecture — Igor Shalamov"
url: https://igorshalamov.com/work/ai-systems-architecture/
language: en
author: Igor Shalamov
updated: 2026-11-21
---

# AI systems architecture

Since April 2023 Igor Shalamov, an AI systems architect and founder of Shalamov.io, has worked with Appvillis, the developer of the Nicegram messenger, on AI-driven feedback automation and content filtering. His role at Appvillis is AI Software Architect and Head of Referral Marketing.

This page describes the engineering discipline behind that work: how AI automation is designed for a messaging product with a large audience, and which decisions matter at each layer.

## Where AI belongs in a communication product

In a messenger, AI does several distinct jobs: it classifies incoming user feedback, routes it to the right queue, drafts replies, and filters content that breaks the rules. Each job has its own cost of error. A wrong draft reply can be corrected by a person; a wrongly blocked message damages trust. Architecture starts by listing these jobs separately and assigning each one its own model, threshold and review path.

## The pipeline

1. **Intake.** Messages and feedback arrive through one entry point with a stable schema: source, language, time, user context that the product is allowed to use.
2. **Queue.** A message queue absorbs peaks so that model latency never blocks the product. Each job reads from its own queue and can be scaled on its own.
3. **Classification.** Fast, inexpensive classifiers decide topic, language, urgency and risk. Large language models are reserved for the steps that need generation.
4. **Policy layer.** Rules and confidence thresholds decide what happens next: automatic action, a suggested reply for a person, or escalation.
5. **Action and logging.** Every automated decision is logged with the model version and the input it saw, so that it can be audited and reversed.

## Choosing models

The main trade-off is quality against cost per request and latency. High-volume steps such as language detection and topic classification run on compact models. Generation runs on larger models only where a person or a user will read the result. Models are versioned, and a new version replaces the old one only after it is compared on the same labelled sample.

## Guardrails

- Confidence thresholds: below the threshold, the system suggests rather than acts.
- Human review for actions that are hard to undo, such as blocking content.
- Data minimisation: models receive only the fields the task needs.
- Audit trail: every decision can be traced to a model version and a rule.
- Fallbacks: if a model is unavailable, messages wait in the queue instead of being processed by a weaker rule.

## Metrics

An AI feature is judged by measured results, not by the presence of a model. Typical measures are precision and recall of the content filter on a labelled sample, the share of feedback resolved without escalation, time to first response, the rate of reversed automated decisions, and the cost per thousand processed messages. Each metric is compared with a baseline before and after the change.

## Connection to growth systems

The same principles apply to referral and recommendation systems: clean event intake, attribution that survives retries and duplicates, anti-fraud checks before rewards, and A/B tests before rollout. Igor Shalamov's research on [neural network architectures for referral funnels](https://igorshalamov.com/research/neural-architectures-referral-funnels/) covers this side. The field as a whole: [AI growth systems](https://igorshalamov.com/ai-growth-systems/).

## Related

- [Biography, roles and periods](https://igorshalamov.com/about/)
- [Research and publications](https://igorshalamov.com/research/)
- [Press kit](https://igorshalamov.com/press-kit/)

---

Canonical page: https://igorshalamov.com/work/ai-systems-architecture/. Author: Igor Shalamov, AI systems architect who designs AI growth systems. Site guide for AI assistants: https://igorshalamov.com/llms.txt
