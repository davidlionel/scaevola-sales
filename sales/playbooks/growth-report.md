---
type: playbook
status: draft
owner: [owner]
last_reviewed: 2026-11-24
---

# Growth report

How the team writes a strategy report for a business. A growth report is a strategy: the top problems the business faces in its market right now, and what to do about each. Numbers and measurement are the evidence behind it, never the substance of it. A report can stand alone (a business that only wants strategy, such as an employer) or open a business that goes on to run plays. The template is in [businesses/_template/reports/](../businesses/_template/reports/README.md).

## The shape every report takes

1. **Summary** (one page): the answer in one sentence, the three problems, the three strategies, what to stop, the one decision needed.
2. **The context:** what's happening in this business's market now, and how buyers and competitors feel about it.
3. **The top problems:** three, more only if absolutely necessary. Each is a problem the business faces in this context, stated plainly, with its evidence.
4. **The strategies:** one per problem. Each is a real choice that changes where the business plays, how it wins, what it sells or how it gets paid, not a measurement or a process fix.
5. **Sequence:** what to do first, ranked by speed to money.
6. **The numbers behind the problems**, **the buyer** (Lens read), **risks and the case against**, **evidence and gaps**, and **the math**.

## Who does what

| Step | Who | Output |
|---|---|---|
| 1. Scope and data request | Strategist | The question, the decider, and the data request below |
| 2. Context | Strategist, with web research | What is changing in the market now, with sources |
| 3. The numbers | Pipeline | Predictability and profitability, with the math shown |
| 4. The buyer | Strategist | The Lens read on the best and worst customers |
| 4b. Motion scorecard | The motion repo's specialists, at the business's motion step | The business scored against the motion's best practice ([contract](../team/motion-contract.md)). Until a motion repo exists, the strategist scores against the motion-fit signs below |
| 5. Problems and strategies | Strategist, with the sales manager and the motion repo's specialists | Three problems, a strategy for each, the sequence |
| 6. Review | Reviewer (and the motion repo's reviewer) | Verdict and the strongest case against |
| 7. Delivery | Strategist | The final report. A person presents it |

## 1. Scope
Write one sentence: the question the decider wants answered. Agree on the period the data covers (24 months if it exists) and any confidentiality terms before data arrives.

## Data request
Ask for what exists; never let a missing item stop the report. Mark each item received, partial or missing, and say in the report what the gaps limit.

1. **Revenue by month** for the period, split by client and by service or product.
2. **Client list** with start date, end date (if gone), and why they left, if known.
3. **Delivery cost** per client or service (time and direct costs).
4. **Where each client came from:** referral, existing client, marketing, outbound, partner, product sign-up, unknown.
5. **Pipeline and win or loss records:** deals, stages, values, dates, reasons.
6. **Pricing:** price list, discounts, how proposals are priced (hours, output, outcome).
7. **Sales and marketing spend and time,** by channel if possible.
8. **Capacity:** who sells, who delivers, and how full they are.
9. **Buyer evidence:** call notes, reviews, emails, and three to five short interviews with good clients and one or two who left.

**Confidential data:** if the decider can't share named data, ask for it anonymized or as totals. Record the terms in `business.md`. Data from one business never leaves its folder.

## 2. Context
Research what is changing in the business's market right now: demand, technology, competitors, pricing models, and how buyers and sellers feel (are they growing, hurting, scared?). Use current sources, cite each one, and rate each claim. Look for the evidence against the picture too. The context is what makes a problem a problem now.

## 3. The numbers
Each measure with its formula and period. Fewer than 12 months, or fewer than 20 records, is a small sample: say so. Put the revenue data in `reports/data/revenue.csv` and calculate the standard measures as [team/calculations.md](../team/calculations.md#growth-report-math) says, with a code tool; for anything it doesn't cover, write the formula into the report next to the number.

**Predictability**
- **Recurring share:** revenue under ongoing contracts or subscriptions, divided by total revenue.
- **Month-to-month swing:** standard deviation of monthly revenue divided by its average.
- **Concentration:** share of revenue from the top client and the top five.
- **Source mix:** share of new clients by source.
- **Win conversion:** how much of the revenue announced or booked from wins actually shows up as revenue, by the quarter won.
- **Pipeline coverage:** open qualified pipeline divided by the target for the period (the "three times" rule is a rule of thumb, not evidence).
- **Forecast accuracy:** past forecasts against what happened.

**Profitability**
- **Gross margin** by client, service and source.
- **Margin against volatility,** by line: the most profitable line is often the least predictable.
- **Retention** after 12 months, and **net revenue retention.**
- **Cost to win a client,** by source.
- **Price leakage:** discounts and unbilled work.

## 4. The buyer
A full Lens read ([charter](../team/charter.md)) on the best clients and on those who left. Interviews follow [discovery.md](discovery.md). Every finding ends in "because ..., we will ...", and the strategies must use them.

## Motion-fit signs (until each motion repo exists)
First, what the business actually runs, judged by where its clients come from, not what it says it runs. Then a first read of fit. These are practical signs (moderate), not rules; a motion repo's scorecard replaces them.

| Motion | Tends to fit when |
|---|---|
| Product-led | Buyers can try the product and get value alone, quickly; price is low enough to buy without a meeting |
| Marketing-led | Many buyers research before talking to anyone; the business can be found and trusted for a clear problem |
| Sales-led | Deals are large or complex, several people decide, and buyers expect to be guided |
| Customer-led | Clients stay, grow and refer; results are visible and easy to vouch for |

## 5. Problems and strategies
**Problems.** Pick the three that most limit predictable, profitable revenue in this context. For each: the problem in one plain sentence, the evidence (the business's numbers plus the market context), and its strength. A symptom (a missed forecast) is not a problem; find what causes it.

**Strategies.** One per problem. Each one says:
- **What:** the choice, specific enough to act on.
- **Cascade:** which choice it changes (where to play, how to win, capabilities, management systems).
- **Why it fits:** the evidence, including what competitors and buyers are doing.
- **Lens read:** "because ..., we will ..." lines that shape the offer, message or price.
- **What would have to be true,** and which of those is least tested.
- **Cheap test,** with confirm and kill counts.

**Pricing principle.** When a strategy changes how the business gets paid:
- **Price against the buyer's cost of the alternative:** doing it themselves, hiring, or building in-house, shown item by item, so the saving is visible without trusting a promise.
- **Use outcome pay only where the outcome is narrow, measurable and mostly controlled by the seller** (per hire, per meeting held, per finished asset). Never ask the buyer to bet on results the seller doesn't control, or ask them to carry a bet the seller won't share.
- **Package judgment as a system the buyer owns and runs.** Depending on someone else's judgment wounds the ego, so the buyer keeps the control and the credit.
- **Check the risk:** an itemized build-it-yourself cost can become the buyer's plan to do exactly that. It holds only where the seller's cost advantage is real.

Measurement fixes (track this, report that) support a strategy; they never stand in for one. The motion scorecard is a main input: a low score on a best practice is often the cause behind a problem, and the motion's usual fixes are candidate strategies. Then rank the strategies by speed to money into a sequence, and say what to stop doing.

## 6. Review and delivery
The reviewer reads the whole report before the decider sees it, and checks first that each strategy is a real strategic choice. The strategist pastes the verdict and the strongest case against into the report, unedited. The report ends with the one decision the decider needs to make.

## Rules
- **Facts are sacred.** Every number traces to the data request or a cited source. Gaps say "unknown".
- **Show the math** in an appendix.
- **Plain words,** no em dashes. The summary fits on one page.
- **No strategy without a test.** A move nobody can check is an opinion.
