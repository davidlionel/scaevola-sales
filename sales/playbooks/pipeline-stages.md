---
type: playbook
status: draft
owner: [owner]
last_reviewed: 2026-11-24
---

# Pipeline stages

The default stages every business uses, unless its motion repo defines its own (the business's `motion.md` says which). A deal moves only when the exit rule is met. Stages count what buyers did, not what we hope.

| Stage | It's here when | It moves on when |
|---|---|---|
| 1. Target | On a play's list, with a dated, linked signal | The first message is sent |
| 2. Contacted | The first message was sent | They reply |
| Inbound | They came to us through a channel in `business.md` | Fit checked and a person replied: a good fit moves to Engaged; otherwise Nurture, Lost or routed elsewhere ([inbound](inbound.md)) |
| 3. Engaged | They replied positively, or asked a question | A meeting is held (not just booked) |
| 4. Discovery | A first meeting was held | The four discovery questions are answered: trigger, cost of doing nothing, who decides, what makes it safe ([discovery](discovery.md)) |
| 5. Qualified | A real problem, a decider in the conversation, and a timeframe | A proposal or price is sent |
| 6. Proposal | Proposal or price sent | They sign or pay, or say no |
| 7. Won | Signed or paid | Hand off to delivery |
| Lost | They said no, or went silent after the play's last follow-up | Record the reason |
| Nurture | "Not now", with a date to check back | The check-back date arrives |

## Rules
- **Every record has a source:** inbound (and the channel) or outbound (and the play). Conversion rates are reported by source, never blended.
- **Held, not booked.** A no-show stays in Engaged.
- **Paid or signed, not "verbal yes".** A verbal yes stays in Proposal.
- **Lost reasons are evidence.** Record them in the buyer's words where possible: price, timing, "already covered", no budget, no reply.
- **Stale deals:** anything with no activity for 21 days (or the play's own limit) gets flagged in the weekly review.

## The numbers that come from this
- Conversion between each pair of stages.
- Time from Contacted to Won.
- Average deal value.
- Win rate (Won divided by Won plus Lost, from Qualified on).

Each becomes a real rate only once at least 20 deals have passed through that stage. Until then, the [operating rhythm](../team/operating-rhythm.md) uses labeled assumptions.
