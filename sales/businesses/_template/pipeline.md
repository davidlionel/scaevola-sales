---
type: business
status: draft
owner: [owner]
last_reviewed: YYYY-MM-DD
---

# Pipeline

Live deals by stage, for businesses without a connected CRM. If the business has one, it's the source of truth and this file says so. Stages and exit rules: [playbooks/pipeline-stages.md](../../playbooks/pipeline-stages.md).

The records live in [pipeline.csv](pipeline.csv), one row per lead, so the team can calculate from them (format: [team/calculations.md](../../team/calculations.md#the-files)). With a CRM, a CSV export in the same columns does the same job. The weekly numbers come from the [tally](../../team/calculations.md#tally-and-forecast) and the scoring check from the [back-test](../../team/calculations.md#back-test-the-scoring-model).

## Suppression list
People and companies who opted out or asked not to be contacted live in [suppression.csv](suppression.csv). Every new list is checked against it ([dedupe](../../team/calculations.md#drop-duplicates-dedupe)).
