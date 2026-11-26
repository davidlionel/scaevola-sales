---
type: playbook
status: draft
owner: [owner]
last_reviewed: 2026-11-26
---

# Inbound

How the core team handles leads that come to the business: a form fill, a demo or contact request, a reply to content, a chat message, a sign-up, a referral introduction. Outbound starts with a public signal the team finds; inbound starts with an action the buyer took. Every motion uses both directions; a motion repo says how much of each to run and what good looks like.

## The inbound path

| Step | Who | Output | Gate |
|---|---|---|---|
| 1. Acknowledge | The business's own tools (for example a HubSpot workflow) | An instant reply from a template the decider approved once | Template approved and switched on by a person; agents never send |
| 2. Research | Prospector | Who they are, what they did, and their company, enriched from approved tools | None |
| 3. Score and route | Prospector, with the current model in `scoring.md` and the routing rules in `business.md` | Fit and timing scores and band ([fit-scoring.md](fit-scoring.md)); good fit, not a fit, existing customer or partner, or spam | None |
| 4. Reply draft | Outreach | A personal reply that answers what they asked, with one next step | A person sends |
| 5. Call prep | Deal support | The one-page prep from [discovery.md](discovery.md) | A person runs the call |
| 6. Record | Pipeline | The lead in the CRM or `pipeline.md`, with its source and response time | None |

The reviewer checks the acknowledgment template and the reply style once per business, then spot-checks five inbound replies a week rather than every one, so speed isn't lost.

## Speed
Inbound leads cool quickly, but agents only work when a person starts them or a schedule runs. So:
- **The acknowledgment is instant** and comes from the business's own automation, set up and approved by a person.
- **The personal reply follows within the business's response target** (set in `business.md`, for example within one business hour). A scheduled task runs steps 2 to 4 on new leads at that cadence; a person reviews and sends.
- **Response time is measured** from the lead's action to the personal reply a person sent.
- **Switching it on:** the checklist and the scheduled task prompt are in [inbound-go-live.md](inbound-go-live.md).

## Routing
Set per business in `business.md`. The default:

| The lead is | Goes to |
|---|---|
| A good fit for `icp.md` | Reply offering a call; deal support preps it |
| Not a fit now | A polite reply that answers their question; nurture if they agreed to hear more |
| An existing customer | Whoever runs that relationship, not a sales reply |
| A partner, job seeker, vendor or press | The person named for it in `business.md` |
| Spam or a bot | Logged, no reply |

## Writing the reply
- **Answer what they asked first,** in the first line. Their action is the trigger; name it ("Thanks for asking about pricing for teams of 20").
- **One next step,** easy to say yes to: a time for a call, or the one thing they need.
- **No pitch they didn't ask for.** They came to you; earn the next step by being useful.
- **The lens still applies:** what they asked for is the stated motive; the call is where the real one comes out ([discovery.md](discovery.md)).
- Plain words, the business's voice, no em dashes ([messaging.md](messaging.md)).

## Records and numbers
- **Every pipeline record carries its source:** inbound (and the channel) or outbound (and the play). Without it, the growth report's source mix and conversion rates are wrong.
- **Inbound enters the pipeline at its own stage** ([pipeline-stages.md](pipeline-stages.md)).
- **Inbound plays** test a change to an inbound channel or offer (a new form, a new lead magnet, a new reply). Their counts: leads, response time, lead to meeting held, meeting to qualified, won.

## Compliance
Replying to what someone asked for is expected. Adding them to marketing emails is a separate step that needs its own basis under [compliance.md](compliance.md) (consent, or a lawful B2B basis where that applies), and an easy opt-out.
