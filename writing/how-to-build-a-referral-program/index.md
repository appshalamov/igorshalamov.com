---
title: "How to Build a Referral Program That Brings Users Who Stay — Igor Shalamov"
url: https://igorshalamov.com/writing/how-to-build-a-referral-program/
language: en
author: Igor Shalamov
updated: 2026-11-21
---

# How to Build a Referral Program That Brings Users Who Stay

[Igor Shalamov](https://igorshalamov.com/about/), an AI systems architect and founder of Shalamov.io. 28 November 2026, 3 min read.

Your referral program brings sign-ups. Then they never pay. Some are fake accounts. The rest leave within a week. The reward is not the problem. The system around it is.

## Architecture

A referral program is not a share button. It is a system with five parts. Attribution records who brought whom. Reward rules decide what each side gets, and for what. Fraud checks stop fake invitations before anyone is paid. Targeting chooses who to ask, and when. Measurement tells you whether any of it worked. And the results flow back: they retrain targeting and tune the rewards.

## Attribution

Start with attribution, because every reward depends on it. Each inviter gets a unique link or code. Then set an attribution window: for example, the friend must sign up within 7 days of the click. The hard part is devices. The friend taps the link on a phone, then signs up on a laptop. So carry the code through the app install, or ask for it at sign-up. And when two people invited the same friend, one written rule decides who gets credit.

## Rewards

Paying for a sign-up rewards empty accounts. Pay for a target action instead: a first purchase, or still being active on day 30. If only the inviter is paid, the friend has no reason to act. A two-sided reward gives both people something real. And cash for any invitation attracts people who farm rewards. Product value, like credits or extra plan time, with a cap per person, attracts people who use the product.

## Fraud

Any reward worth having will be gamed. The simplest fraud is a self-invite: a second account for yourself. The signal: the same device or the same payment card on both sides. Then account farms: dozens of sign-ups from one source. The signal: many accounts behind one IP address. And bots that rush through the target action. The signal is velocity: too many steps, too fast. Combine the signals into a risk score, and hold the reward until the checks pass.

## Targeting

Most programs ask everyone right after sign-up, before the user has seen any value. Ask after the aha moment, the first time the product delivers real value. Ranked by activity alone, the busiest users come first. A propensity model predicts something better: the chance that this user invites a friend who stays. Chloe is quiet, but her friends stay. She moves up to second. Ask the top users first, and cap how often anyone is asked.

## K-factor

Now measurement. The classic number is the K-factor. It equals invitations per user, times the share of invitations that convert. In a made-up example, 100 users send 3 invitations each, and 10% convert. 3 × 0.1 gives a K-factor of 0.3. Now count only the invited users still active on day 30: 12 of them. The K-factor that matters is 0.12. Above one, growth feeds itself. Below one, referrals amplify your other channels, but do not replace them.

## Incrementality

The K-factor has a blind spot: some invited friends would have joined anyway. So keep a holdout: a random group of users who never see the program. Compare them with everyone else, and count retained users, not sign-ups. These numbers are illustrative. If the gap is close to zero, you are paying rewards for users you would have had anyway.

## Mistakes

Four mistakes show up again and again. Paying for sign-ups instead of users who stay. Paying rewards before the fraud checks are done. Asking for invitations before the user has seen any value. And trusting the K-factor without a holdout. Fix these four, and each part of the system starts to work for the next one.

## Recap

To recap: attribute every invitation, reward the action that matters, and check for fraud before paying. Ask the right users after the aha moment, and judge the result against a holdout.

## Video

Watch the episode: [How to Build a Referral Program That Brings Users Who Stay](https://youtu.be/PbHN5ZZMan4)

![Igor Shalamov](https://igorshalamov.com/press-kit/igor-shalamov-160.jpg)

[Igor Shalamov](https://igorshalamov.com/about/) is an AI systems architect who designs AI growth systems: referral and recommendation systems, AI-driven communication automation, semantic search and classification. He founded Shalamov.io and publishes [research](https://igorshalamov.com/research/) on semantic search and neural classification.

## More notes

- [Two Tower Model Explained: Recommendation Retrieval at Scale](https://igorshalamov.com/writing/two-tower-model-explained/)
- [How to Evaluate Recommendation Systems: Precision@K, nDCG and A/B Tests](https://igorshalamov.com/writing/how-to-evaluate-recommendation-systems/)
- [Semantic Search vs Keyword Search: How Embeddings Find Meaning](https://igorshalamov.com/writing/semantic-search-vs-keyword-search/)
- [How to Build a Referral System That Works Like a Recommender](https://igorshalamov.com/writing/how-to-build-a-referral-system/)
- [Uplift modeling explained: pay the referral bonus only where it changes behaviour](https://igorshalamov.com/writing/uplift-modeling-explained/)

Subscribe: [RSS feed](https://igorshalamov.com/writing/feed.xml). All notes: [Writing](https://igorshalamov.com/writing/).

---

Canonical page: https://igorshalamov.com/writing/how-to-build-a-referral-program/. Author: Igor Shalamov, AI systems architect who designs AI growth systems. Site guide for AI assistants: https://igorshalamov.com/llms.txt
