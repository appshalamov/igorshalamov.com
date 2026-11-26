---
title: "Uplift modeling explained: pay the referral bonus only where it changes behaviour — Igor Shalamov"
url: https://igorshalamov.com/writing/uplift-modeling-explained/
language: en
author: Igor Shalamov
updated: 2026-11-21
---

# Uplift modeling explained: pay the referral bonus only where it changes behaviour

[Igor Shalamov](https://igorshalamov.com/about/), an AI systems architect and founder of Shalamov.io. 30 November 2026, 2 min read.

A referral bonus sent to 100,000 users raises invitations. Many of those users would have invited friends anyway, and a model trained on who invites will tell you to pay them again next month. Uplift modeling asks a different question: for which users does the bonus change what they do?

## Four kinds of users

- **Persuadables** invite only if they get the bonus.
- **Sure things** invite anyway. For them, the bonus is a gift.
- **Lost causes** never invite, with or without it.
- **Sleeping dogs** react badly: a push for invitations makes them leave.

Only persuadables are worth paying. A response model, also called a propensity model, ranks users by the chance they invite, so it puts sure things at the top and pays for invitations the product would get for free.

## Uplift is a difference

For a user with features x:

`uplift(x) = P(invite | bonus, x) − P(invite | no bonus, x)`

You never observe both outcomes for the same person, so the estimate comes from a randomised test. In the illustrative example from the episode, 5 in 100 users in the control group invite without a bonus and 8 in 100 in the treatment group invite with it. The average uplift is 3 points. The model's job is to predict that difference for each user.

## Building it with two models

The simplest approach, often called the T-learner, trains one model on the bonus group and one on the control group. Each predicts the chance a user invites. For a new user, run both and subtract: the bonus model's score minus the control model's score. Direct methods such as causal forests estimate the difference in one model and are the next step when the two-model estimate is too noisy.

## Checking it with the uplift curve

Run a fresh randomised test and target 30% of users in three ways. In the episode's illustrative numbers, random targeting earns 10 extra invitations per 1,000 users, the top 30% by response score earns 6, and the top 30% by uplift earns 24. Repeat this for every cut-off and you get the uplift curve; the Qini curve is its common variant. The gap above random targeting is what the model is worth.

## Three ways uplift models lie

1. **Training on past campaigns**, where someone chose who got the bonus. Train only on randomised tests and keep a random control group in every campaign.
2. **Ignoring sleeping dogs.** If predicted uplift is below zero, send no offer at all.
3. **Judging by accuracy on the outcome.** A model can predict invitations well and still rank uplift badly. Judge it by the uplift curve on new data.

The same logic applies wherever an action costs money or attention: discounts and coupons, retention offers for users about to leave, and push notifications, where the cost is the user's patience.

## Where uplift fits

Uplift targeting sits in the models layer of an [AI growth system](https://igorshalamov.com/writing/what-is-an-ai-growth-system/): once a referral system knows who is likely to invite, uplift decides whom to pay.

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

Canonical page: https://igorshalamov.com/writing/uplift-modeling-explained/. Author: Igor Shalamov, AI systems architect who designs AI growth systems. Site guide for AI assistants: https://igorshalamov.com/llms.txt
