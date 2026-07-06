# FERN Public Signal Lab

Research-only public problem kit for a market-structure classification problem.

This is not the private FERN system, not a trading bot, and not live-execution code.

## Problem

An OHLCV-based intraday selector appears to detect important market imbalance, but clean out-of-sample tests show that it often confuses direction or action type.

Observed research results so far:

- simple exit variants did not solve the issue
- symbol-level exclusion overfit and inverted out of sample
- several negative signals are structured rather than random
- current numeric features make some future winners and losers look similar
- human chart review suggests a missing feature layer

Working question:

What live-safe feature layer separates continuation from exhaustion when standard OHLCV features flatten them into the same profile?

## Help wanted

We are looking for ideas, code examples, and review around live-safe features for:

- continuation vs exhaustion
- liquidity sweep and reclaim quality
- late chase vs healthy expansion
- meaningful location vs midair signal
- VWAP and auction-location context
- order-flow or volume-at-price proxies
- regime/cold-period detection
- meta-labeling: take, avoid, delay, or reduce risk

## Guardrails

- research only
- no live trading
- no broker adapters
- no account data
- no API keys
- no future leakage
- no answer-key fields
- train / validation / out-of-sample discipline required
- every feature must be computable at decision time

## Public scope

This folder is intended to become a sanitized public repository named `FERN_PUBLIC_LAB`.

The first public release is docs-only: problem statement, benchmark summary, data dictionary draft, contribution rules, issue prompts, release checklist, and sanitization notes.

No sample data, scripts, notebooks, production code, runtime code, broker code, account data, private logs, or candidate dossiers are included in the first release. Any future sample data requires a separate sanitation pass before publication.
