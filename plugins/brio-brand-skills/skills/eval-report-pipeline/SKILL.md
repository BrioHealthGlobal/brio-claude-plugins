---
name: eval-report-pipeline
description: >
  This skill should be used for a full monitoring & evaluation (M&E)
  reporting pipeline — intake, data audit, structure confirmation, full
  report draft, limitations review, and stakeholder-ready output. Covers
  program evaluations, 360-degree feedback summaries, pre/post
  assessments, and other M&E deliverables. Trigger on requests like "draft
  the program evaluation report" or "turn this survey data into an eval
  report".
metadata:
  version: "1.0"
  argument-hint: "[program name or eval type] + [data source]"
---

# M&E Content Pipeline

Full evaluation pipeline: intake → data audit → structure confirmation →
full report draft → limitations review → stakeholder-ready output.

## Ground rules
Always surface data limitations explicitly — never bury caveats.
Distinguish clearly between measured findings and inferred conclusions.
Do not overstate statistical significance. Flag missing data as a gap,
not something to fill with assumptions.

## Process

### Stage 1 — Intake
Ask the user, all at once, numbered:
1. What program or initiative is being evaluated?
2. Who is the primary audience? (board / funders / program staff /
   external stakeholders)
3. What data do you have? (paste it, describe it, or give a file path)
4. What is the core evaluation question this report must answer?
5. Any constraints — page limit, required sections, funder template?

Wait for the full response before continuing.

### Stage 2 — Data audit
Review the provided data and assess:
- What is present and usable
- What is missing or ambiguous
- Sample size and statistical power limitations
- Instrument-specific notes if relevant (e.g. IWPQ subscales, OCB-C rater
  source, CATME self vs. peer ratings, Qualtrics export completeness)

Output a data audit (5–8 bullets) and ask: "Does this look right before I
structure the report?" Wait for confirmation.

### Stage 3 — Confirm structure
Propose a report outline based on audience and evaluation question.
Default structure:
  1. Executive Summary (findings + recommendations only, max 1 page)
  2. Program Overview
  3. Evaluation Methodology
  4. Findings (organized by evaluation question)
  5. Implications & Recommendations
  6. Limitations
  7. Appendix (instruments, raw tables if applicable)

Ask: "Does this structure work or do you want to adjust?" Wait for
explicit confirmation before drafting.

### Stage 4 — Draft report
Apply these conventions throughout:
- Executive Summary: conclusions first, no methodology detail
- Each findings section: conclusion first, then supporting evidence
- Tables for any comparison with 3+ items
- Plain language: define all technical terms on first use
- Do not overstate statistical significance
- Do not bury caveats — surface them in the section they affect, then
  consolidate in Limitations

### Stage 5 — Limitations and gap review
Write a Limitations section that explicitly covers:
- Data gaps that affected any finding
- Any conclusion inferred rather than directly measured
- Sample size or representativeness concerns
- Recommendations for follow-up data collection

This section is mandatory — do not omit even if data is strong.

### Stage 6 — Flagged assumptions
After the report, list numbered assumptions made during drafting:
  1. [assumption] — please confirm or provide actual data
Be specific — "I assumed the pre/post interval was 6 weeks based on
program description" not "some assumptions were made."

### Stage 7 — Save
Ask the user where to save the final report.
