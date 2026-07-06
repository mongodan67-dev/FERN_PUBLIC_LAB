# Sanitized Benchmark Results

These are high-level research findings only. They are not strategy recommendations and should not be treated as financial advice.

## Summary

The research arc tested whether the current selector could be rescued through context gates, exit management, symbol exclusions, or simple poison flags.

The answer so far: most simple levers failed under honest out-of-sample discipline.

## Findings

### Context/ranking

- Context used as a hard gate failed.
- Context used as a ranker improved the baseline directionally but did not create a robust edge.

### Exit management

- Fixed wider targets helped some samples.
- Ride-follow management was directionally useful but statistically tied with a fixed wider target.
- Profit-protect overlays were neutral.
- More exit variants are unlikely to solve the missing-feature problem.

### Realm behavior

- Crypto remained negative under the tested exit shapes.
- Stocks looked promising in a small sample but failed at higher cadence.
- Stock short diagnostics were positive in one audit but not promoted because they violated project doctrine and require stronger proof.

### Symbol exclusions

- Train-discovered bad-symbol lists inverted out of sample.
- Same-sample symbol removals can look excellent and still be invalid.
- Symbol bans are not a reliable lever from the current evidence.

### OHLCV poison primitives

Derivable older primitives were retested:

- chase / extension poison: weak avoid signal, not enough by itself
- sustained-dump poison: structured negative signal, possible inverse/avoid research lead
- repair-pressure-release: inverted and became a loser signal on the clean foundation

## Current useful research lead

The most interesting remaining lead is not a broad filter. It is the possibility that some negative imbalance signals indicate the wrong action type, not useless noise.

Research question:

Can a feature layer distinguish continuation from exhaustion before assigning action?

## What would count as progress

A contribution is useful if it:

- is computable at decision time
- avoids future leakage
- improves train-to-OOS behavior
- explains continuation vs exhaustion better than current OHLCV features
- does not depend on same-sample symbol removal
- has clear failure reporting
