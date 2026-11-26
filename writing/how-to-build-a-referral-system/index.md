---
title: "How to Build a Referral System That Works Like a Recommender — Igor Shalamov"
url: https://igorshalamov.com/writing/how-to-build-a-referral-system/
language: en
author: Igor Shalamov
updated: 2026-11-21
---

# How to Build a Referral System That Works Like a Recommender

[Igor Shalamov](https://igorshalamov.com/about/), an AI systems architect and founder of Shalamov.io. 25 November 2026, 2 min read.

Most referral programs are a reward table: invite a friend, get a bonus. But the reward is the easy part. The hard part is deciding who should invite whom. That is a ranking problem, and it makes a referral system a recommender system.

## The problem

Take one user. Call her Ana. In this made-up example, Ana has eight contacts in the app. A static program sends the same invitation to all eight. Two of them join. Six people got a message they did not want. And realistically, Ana will message three people, not eight. So the real question is: which three should the system suggest?

## Architecture

We start from a user graph: contacts, shared groups, interactions. From the graph we generate candidate pairs: an inviter and a possible invitee. A ranking model scores every pair. The best pairs become invitation suggestions. Now the key part: every accepted or ignored invitation becomes a training label. Without the loop, this is automation. With it, the system learns.

## Retrieval

With eight contacts, we could score everyone. With millions of possible pairs we cannot, so retrieval comes first. A two-tower model maps the inviter and every candidate into one vector space. It is trained so that pairs with accepted invitations end up close together. Retrieval is then a nearest neighbour search around Ana. We keep the five nearest candidates.

## Ranking

The ranking model scores these five pairs with richer features. Start with tie strength alone: how often and how recently two people talk. The top three would be Dev, Ben and Chloe. Now add invitee fit: the predicted chance that a new user stays active. The order changes: Fay moves up to second, and Dev drops out of the top three.

## Precision@K

To check the ranking, we use Precision@K. It is the share of the top K suggestions that were accepted. Ana sends three invitations, so K = 3. In our made-up example, two of her eight contacts would accept. Three random picks give a precision of 0.25. Tie strength alone found one of the two: 0.33. The full model found both: 0.67. Same user, same three messages, over two and a half times the random baseline.

## Incremental lift

One trap remains: some invited people would have joined anyway. So keep a holdout group with no model-driven suggestions. Compare it with the group that gets them, and count retained users, not acceptances. These numbers are illustrative. That difference is what the system actually earned.

## Pitfalls

Three things go wrong in practice. First, the feedback loop is biased: the model only sees outcomes for pairs it chose. So keep a small slice of random suggestions. Second, optimising for acceptances rewards pressure. Optimise for retained users, and cap invitations per person. Third, contact data needs explicit consent. Without it, the feature stays off.

## Recap

To recap: a referral system is a recommender over a user graph. Retrieve candidates, rank them, suggest the invitation, and learn from every outcome. Judge it by Precision@K, by retention, and by lift against a holdout.

## Video

Watch the episode: [How to Build a Referral System That Works Like a Recommender](https://youtu.be/fzfCppUap7Y)

![Igor Shalamov](https://igorshalamov.com/press-kit/igor-shalamov-160.jpg)

[Igor Shalamov](https://igorshalamov.com/about/) is an AI systems architect who designs AI growth systems: referral and recommendation systems, AI-driven communication automation, semantic search and classification. He founded Shalamov.io and publishes [research](https://igorshalamov.com/research/) on semantic search and neural classification.

## More notes

- [Two Tower Model Explained: Recommendation Retrieval at Scale](https://igorshalamov.com/writing/two-tower-model-explained/)
- [How to Build a Referral Program That Brings Users Who Stay](https://igorshalamov.com/writing/how-to-build-a-referral-program/)
- [How to Evaluate Recommendation Systems: Precision@K, nDCG and A/B Tests](https://igorshalamov.com/writing/how-to-evaluate-recommendation-systems/)
- [Semantic Search vs Keyword Search: How Embeddings Find Meaning](https://igorshalamov.com/writing/semantic-search-vs-keyword-search/)
- [Uplift modeling explained: pay the referral bonus only where it changes behaviour](https://igorshalamov.com/writing/uplift-modeling-explained/)

Subscribe: [RSS feed](https://igorshalamov.com/writing/feed.xml). All notes: [Writing](https://igorshalamov.com/writing/).

---

Canonical page: https://igorshalamov.com/writing/how-to-build-a-referral-system/. Author: Igor Shalamov, AI systems architect who designs AI growth systems. Site guide for AI assistants: https://igorshalamov.com/llms.txt
