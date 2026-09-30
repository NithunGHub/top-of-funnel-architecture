# 02 - Lead Scoring

Scoring answers one question: which lead should a human touch next? Everything else is decoration.

## The three inputs

| Input | What it measures | Example signals |
|-------|-----------------|-----------------|
| Fit | Can they buy? | Employee count, industry, geography, tech stack, title seniority |
| Intent | Are they in a buying motion? | Third-party intent topics, funding news, hiring patterns, website visits to pricing |
| Engagement | Are they paying attention to us? | Email opens/clicks (weak), content depth, demo requests, trial activity (strong) |

Fit is stable and gates everything. Intent is spiky and time-sensitive. Engagement is abundant and mostly noise. Weight accordingly.

## Building the model (v1, no data science required)

1. **Define fit explicitly.** Ideal customer profile as rules: e.g., 200-5000 employees, SaaS or tech-enabled services, North America + EMEA. Score 0-50 on fit.
2. **Score intent 0-30.** Only from signals you trust. One strong intent signal beats five weak ones.
3. **Score engagement 0-20.** Weight depth over volume: pricing page visit > 10 email opens.
4. **Set thresholds with sales, not for them.** MQL at a score the SDR team agrees is worth a same-day touch. If they disagree, the threshold is wrong or the model is.
5. **Grade and score separately (BANT-style).** Grade = fit (A-D), Score = interest (1-100). An A-20 (perfect fit, no interest) goes to nurture; a C-85 (bad fit, hot) goes nowhere near a rep.

## Decay and recycling

- Scores decay. Engagement older than 90 days should barely count; intent older than 30 days is history.
- Recycled leads (disqualified, bad timing) re-enter nurture with their history intact. When they re-engage, they should re-score, not start over.

## What to avoid

- **Black-box scores nobody trusts.** If SDRs cannot explain why a lead is hot, they will ignore the score.
- **Scoring on vanity engagement.** Email opens are not buying signals.
- **Set-and-forget models.** Review quarterly: conversion of MQL to SQL by score band tells you if the model still works.
- **Negative scoring as punishment.** Use negative scores sparingly (competitor, student, existing customer); overuse makes the model unreadable.

## Graduating to predictive

Once you have 12+ months of clean outcome data (MQL → SQL → won/lost), a predictive model can outperform rules. Until then, explicit rules beat a model trained on messy history. Most companies should stay on rules longer than they think.
