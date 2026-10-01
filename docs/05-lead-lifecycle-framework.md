# 05 - Lead Lifecycle Framework

The canonical stage model for top-of-funnel. Adapt the names to your CRM, but keep the gates: every stage transition is a decision with criteria, an owner, and a timestamp.

## The stages

| Stage | Definition | Owner | Entered by |
|-------|-----------|-------|-----------|
| Inquiry | Someone raised a hand (form, chat, event, import) | Marketing Ops (automation) | System |
| MQL | Meets scoring threshold; worth human attention | Marketing | Scoring automation |
| SAL | SDR accepted the MQL into a working queue | SDR | SDR acceptance |
| SQL | Qualified per framework; real opportunity | SDR → AE | Conversion |
| Opportunity | Converted; account, contact(s), and deal created | AE | Conversion |

Between MQL and SAL sits the most important gate in the funnel: a human looked at this lead and decided it deserves effort. Measure acceptance rate; it is the quality score of your scoring model.

## Entry and exit criteria

**Inquiry → MQL:** Score meets threshold (see [02 - Lead Scoring](02-lead-scoring.md)). Enriched and deduped first. No exceptions for "hot" leads; hot leads score hot.

**MQL → SAL:** SDR accepts within SLA. Acceptance means: valid contact info, reachable, in ICP or worth an exception with a reason.

**SAL → SQL:** Qualification framework complete (BANT or MEDDPICC-lite). AE accepts within 24 hours.

**SQL → Opportunity:** Converted with account matched, contact roles assigned, next step dated.

## Dispositions (the honest exits)

Every SAL that does not become an SQL gets a disposition. No disposition, no recycle path.

| Disposition | Meaning | Recycle path |
|-------------|---------|--------------|
| Bad timing | Real need, wrong quarter | Nurture; re-score on engagement |
| No budget | Need confirmed, no funds | Nurture; watch for funding/intent signals |
| No authority | Wrong person, no path to power | Find the right contact; nurture the account |
| Bad fit | Outside ICP | Suppress; do not re-score |
| Bad data | Unreachable, fake info | Suppress after one verification attempt |
| Competitor | Chose someone else | Competitive nurture track; re-engage at renewal |

## Recycling rules

- Recycled leads keep their history. When they re-engage, they re-score with history intact.
- A lead recycled twice for the same reason is a process failure, not a lead failure. Review the entry criteria.
- Never delete disqualified leads. Deletion destroys the denominator your conversion math needs.

## Reporting

- Conversion at each gate, by source and by month.
- SAL acceptance rate (SDR trust in marketing).
- SQL acceptance rate (AE trust in SDR).
- Time in stage and stage age outliers.
- Disposition mix: if "bad timing" dominates, your threshold is too low; if "bad fit" dominates, your targeting is off.
