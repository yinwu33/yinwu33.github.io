---
title: "CounterPlay: Counterfactual Post-Training for Self-Play Driving Policies"
collection: publications
category: preprints
permalink: /publication/counterplay2026
homepage: true
date: 2026-09-18
venue: "Preprint"
authors:
  - Jiarong Wei
  - Yin Wu
  - Runkai He
  - Abhinav Valada
cover: /images/publications/counterplay/cover.jpg
cover_alt: "A self-play policy repeatedly times out; CounterPlay backtracks to an earlier state and retries under alternate driving styles"
pdf: "https://arxiv.org/pdf/2609.21617"
paperurl: "https://arxiv.org/abs/2609.21617"
excerpt: "A counterfactual post-training approach for self-play driving policies that backtracks from failed tasks and retries them under alternate driving styles."
citation: 'Wei, Jiarong, et al. "CounterPlay: Counterfactual Post-Training for Self-Play Driving Policies." arXiv preprint arXiv:2609.21617 (2026).'
---

CounterPlay backtracks from failed self-play tasks to an earlier stored state, retries them under driving styles from cautious to aggressive, keeps only retries that harm no other vehicle, and distills them into the policy. On BehaviorBench it reaches state-of-the-art scores on both the Interactive and Random splits using 1% of the anchor policy's self-play training budget.
