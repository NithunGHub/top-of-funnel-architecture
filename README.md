# Top-of-Funnel Architecture

How pipeline starts: capturing demand, enriching it, scoring it, routing it to the right human fast, and running the SDR motion that turns interest into qualified opportunities.

This repo covers the top of the funnel as a system: the mechanics of lead capture, the data work that makes leads routable, the scoring models that prioritize them, and the operating playbook for the team that works them.

## Who this is for

- Marketing Ops and SDR leaders building or fixing inbound flow
- Salesforce admins implementing assignment, scoring, and queues
- Founders who suspect leads are dying quietly in a queue somewhere (they are)

## Contents

| Doc | What it covers |
|-----|---------------|
| [01 - Capture and Enrichment](docs/01-capture-and-enrichment.md) | Intake channels, validation, and the enrichment waterfall |
| [02 - Lead Scoring](docs/02-lead-scoring.md) | Fit, intent, and engagement scoring; thresholds; decay |
| [03 - Routing and Assignment](docs/03-routing-and-assignment.md) | Territory, round-robin, and account-based routing; SLAs; fallbacks |
| [04 - SDR Playbook](docs/04-sdr-playbook.md) | Working cadence, sequences, qualification, and the AE handoff |
| [05 - Lead Lifecycle Framework](docs/05-lead-lifecycle-framework.md) | The canonical stage model: gates, dispositions, and recycling rules |
| [06 - Funnel Math](docs/06-funnel-math.md) | Sizing top-of-funnel from a revenue target, with a worked example |

### Templates

| Template | Purpose |
|----------|---------|
| [Response SLA Matrix Template](templates/sla-matrix-template.md) | First-touch SLAs by lead type, with escalation rules |

## The core loop

```
Capture → Validate → Enrich → Dedupe → Score → Route → Work fast → Qualify → Convert
```

Every stage has an owner, a metric, and a failure mode documented in this repo. The most expensive failure in top-of-funnel is not bad leads; it is good leads worked too slowly or routed to nobody.
