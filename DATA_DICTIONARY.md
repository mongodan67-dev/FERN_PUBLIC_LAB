# Data Dictionary Draft

This is a draft schema for future sanitized sample data. Do not publish private logs, broker data, account values, API paths, or full production feature dumps.

## Candidate-level columns

| Column | Type | Description |
|---|---|---|
| candidate_id | string | Anonymous candidate identifier |
| timestamp | datetime | Decision timestamp, rounded or bucketed if needed |
| symbol_group | string | Optional anonymized symbol or sector/group |
| realm | category | Market family, e.g. stocks or crypto |
| side | category | Proposed direction at decision time |
| session_bucket | category | Open, midday, close, overnight, or other bucket |
| regime_bucket | category | Optional regime/context bucket if live-safe |
| feature_snapshot_id | string | Reference to the row's feature snapshot |
| decision_label | category | Proposed action label in the research set |
| outcome_label | category | Future result label, withheld from decision features |
| final_r | numeric | Outcome in R units, used only after decision seal |
| mfe_r | numeric | Maximum favorable excursion after decision, outcome-only |
| mae_r | numeric | Maximum adverse excursion after decision, outcome-only |

## Live-safe feature examples

| Feature | Description |
|---|---|
| ret_4 | Recent return over 4 bars |
| ret_8 | Recent return over 8 bars |
| ret_24 | Recent return over 24 bars |
| vwap_dist | Distance from VWAP or VWAP proxy at decision time |
| upper_wick | Upper-wick proportion at decision time |
| red_pressure | Recent downside pressure proxy |
| volume_z | Relative volume z-score |
| range_24 | Recent range proxy |
| atr_pct | ATR as percent of price |

## Derived research flags

| Flag | Description |
|---|---|
| chase_or_extension_poison | Candidate appears extended/chase-like using only live-safe OHLCV fields |
| sustained_dump_poison | Candidate appears to follow a sustained downside move using live-safe OHLCV fields |
| repair_pressure_release | Older pressure-release primitive, currently not trusted |

## Strict separation

Decision-time inputs may not include:

- final_r
- win/loss labels
- MFE/MAE
- exit reason
- future bars
- scenario-family fields derived after outcome
- any manually added answer-key tags

Outcome fields can be used only for evaluation after the decision packet is sealed.
