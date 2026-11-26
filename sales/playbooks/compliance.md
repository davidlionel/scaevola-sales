---
type: playbook
status: reference
owner: [owner]
last_reviewed: 2026-11-24
review_after: 2027-05-24
---

# Compliance and deliverability

The rules a message must meet before a person sends it. This is a working checklist, not legal advice. Laws and inbox rules change: recheck the sources after `review_after`, and when a business sells into a new country, check that country's rules before the first send.

## United States: CAN-SPAM (strong; FTC guidance)
Source: [FTC CAN-SPAM compliance guide](https://www.ftc.gov/business-guidance/resources/can-spam-act-compliance-guide-business).
- It covers any email whose main purpose is promoting a product or service. There is no exception for business-to-business email.
- Accurate "From", "To", "Reply-To" and routing details that identify the sender.
- No misleading subject lines.
- Make clear the message is promotional (the law leaves room in how).
- A valid physical postal address in every message.
- A clear way to opt out, honored within 10 business days, and never sold or passed on.
- The business is responsible for what anyone sends on its behalf, including this team's drafts once a person sends them.

## United Kingdom: PECR and UK GDPR (strong; ICO guidance)
Source: [ICO business-to-business marketing](https://ico.org.uk/for-organisations/direct-marketing-and-privacy-and-electronic-communications/business-to-business-marketing/).
- Limited companies, LLPs and other corporate bodies can get B2B marketing emails without prior consent under PECR.
- Sole traders and most ordinary partnerships are treated like individuals: email them only with consent (or the narrow "soft opt-in" for past customers).
- UK GDPR still applies to the personal data used. The usual basis is legitimate interests: the message must be relevant to the person's role, and they must be able to object easily.
- Always identify the sender and give a simple opt-out. Keep a suppression list and check new lists against it.

## European Union (moderate; varies by country)
GDPR applies everywhere in the EU, but national e-marketing rules differ, and some countries require consent even for B2B email. Check the country's rules before the first send. If unsure, don't send cold email there; flag it to the decider.

## Canada: CASL (moderate)
Commercial email needs consent. Implied consent can apply when a business address is publicly published, the message relates to the person's role, and there's no statement saying they don't want messages. Every message identifies the sender, gives contact details and an unsubscribe. Check the business's case before sending.

## Inbox rules: Gmail and other large providers (strong; Google guidance)
Source: [Google email sender guidelines](https://support.google.com/a/answer/81126).
- **Every sender:** SPF or DKIM on the sending domain, valid DNS, a secure (TLS) connection, and a user-reported spam rate kept under 0.3%.
- **Bulk senders** (more than 5,000 messages a day to Gmail): SPF, DKIM and DMARC, a "From" domain aligned with them, one-click unsubscribe on marketing messages, and unsubscribes honored within 48 hours.
- **Practice (moderate):** send cold outreach in small daily volumes from real, warmed-up mailboxes, often on a separate domain so the main domain's reputation is protected. Stop a play if bounces or spam complaints climb.

## LinkedIn and other platforms (strong)
LinkedIn's User Agreement bans scraping and automated activity (bots, auto-connect, auto-message tools). LinkedIn actions are manual, by a person, from their own account. Apply the same rule to any platform whose terms forbid automation.

## Before any send (the reviewer's checklist)
1. The buyer's country and type (company or individual) are known, and the rule above allows the message.
2. Sender identity, a physical address (for US commercial email) and a simple opt-out are present.
3. The subject line matches the message.
4. Every row passed the suppression list and the overlap check.
5. The sending domain is authenticated and the volume is within the business's limits in `business.md`.
