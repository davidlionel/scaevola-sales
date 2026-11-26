# Sales team

[Owner's first name]'s sales team, set up with Scaevola Sales. Eight assistants that find buyers, start conversations, support deals and keep the pipeline honest, for every business [Owner's first name] points them at. They draft; a person decides and sends.

## How to use it
Open this repository in Claude Code (claude.ai/code), plus the Scaevola team repository if the team is bolted on, and start with "Follow CLAUDE.md." Then:
- **Set up a business:** "Strategist: set up a business for [name]." It interviews you and writes the business pack.
- **Run outreach:** "Sales manager: plan a play for [business]." The prospector builds the list, outreach drafts the messages, the reviewer checks, you send.
- **Answer inbound leads:** follow [playbooks/inbound-go-live.md](playbooks/inbound-go-live.md) once per business.
- **Get a strategy report:** "Strategist: write a growth report for [business]."
- **Tighten the lead score:** "Fit scorer: run the back-test for [business]."
- **When an assistant gets something wrong:** tell it in the chat. It drafts a lesson and saves it only on your yes.

## What's here
- [CLAUDE.md](CLAUDE.md): the rules every assistant follows, and the mode (on its own, or bolted on to Scaevola).
- [method/](method/README.md): your buyer lens, strategy, evidence rules and house rules. Replace the starters with your own.
- [team/](team/charter.md): who owns what, the weekly rhythm, the operating modes.
- [.claude/agents/](.claude/agents/sales-manager.md): the eight assistants.
- [playbooks/](playbooks/signals.md): signals, messaging, discovery, inbound, pipeline stages, fit scoring, growth reports, compliance.
- [team/calculations.md](team/calculations.md): exact methods for scoring, back-tests, deduping and tallies; Claude calculates with its own code tool, and no code ships in this kit.
- [businesses/](businesses/README.md): one pack per business you sell for.
- [index.md](index.md): every file, one line each.
