# Sanitization Notes

These notes document the public-scope boundary for the first `FERN_PUBLIC_LAB` release.

## Scope reviewed

The public kit is limited to documents under `public_signal_lab/`:

- `README.md`
- `PROBLEM_STATEMENT.md`
- `BENCHMARK_RESULTS.md`
- `DATA_DICTIONARY.md`
- `CONTRIBUTING.md`
- `ISSUE_PROMPTS.md`
- `PUBLIC_RELEASE_CHECKLIST.md`
- `SANITIZATION_NOTES.md`

## Public framing

The release describes a research-only market-structure classification problem:

> An OHLCV-based intraday selector appears to detect meaningful imbalance, but often assigns the wrong action type.

The public research question is:

> What live-safe feature layer separates continuation from exhaustion when ordinary OHLCV features make winners and losers look similar?

## Explicitly excluded

The public release must not include:

- private FERN source code
- production runtime code
- broker code or broker adapters
- prop-firm harness code or implementation details
- account information
- API keys, tokens, credentials, environment variable names, or secrets
- local filesystem paths
- private logs
- candidate dossiers
- raw trade records
- private architecture diagrams
- unsanitized sample data
- claims of profitability

## Data status

No sample data is approved for the first public release.

The data dictionary is a draft schema only. It describes what a future sanitized research packet might contain after a separate sanitation pass.

Any future data release must be reviewed separately for:

- symbol anonymity or acceptable public symbol handling
- timestamp precision and bucketing
- removal of private candidate identifiers
- removal of private logs and runtime metadata
- strict separation of decision-time fields from outcome fields
- no answer-key leakage
- no account, broker, fill, order, or balance information

## Current release judgment

The current kit is suitable for a docs-only public export after final manual review against `PUBLIC_RELEASE_CHECKLIST.md`.

The next public step should be creation of a clean public repository named `FERN_PUBLIC_LAB`, followed by a first issue asking for missing feature-layer suggestions.
