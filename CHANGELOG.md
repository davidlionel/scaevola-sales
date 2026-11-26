# Changelog

## 1.1.0 (2026-11-26)
No code, for your security.
- The scripts are gone. Every calculation (scoring, freshness, deduping, back-tests, tallies, forecasts, growth-report math) is now a written method in team/calculations.md, and Claude calculates with its own code tool. Nothing from this repository runs on your computer.
- Updates stop if a release ever contains anything but text and CSV files.
- Files that changed: README.md, PROMPT.md, sales/CLAUDE.md, sales/README.md, sales/index.md, sales/method/README.md, sales/method/evidence.md, sales/team/calculations.md (new), sales/team/operating-modes.md, sales/team/operating-rhythm.md, sales/playbooks/fit-scoring.md, sales/playbooks/growth-report.md, sales/playbooks/inbound-go-live.md, sales/.claude/agents/prospector.md, sales/.claude/agents/fit-scorer.md, sales/.claude/agents/pipeline.md, and the business templates (README.md, scoring.md, pipeline.md, plays/_play-template/list.md). sales/scripts/ is removed.

## 1.0.0 (2026-11-26)
First release. Built with Scaevola, and released early on purpose: it improves in the open, with every release. Share what you made in Discussions.
- Eight assistants: sales manager, strategist, prospector, fit scorer, outreach, deal support, pipeline and reviewer.
- Your own method: buyer lens, strategy, evidence rules and house rules, with starters to replace.
- Runs on its own or bolted on to Scaevola 1.0.0 or later, reporting to the CRO seat.
- Outbound plays from public signals, and inbound lead handling with a go-live checklist.
- Fit and timing scores, back-tested against your own wins and losses once 20 deals have closed and improved one proven change at a time.
- Growth reports: market context, three problems and a strategy for each.
- Scripts for scoring, back-tests, deduping, freshness, tallies and report math.
