---
layout: post
title: "Listwise Learning to Rank: From ListNet to LLM Re-Rankers"
date: 2025-08-20 10:00:00+0800
description: A short reading note on the evolution of listwise learning-to-rank, from classic probabilistic losses to large language model re-rankers.
tags: learning-to-rank listwise information-retrieval llm
categories: reading-notes
related_posts: false
---

Ranking a list of documents for a query is the core problem of information retrieval. Among the three classic learning-to-rank (LTR) paradigms — pointwise, pairwise, and listwise — the **listwise** approach directly optimizes over the whole ranked list, which aligns best with list-level evaluation metrics such as NDCG and MAP. Below is a brief reading note tracing its evolution.

#### Classic listwise methods

- **ListNet** (Cao et al., *ICML 2007*, "Learning to Rank: From Pairwise Approach to Listwise Approach") introduced a probabilistic model over permutations. Using the Plackett–Luce top-one probability, it defines a cross-entropy loss between the predicted and ground-truth score distributions, making the whole list the unit of learning.

- **ListMLE** (Xia et al., *ICML 2008*, "Listwise Approach to Learning to Rank: Theory and Algorithm") replaces the cross-entropy surrogate with the negative log-likelihood of the ground-truth permutation, and studies the consistency and soundness of listwise losses theoretically.

- **LambdaMART** (Burges, 2010, "From RankNet to LambdaRank to LambdaMART") combines gradient boosted trees with the *lambda gradients* that directly incorporate the change in NDCG when swapping a pair. For years it remained the strongest practical LTR model and a standard baseline in industry.

#### The LLM era

Large language models reshaped re-ranking by treating it as a **sequence generation** problem rather than pure scoring:

- **RankGPT** (Sun et al., *EMNLP 2023*, "Is ChatGPT Good at Search? Investigating Large Language Models as Re-Ranking Agents") prompts an LLM to output a permutation of candidate passages directly, and proposes a *sliding-window* strategy plus *permutation distillation* into smaller specialized rankers.

- Follow-ups such as **RankVicuna** and **RankZephyr** distill this listwise ranking ability into open-source models, achieving strong zero-shot effectiveness while being reproducible.

#### Takeaways

The through-line is clear: define the objective at the *list* level so it matches the metric we truly care about. Classic methods encode this via permutation probabilities; modern LLM re-rankers encode it by directly generating an ordering. My own work on search-quality evaluation builds on this listwise philosophy — evaluating and comparing whole result pages rather than isolated items.
