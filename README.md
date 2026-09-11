# Property-Driven AI-Assisted Security Reviews

This is the accompanying repository for the blog post **"Property-Driven AI-Assisted Security Reviews."**

The post asks a simple question: when you ask an LLM to help you audit a codebase, what should you actually tell it to look for? We compared a blind audit against several ways of framing the same guidance — a plain bug description, increasingly detailed hints, a system-level property the code must preserve, that property plus a verification procedure, and an attack narrative — across three real-world vulnerabilities (Sonne Finance, Pareto's sUSP vault, and Napier's `BaseLSTAdapter`) that all stem from the same broken invariant: exchange rate integrity between an underlying asset and its receipt token.

This repo contains the raw material used to run that evaluation:

- [`cases/`](cases/) — the three vulnerable codebases/commits used in the evaluation
- [`prompts/`](prompts/) — the audit prompts for each instruction condition (blind, targeted/hints, invariant/property, invariant + procedure, attack framing)
- [`invariants/`](invariants/) — the shared exchange-rate-integrity property definition
- [`attacks/`](attacks/) — the attack-framing description of the same underlying issue

