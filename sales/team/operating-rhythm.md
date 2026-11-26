---
type: team
status: draft
owner: [owner]
last_reviewed: 2026-11-24
---

# Operating rhythm

How a business runs, from intake to a predictable number. The stage rules are in [playbooks/pipeline-stages.md](../playbooks/pipeline-stages.md).

## The cycle

| Step | Who | Output | Gate |
|---|---|---|---|
| 1. Intake | Strategist | The business pack in `businesses/<name>/` | Decider approves `icp.md`, `offer.md` and `targets.md` |
| 2. Motion | Strategist, with the motion repo | The motion scorecard (the business's current approach scored against the motion's best practice), and `motion.md` naming the motion repo(s) and what changes for the core team | Decider approves |
| 3. Play plan | Sales manager | `plays/<date>-<name>/plan.md`: one buyer, one trigger, the list size, confirm and kill counts | Reviewer, then decider |
| 4. List | Prospector | `list.md`: every row has the signal, its date, the source link, and its fit and timing scores from the current model | Reviewer spot-checks 10 rows; fit scorer spot-checks 5 scores a week |
| 5. Messages | Outreach | `drafts.md`: first message plus up to two follow-ups per row | Reviewer, then decider. A person sends |
| 6. Conversations | Deal support | Call prep before each call; notes and follow-up after | A person runs the call |
| 7. Tally | Pipeline | `tally.md` and the business's `pipeline.md` updated | None |
| 8. Weekly review | Sales manager, with pipeline | Keep, change or stop each play; the one decision needed | Decider |
| 8b. Score back-test | Fit scorer | After 20 or more new outcomes have closed and at least a month has passed: conversion by band, every problem found, ranked by cost, and the proposed fixes ([fit-scoring.md](../playbooks/fit-scoring.md)) | Reviewer, then decider |
| 9. Learn | Whoever was corrected | A lesson in [lessons.md](../lessons.md) or the business's `decisions/` | Decider confirms on Sundays |

## Inbound and outbound
The cycle above runs outbound plays: the team finds the buyer. Leads that come to the business run on the inbound path in [playbooks/inbound.md](../playbooks/inbound.md): acknowledge, research, fit and route, reply, call, record. A business can run either direction or both; `business.md` says which inbound channels the team watches, and the weekly review covers both, split by source.

## The report path
A business can start with a growth report instead of plays, or only ever want reports (for example, an employer that wants strategy). Either way it goes through step 2 first: the motion repo scores the business against its motion's best practice, and the report uses that score. The report's steps are in [playbooks/growth-report.md](../playbooks/growth-report.md). Its approved moves become the business's first plays.

## Weekly review (one page)
The numbers come from the tally in [team/calculations.md](calculations.md#tally-and-forecast), run on the business's pipeline records.

1. **The number:** revenue won this week and to date, against the target in `targets.md`.
2. **Each live play:** sent, replies (positive, negative, "not now", "already covered"), meetings held, qualified opportunities, won. Say plainly when a confirm or kill count is hit.
3. **What buyers actually did** (not what they said): who booked, who showed, who paid.
4. **Conversion between stages** once there are at least 20 in a stage. Below that, report counts only and say the sample is small.
5. **Keep, change or stop,** with the cascade level the change sits at.
6. **The one decision needed,** as a yes or no question.
7. **Scaevola Sales update:** compare the version in `CLAUDE.md` with VERSION in https://github.com/davidlionel/scaevola-sales. If the public one is newer, list each change in one line from its CHANGELOG.md and say "paste PROMPT.md to update". If they're the same, or the public repository can't be reached, leave this line out.

## Making the number predictable
Work back from the revenue goal in `targets.md`:

> revenue goal / average deal value = deals needed
> deals needed / win rate = qualified opportunities needed
> opportunities / meeting-to-opportunity rate = meetings needed
> meetings / reply-to-meeting rate = positive replies needed
> replies / reply rate = people to reach

Until a business has its own history, every rate is a labeled assumption, not a fact. Replace each one with the business's real rate once a stage has 20 or more records. A forecast is only as good as the rates under it; the weekly review says which are real and which are still guesses.

## Making it profitable
- Every price, discount or custom term is checked against the business's pricing rules in `offer.md`. Anything outside them goes to the decider.
- Track cost per won deal (time, tools, spend) once there's spend to track.
- Retention and expansion are cheaper than new customers. A retention role is planned for a later version.
