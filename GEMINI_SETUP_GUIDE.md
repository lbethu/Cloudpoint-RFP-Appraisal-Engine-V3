# Gemini Gem Setup Guide

## Gem Name

Recommended name:

```text
Cloudpoint RFP Appraisal Engine V3
```

Alternative names:

```text
LG RFP GPT V3
Local Government RFP Review Assistant
Cloudpoint Go/No-Go RFP Assistant
RFP Appraisal Decision Engine
```

---

## Gem Short Description

Use this if Gemini asks for a short description:

```text
An internal RFP appraisal assistant that evaluates Local Government solicitations, detects risks, reviews scope fit, checks field-work and subcontractor requirements, builds compliance matrices, and creates PDF-ready Go/No-Go summaries.
```

---

## Gem Full Description

Use this as the main public/internal Gem description:

```text
Cloudpoint RFP Appraisal Engine V3 is an internal AI assistant designed to evaluate Local Government RFPs, RFQs, bids, and solicitation documents. It helps determine whether an opportunity should be pursued, declined, or further reviewed by checking scope fit, hidden field-work requirements, geography and drive-time concerns, subcontractor needs, insurance and liability risks, award criteria, page limits, compliance requirements, and historical Go/No-Go examples.

The assistant is designed to act as a structured RFP appraisal workflow, not a basic document summarizer. It separates knowledge base files from the actual RFP, avoids hallucinating when the solicitation is missing, and produces a decision-ready output with a scorecard, compliance matrix, and PDF-ready executive summary.
```

---

## What To Paste Into Gemini Instructions

Paste the full contents of:

```text
prompts/v3_master_instruction_prompt.md
```

into the Gemini Gem instruction area.

---

## What To Upload Into Gemini Knowledge

Upload knowledge base files in this order where possible:

1. Company context
2. Service catalogs
3. Decision rules
4. Geography and drive-time logic
5. Historical Go/No-Go examples
6. Output templates
7. Test cases

Recommended knowledge base organization:

```text
01_Company_Context
02_Service_Catalogs
03_Decision_Rules
04_Geography_Drive_Time
05_Historical_RFP_Examples
06_Output_Templates
07_Test_Cases
```

---

## Initial Test Prompt

After setup, run this first:

```text
Please review this RFP and provide a Go/No-Go recommendation for Cloudpoint.

In your review, identify red flags, hidden field-work requirements, onsite or travel concerns, insurance risks, subcontractor needs, geography risk, award criteria, page limits, and compliance requirements.

Also create a compliance matrix with requirement, owner, status, risk level, and notes. End with a PDF-ready executive summary.
```

If no actual RFP is uploaded, the assistant should say the RFP is missing and should not invent an appraisal.

---

## Full Appraisal Prompt

Use this once a real RFP is uploaded:

```text
Please review this RFP using Cloudpoint’s knowledge base and any prior Go/No-Go examples available.

Do not only summarize the RFP. Evaluate whether Cloudpoint should pursue, decline, or further review this opportunity.

Include:
1. Go / Conditional Go / No-Go recommendation
2. Scorecard with reasoning
3. Scope fit against Cloudpoint’s services
4. Hidden red flags, including field work, onsite work, GPS/data collection, asset inventory, inspection, surveying, drone, LiDAR, or civil engineering language
5. Geography and drive-time risk from Metamora, IL
6. Subcontractor need detection
7. Award criteria and scoring review
8. Page-limit and proposal strategy risk
9. Similar past RFP comparison
10. Compliance matrix with requirement, owner, status, risk level, and notes
11. PDF-ready executive summary

Important: If the actual RFP document is not provided, do not invent an appraisal. Clearly say that the RFP is missing, explain what reference files were found, and state what document is needed before completing the review.
```

---

## Recommended Maintenance Rule

Whenever the Gem instructions are updated, also update:

- `CHANGELOG.md`
- `docs/02_v3_instruction_logic.md`
- `examples/sample_test_cases.md`
- `tests/expected_behavior_matrix.md`

This keeps the product maintainable.
