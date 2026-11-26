---
type: playbook
status: draft
owner: [owner]
last_reviewed: 2026-11-26
---

# Fit scoring

How the team scores every lead, inbound and outbound, and how the score gets tighter over time. The [fit scorer](../.claude/agents/fit-scorer.md) owns the model and the improvement loop. The prospector applies the model to each lead. Pipeline keeps the outcomes. The strategist owns the ICP the model starts from.

## Two scores, not one
- **Fit (0 to 100):** how closely the company and person match `icp.md`. Slow to change.
- **Timing (0 to 100):** how strong and recent the trigger is (outbound), or what the lead just did (inbound). Changes week to week.

A perfect fit with no trigger and a weaker fit with an urgent trigger call for different moves, so the two are never blended into one number.

## Bands and what they decide

| Band | Fit | Timing | Default move |
|---|---|---|---|
| A | 70 or more | 70 or more | Priority: personal outreach or a fast inbound reply offering a call |
| B | 70 or more | under 70 | Right company, wrong moment: nurture, and watch for a trigger |
| C | under 70 | 70 or more | Urgent but a weaker fit: answer helpfully; qualify on the call |
| D | under 70 | under 70 | No outreach; inbound gets a polite answer |
| Out | Any disqualifier | Any | No outreach; logged with the reason |

The thresholds start at 70 and move only through calibration (below). Each business can set its own in `scoring.md`.

## The model
Each business's model lives in its `scoring-model.csv`, one rule per row with a version number, and `scoring.md` explains why each rule is there. It lists:
- **Fit factors** with points: for example company type, size, the role of the person, tools they use, region. Each factor traces to `icp.md`.
- **Timing factors** with points: each signal type from [signals.md](signals.md), with points that fall as the signal ages; for inbound, each action type (demo request, pricing page, content download).
- **Disqualifiers:** hard noes from `icp.md` ("who we won't target"), existing customers, opt-outs, competitors.
- **Evidence for each factor:** where it came from (the strategist's hypothesis, a client interview, or a back-test) and its strength.

The model is written so it can be applied the same way every time: points for facts, not judgment. [team/calculations.md](../team/calculations.md#score-leads) says exactly how to apply it, and the scores are computed with a code tool, not estimated. Where the business enriches in Clay, the same rules can also run there as a Clay formula, as long as both give the same scores.

## Applying it
- The prospector scores every list row and every inbound lead as [calculations.md](../team/calculations.md#score-leads) says, and records **fit, timing, band and model version** with the lead.
- A factor with no data scores zero and is marked "unknown"; it is never guessed.
- Scores are recorded in the CRM (as properties) or in the business's `pipeline.csv`, and kept even after the deal closes. The back-test depends on them.

## The improvement loop

**When:** the fit scorer runs a back-test after a business has 20 or more new closed outcomes (won or lost) since the last one and at least a month has passed. The 20 stops changes made on too little evidence; the month stops a fast-closing business from changing its scoring every couple of weeks. Fewer than 20 outcomes in a band means that band's numbers are reported as counts only.

**The back-test reports** ([how to calculate them](../team/calculations.md#back-test-the-scoring-model)):
1. **Conversion by band:** share of leads that reached a meeting held, a qualified opportunity, and a win, for each band. A good model shows A well above B, C and D.
2. **Share of wins from band A.** The higher, the more the score is doing its job.
3. **Misses that matter most:** wins that scored low. What did they have that the model didn't count?
4. **False alarms:** A-band leads that went nowhere, and their lost reasons.
5. **Factor check:** which factors show up more in wins than losses, and which don't.
6. **Inbound and outbound separately,** because the same score can mean different things in each.

**How the model changes:**
- The back-test **lists every problem it finds, ranked by what it costs** (missed wins, wasted effort on false alarms), with the evidence and sample size for each. The decider sees all of them and chooses which to fix.
- **Clear errors are fixed right away** once approved: a broken disqualifier, a factor scored from bad data, a rule that contradicts `icp.md`.
- **Judgment calls are tested one at a time:** a weight, a threshold or a new factor. Changing several at once hides which one helped or hurt, especially with about 20 outcomes per check. The rest wait their turn on the ranked list.
- The reviewer checks the proposal; the decider approves it.
- **The new version runs beside the old one:** every new lead is scored by both, and the new version is promoted only when the next back-test shows it sorts leads better (higher conversion in A, fewer misses). Otherwise the old one stays.
- Each promoted version gets a dated file in the business's `decisions/` and a line in `scoring.md`'s version log.
- When the evidence says the ICP itself is wrong (not just the weights), the fit scorer proposes the change to the strategist, who owns `icp.md`.

## Starting with no data
A new business has no outcomes yet. Version 1 comes from `icp.md` and the strategist's best judgment, every weight labeled an assumption. The first plays then double as tests of the model. Until the first back-test, bands guide the order of work but nothing is ruled out on score alone except disqualifiers.

## Spot checks
Each week the fit scorer re-scores five leads the prospector scored and compares. Differences of more than 10 points on either score are traced to a fact or a rule and fixed, so the scoring stays consistent.
