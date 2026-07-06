# Problem Statement

## Core hypothesis

The current feature set may be missing a market-structure sense organ.

The selector is not purely random. It finds recurring imbalance, but the action assignment is unreliable. A signal may mean continuation, exhaustion, delay, avoid, or reduced risk rather than a simple directional entry.

## What failed cleanly

Recent clean out-of-sample research rejected several easy answers:

1. Exit variants were not the missing key.
2. A fixed wider target improved some slices but did not produce a robust long book.
3. Ride-follow style management tied fixed-target exits and was not independently promotable.
4. Symbol bans failed train-to-OOS discipline.
5. Same-sample TSLA removal looked good but was not valid.
6. Broad context gating was weaker than ranking/contextual use.

## What remains interesting

Several negative signals were structured. That suggests the system may detect imbalance before it knows the right response.

The open research question is whether a missing feature layer can map a detected imbalance into one of these labels:

- continue
- exhaust
- avoid
- delay
- reduce risk
- retest required

## Desired help

We need outside review on:

- live-safe feature engineering
- no-leakage labeling methods
- train / validation / OOS test design
- OHLCV limitations
- order-flow or auction-market proxies
- continuation vs exhaustion detection
- human chart-review features that can be encoded

## Non-goals

- no live trading system
- no broker integration
- no profit claims
- no paid signal service
- no closed-source strategy dump
- no parameter curve-fitting
