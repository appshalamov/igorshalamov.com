---
title: "How a feedback system in a messenger works — Igor Shalamov"
url: https://igorshalamov.com/writing/feedback-system-in-a-messenger/
language: en
author: Igor Shalamov
updated: 2026-11-21
---

# How a feedback system in a messenger works

[Igor Shalamov](https://igorshalamov.com/about/), an AI systems architect and founder of Shalamov.io. 21 November 2026, 1 min read.

At Appvillis UAB, the developer of the Nicegram messenger, I work as AI Software Architect on AI-driven feedback automation. Here is the general shape of such a system.

1. **Intake**: every message from a user lands in one queue, whatever the channel.
2. **Understanding**: models classify the topic, the intent and the sentiment.
3. **Routing**: simple cases get an answer at once; complex or emotional ones go to a person, with context attached.
4. **Reply**: a generated draft that a person can send as is or edit.
5. **Learning**: every edit and every escalation becomes training data.

The fifth step is what turns automation into a [growth system](https://igorshalamov.com/writing/what-is-an-ai-growth-system/).

![Igor Shalamov](https://igorshalamov.com/press-kit/igor-shalamov-160.jpg)

[Igor Shalamov](https://igorshalamov.com/about/) is an AI systems architect who designs AI growth systems: referral and recommendation systems, AI-driven communication automation, semantic search and classification. He founded Shalamov.io and publishes [research](https://igorshalamov.com/research/) on semantic search and neural classification.

## More notes

- [Uplift modeling explained: pay the referral bonus only where it changes behaviour](https://igorshalamov.com/writing/uplift-modeling-explained/)
- [News personalization with BERT and LSTM: one model for the article, one for the reader](https://igorshalamov.com/writing/news-personalization-bert-lstm/)
- [One pipeline for intent, sentiment and toxicity](https://igorshalamov.com/writing/one-pipeline-intent-sentiment-toxicity/)
- [Telegram Mini Apps as a recommendation surface](https://igorshalamov.com/writing/telegram-mini-apps-recommendation-surface/)
- [How to measure personalization](https://igorshalamov.com/writing/how-to-measure-personalization/)

Subscribe: [RSS feed](https://igorshalamov.com/writing/feed.xml). All notes: [Writing](https://igorshalamov.com/writing/).

---

Canonical page: https://igorshalamov.com/writing/feedback-system-in-a-messenger/. Author: Igor Shalamov, AI systems architect who designs AI growth systems. Site guide for AI assistants: https://igorshalamov.com/llms.txt
