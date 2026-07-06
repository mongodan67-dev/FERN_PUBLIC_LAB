# Issue Prompts

Use these prompts to turn outside feedback into testable research tickets.

## Feature idea

Title: Feature idea: <name>

- Hypothesis:
- Required data:
- Available at decision time? yes/no:
- Leakage risk:
- Expected behavior:
- Test split:
- What would falsify it:
- Implementation difficulty:

## Continuation vs exhaustion

Title: How should we distinguish continuation from exhaustion?

Context:
An OHLCV selector detects imbalance but sometimes assigns the wrong action.

Questions:
- What live-safe features help identify exhaustion?
- What live-safe features help identify continuation?
- Can the idea be tested without future information?

## Data source suggestion

Title: Data source suggestion: <source>

- What data is provided?
- Cost or access constraints:
- Historical availability:
- Decision-time availability:
- Useful fields:
- Integration difficulty:

## Test design critique

Title: Test design critique: <topic>

- Current test weakness:
- Proposed correction:
- How to avoid leakage:
- How to handle symbol and time holdouts:
- What failure would look like:
