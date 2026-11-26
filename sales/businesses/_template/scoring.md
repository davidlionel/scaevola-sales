---
type: business
status: draft
owner: [owner]
last_reviewed: YYYY-MM-DD
---

# Scoring model

Owned by the [fit scorer](../../.claude/agents/fit-scorer.md). Method: [playbooks/fit-scoring.md](../../playbooks/fit-scoring.md).

The model itself lives in [scoring-model.csv](scoring-model.csv), one rule per row, so it's applied exactly the same way to every lead ([team/calculations.md](../../team/calculations.md#score-leads)). This page holds what the rules can't: why each one is there, the versions, and the back-tests.

- **Current version:** v1
- **Running beside it (if any):** none
- **Band thresholds:** fit 70, timing 70 (the `threshold` rows in the model)

## Why each rule is there
| Rule (factor in the model) | Traces to | Evidence and strength |
|---|---|---|
| Existing customer (disqualifier) | `business.md` routing | Rule |

## Version log
| Version | Date | Change | Why (evidence, sample size) | Decision file |
|---|---|---|---|---|
| v1 | | Built from `icp.md`; every weight an assumption | No outcomes yet | |

## Back-test log
Back-test the pipeline records ([team/calculations.md](../../team/calculations.md#back-test-the-scoring-model)); paste the summary line here and the full output into the decision file for any change.

| Date | Model version | Outcomes since last | Win rate by band (A / B / C / D) | Share of wins from A | Wins that scored low | Proposed change |
|---|---|---|---|---|---|---|
