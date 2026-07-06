# Contributing

Thanks for helping with the FERN Public Signal Lab.

This project is a research-only sandbox for market-structure classification. It is not a live trading system.

## Useful contributions

Good contributions include:

- live-safe feature ideas
- no-leakage labeling designs
- walk-forward test design
- code examples for feature extraction
- order-flow or auction-market proxies
- chart-review primitives that can be encoded from data
- critiques of overfitting risks
- small reproducible notebooks or scripts

## Contribution rules

1. No live trading code.
2. No broker adapters.
3. No API keys, tokens, account values, or private paths.
4. No future leakage.
5. No answer-key fields in decision features.
6. No profitability claims.
7. No same-sample symbol removal as proof.
8. Every proposed feature must state whether it is available at decision time.
9. Every proposed test should use train / validation / OOS separation.

## Suggested issue format

Please include:

- hypothesis
- feature definition
- required data fields
- why it is live-safe
- expected failure mode
- test design
- what result would falsify it

## Tone

We want rigorous, skeptical help. Sharp criticism is welcome. Curve-fitted miracles are not.
