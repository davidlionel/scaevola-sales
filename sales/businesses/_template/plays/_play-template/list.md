---
type: play
status: draft
owner: [owner]
last_reviewed: YYYY-MM-DD
---

# List

Every row needs a dated, linked signal. Rules: [playbooks/signals.md](../../../../playbooks/signals.md).

The rows live in [list.csv](list.csv) so the team can calculate from them ([team/calculations.md](../../../../team/calculations.md)). Before the list goes to outreach, the prospector runs, in order:
1. Freshness: drop rows whose signal is older than the play's window.
2. Dedupe: drop rows already in the pipeline, the CRM or another live play, or on the suppression list.
3. Score: fit, timing, band and model version from the business's `scoring-model.csv` ([fit-scoring.md](../../../../playbooks/fit-scoring.md)).

Notes on the list (where it came from, anything unusual) go here.
