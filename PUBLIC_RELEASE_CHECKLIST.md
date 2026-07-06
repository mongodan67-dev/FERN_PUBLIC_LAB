# Public Release Checklist

Use this checklist before copying `public_signal_lab/` into the public `FERN_PUBLIC_LAB` repository.

## Release type

- [ ] First release is docs-only.
- [ ] No sample data is included.
- [ ] No scripts, notebooks, runtime code, broker code, or private strategy code are included.
- [ ] The public repo is framed as a research lab, not a trading bot launch.

## Language safety

- [ ] No profitability claims.
- [ ] No implication that the project produces trade signals for public use.
- [ ] No request for contributors to build a money-making system.
- [ ] Research question is stated as continuation vs exhaustion classification.
- [ ] All feature requests require decision-time availability and no future leakage.

## Private-system protection

- [ ] No private FERN source code.
- [ ] No prop-firm harness code or details.
- [ ] No broker adapters or broker workflow details.
- [ ] No account data, balances, fills, orders, or API references.
- [ ] No API keys, tokens, secrets, environment variable names, or credentials.
- [ ] No private local paths.
- [ ] No private logs, candidate dossiers, production runtime details, or internal architecture diagrams.

## Data protection

- [ ] Data dictionary is clearly marked as a draft for future sanitized data.
- [ ] Outcome fields are clearly separated from decision-time features.
- [ ] No answer-key fields appear as decision-time inputs.
- [ ] No raw data is published until a separate sanitation pass is completed.

## Final grep/search terms

Search the release folder for these terms before public copy:

- `FERN_PROP_GAUNTLET`
- `broker`
- `prop`
- `harness`
- `account`
- `API`
- `key`
- `secret`
- `token`
- `runtime`
- `logs`
- `candidate`
- `dossier`
- `C:\`
- `/Users/`
- `.env`

Finding a term is not automatically a failure, but every hit must be intentional, public-safe, and research-framed.

## Publish gate

- [ ] Public export approved by Dan.
- [ ] Public repo name is `FERN_PUBLIC_LAB`.
- [ ] First public commit contains docs only.
- [ ] First GitHub issue asks for missing feature-layer help, not trading execution help.
