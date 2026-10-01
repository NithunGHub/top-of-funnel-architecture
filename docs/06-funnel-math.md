# 06 - Funnel Math

How to size the top of funnel from a revenue target. Every GTM plan is this arithmetic; the only question is whether you did it before or after committing to the number.

## The chain

```
Revenue target → Deals needed → Opportunities needed → SQLs needed → MQLs needed → Inquiries needed
```

Each arrow divides by the conversion rate of that gate. Work backwards from revenue.

## Worked example

Assumptions (replace with your own trailing 12-month actuals):

| Input | Value |
|-------|-------|
| New ARR target | $10,000,000 |
| Average ACV | $50,000 |
| Win rate (opportunity → closed won) | 20% |
| SQL → opportunity | 60% |
| SAL → SQL | 40% |
| MQL → SAL (acceptance) | 70% |
| Inquiry → MQL | 15% |

Math:

- Deals needed: 10,000,000 / 50,000 = **200 deals**
- Opportunities needed: 200 / 0.20 = **1,000 opportunities**
- SQLs needed: 1,000 / 0.60 = **1,667 SQLs**
- SALs needed: 1,667 / 0.40 = **4,167 SALs**
- MQLs needed: 4,167 / 0.70 = **5,953 MQLs**
- Inquiries needed: 5,953 / 0.15 = **39,687 inquiries**

Per month (÷ 12): ~3,307 inquiries → ~496 MQLs → ~347 SALs → ~139 SQLs → ~83 opportunities → ~17 deals.

## Using it

1. **Plan capacity.** 347 SALs per month across how many SDRs? At ~100 SALs per SDR per month, that is 3.5 SDRs. Hire or lower the target.
2. **Find the constraint.** Which gate has the worst conversion vs. benchmark? Fix that gate before buying more top-of-funnel.
3. **Sanity-check the target.** If the inquiry volume needed is 5x your best month ever, the plan needs a new channel, not optimism.
4. **Recompute quarterly.** Conversion rates drift as segments and channels change.

## Benchmarks (directional, B2B SaaS)

| Gate | Weak | Healthy | Strong |
|------|------|---------|--------|
| Inquiry → MQL | < 8% | 12-20% | > 25% |
| MQL → SAL | < 50% | 65-80% | > 85% |
| SAL → SQL | < 25% | 35-50% | > 55% |
| SQL → Opportunity | < 50% | 60-75% | > 80% |
| Win rate | < 15% | 20-30% | > 35% |

Benchmarks are for orientation. Your trailing actuals are the plan input; industry averages are not.

## Sensitivity

Small moves at high-leverage gates beat big moves at the top. In the example, improving SAL → SQL from 40% to 50% removes ~830 SALs of required volume. Improving inquiry → MQL by the same relative amount removes far less. Always fix the lowest gate first.
