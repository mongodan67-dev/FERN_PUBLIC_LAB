# Fear/Greed Regime Thermostat Lead

Status: research backlog lead only.

Guardrails:
- Do not run a proof yet.
- Do not change live logic.
- Do not add external data code yet.
- Do not commit production changes.

## Source idea

Fear and Greed Index + Markov switching regression regime filter.

## Why it matters to FERN

Recent public-lab findings suggest the missing edge may not be a simple hostile/risk-off avoidance problem:

- Risk-on/supportive longs lost.
- Hostile/risk-off was not the obvious problem.
- This points toward continuation-vs-exhaustion timing rather than a broad market-danger filter.

FERN may need a regime thermostat that asks whether a long candidate is being entered during useful recovery energy or during late-extension greed.

## Hypothesis

FERN may be buying greed / late extension.

Long entries may work better in fear or post-fear recovery than during mature greed regimes, where apparent continuation can actually be exhaustion.

## Test design

1. Build a decision-time fear/greed proxy.
   - Use only features available before the trade decision.
   - Keep this proxy separate from live logic until tested.

2. Classify fear/greed regime.
   - Candidate approaches:
     - Markov switching regression / hidden regime filter.
     - Percentile-state classifier as a simpler baseline.
   - Map the lower-mean regime to fear.

3. Test FERN entries by regime.
   - Slice existing FERN entry outcomes by fear, greed, and post-fear recovery states.
   - Compare hit rate, expectancy, drawdown, MAE/MFE, and time-to-resolution.

4. Test random entries by regime as control.
   - Determine whether any regime advantage is FERN-specific or merely a market-wide drift artifact.
   - Random control must use the same decision-time universe and same leakage rules.

5. Test sustained-dump fade by regime.
   - Check whether sustained-dump fade behavior improves in fear or post-fear recovery states.
   - Separate genuine recovery from knife-catching during active breakdown.

## Leakage rules

- Use only data known before trade.
- Decision-time regime state only; no future candles, future index values, or post-trade normalization.
- Map lower-mean regime to fear.
- No same-sample threshold tuning.
- Train thresholds/regime definitions on train only, then evaluate OOS.
- Do not select symbols or time windows based on OOS results.

## Public campaign use

Add as a GitHub issue / post topic:

**Regime thermostat for continuation vs exhaustion**

Public framing:

> FERN may not simply need a better risk-off filter. The failed long edge may be buying too much late greed / extension. We want to test whether continuation entries behave differently in fear, post-fear recovery, and greed states using decision-time-only regime labels and random-entry controls.

## Non-goals for now

- No proof run.
- No production logic change.
- No broker/runtime integration.
- No external-data ingestion code.
- No live decision authority.
