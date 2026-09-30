# 01 - Capture and Enrichment

Pipeline quality is decided at intake. Garbage in does not just waste SDR time; it corrupts scoring, routing, and attribution for months.

## Intake channels

| Channel | Characteristics | Watch out for |
|---------|----------------|---------------|
| Web forms (demo, contact, trial) | Highest intent; structured data | Over-long forms kill conversion; progressive profiling beats 12 fields |
| Chat / conversational | Real-time; high engagement | Needs instant routing or it is worse than a form |
| Events / webinars | Volume; mixed intent | Attendee vs. registrant matters; import hygiene |
| Content downloads | Nurture fuel, rarely sales-ready | Score lightly; do not route to SDRs on an ebook |
| List imports / ABM | Targeted; no behavioral signal | Verify before import; never skip dedupe |
| Product signup (PLS) | Strongest signal in PLG | Identity resolution: signup user vs. buyer account |

## Validation at the door

Before a lead record is created or updated:

1. **Email validity.** Syntax check plus mailbox verification on high-value forms. Role-based addresses (`info@`, `support@`) get flagged, not routed.
2. **Required minimums.** Name, work email, company. Everything else can be enriched.
3. **Bot and spam filtering.** CAPTCHA or equivalent on public forms; quarantine obvious junk.

## The enrichment waterfall

No single provider covers everything. A waterfall tries providers in order and stops at the first confident match.

```
Lead created (sparse)
  → Provider A (firmographics: size, industry, revenue)
  → Provider B (technographics, contacts)
  → Provider C (intent data, funding signals)
  → Normalized + stamped with enrichment date
```

Design rules:

- **Enrich before scoring and routing.** A lead routed on `Company = "asdf"` is a lead misrouted.
- **Stamp what you enriched and when.** Enrichment decays; re-enrich on recycle, not on every touch.
- **Waterfall, not parallel.** Parallel calls cost 3x for marginally better fill rates.
- **Cap spend per record.** Enrichment on a student with a gmail address is charity.

## Dedupe and survivorship

Run matching **before** insert (against leads, contacts, and accounts):

- Exact email match on person; domain match on company.
- Fuzzy match on company name for the long tail.

When a duplicate is found, survivorship rules decide field by field (newest verified email wins; never overwrite a human-entered phone with an enriched guess). Log merges; unmergeable edge cases go to a weekly human review queue.

## What good looks like

A lead arrives in the working queue with: verified work email, normalized company (matched to an account or a clean new company), employee count band, industry, source, and an enrichment timestamp. Anything less and your SDRs are doing data entry instead of selling.
