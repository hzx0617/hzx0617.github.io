---
layout: post
title: "LLM Agents: From ReAct to Reflection and Tool Use"
date: 2025-09-10 10:00:00+0800
description: A short reading note on the key paradigms that turn large language models into autonomous agents — reasoning-acting loops, self-reflection, tool use, and lifelong exploration.
tags: llm agent reasoning tool-use reinforcement-learning
categories: reading-notes
related_posts: false
---

An *agent* is a system that perceives, reasons, and acts to accomplish a goal. Large language models make surprisingly capable agent backbones: they can plan in natural language, call external tools, and revise their behavior from feedback. This note summarizes a few foundational papers I keep returning to.

#### Reasoning + acting

- **ReAct** (Yao et al., *ICLR 2023*, "ReAct: Synergizing Reasoning and Acting in Language Models") interleaves *thought* traces with *actions* in a single loop. The model reasons about what to do, takes an action (e.g., a search query), observes the result, and continues. This simple Thought→Action→Observation pattern remains the backbone of most modern agent frameworks.

#### Learning from one's own mistakes

- **Reflexion** (Shinn et al., *NeurIPS 2023*, "Reflexion: Language Agents with Verbal Reinforcement Learning") adds a self-reflection step: after a failed attempt, the agent writes a natural-language critique of what went wrong and stores it in memory, using it to improve subsequent trials — reinforcement learning without gradient updates.

#### Giving models tools

- **Toolformer** (Schick et al., *NeurIPS 2023*, "Toolformer: Language Models Can Teach Themselves to Use Tools") shows an LLM can learn *when* and *how* to call APIs (calculator, search, translation) in a self-supervised way, by deciding which API calls actually reduce its language-modeling loss.

#### Long-horizon exploration

- **Voyager** (Wang et al., 2023, "Voyager: An Open-Ended Embodied Agent with Large Language Models") builds a lifelong-learning agent in Minecraft that maintains a growing *skill library* of reusable code, driven by an automatic curriculum — an early demonstration of open-ended, self-improving behavior.

#### Takeaways

Two ideas recur across these works: (1) **externalizing reasoning** as explicit intermediate steps makes behavior more controllable and debuggable; and (2) **closing the loop with feedback** — from tools, environments, or self-reflection — is what turns a static model into an adaptive agent. Combining these with retrieval and reward modeling is exactly where my current research interests lie.
