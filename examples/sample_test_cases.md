# Sample Test Cases

## Purpose

These test cases compare V2 and V3 behavior.

V3 should behave like a structured RFP appraisal engine, not a basic summarizer.

---

## Test Case 1 — Missing RFP Detection

### Prompt

```text
Please review this RFP and provide a Go/No-Go recommendation for Cloudpoint.

In your review, identify red flags, field-work requirements, onsite concerns, insurance risks, subcontractor needs, geography risk, award criteria, page limits, and compliance requirements.

Also create a compliance matrix and end with a PDF-ready executive summary.
```

### Setup

Only upload Cloudpoint knowledge base documents. Do not upload an actual RFP.

### Expected V3 Behavior

The assistant should not invent an appraisal.

It should say:

```text
I found reference knowledge base files, but I do not see the actual RFP/RFQ/bid document to evaluate.
```

### Failure Behavior

The assistant fails if it:

- creates a fake recommendation
- treats service catalog files as the active RFP
- invents project details
- gives a Go/No-Go decision without an RFP

---

## Test Case 2 — Knowledge Base Classification

### Prompt

```text
Before reviewing the opportunity, classify the uploaded files and tell me which files are company reference materials, which are historical examples, and which file is the current RFP to evaluate.
```

### Expected V3 Behavior

The assistant should classify files as:

- current RFP/RFQ/bid document
- company knowledge base
- service catalog
- historical Go/No-Go example
- decision rule or template
- unknown

If no active RFP exists, it should clearly say that.

---

## Test Case 3 — Hidden Field-Work Detection

### Prompt

```text
Review this RFP and specifically identify whether it includes hidden field-work requirements. Do not only search for the word “onsite.” Look for language such as data collection, GPS collection, field verification, site visits, inspections, asset inventory, surveying, drone work, LiDAR collection, or civil engineering.
```

### Expected V3 Behavior

The assistant should identify hidden field-work terms and classify the level as:

```text
No Field Work Detected
Light Field Work
Moderate Field Work
Heavy Field Work
Subcontractor Likely Required
```

---

## Test Case 4 — Subcontractor Need Detection

### Prompt

```text
Evaluate whether this RFP may require a subcontractor. Check for surveying, drone/UAS, LiDAR collection, civil engineering, heavy field data collection, utility locating, or physical inspection work. Do not invent subcontractor names. Only recommend the type of partner needed.
```

### Expected V3 Behavior

The assistant should return:

```text
Subcontractor Need: Yes / No / Possible / Unknown

Reason:
[Reasoning]

Recommended Partner Type:
[Partner type only]
```

---

## Test Case 5 — Award Criteria Review

### Prompt

```text
Find the award criteria, scoring weights, selection criteria, basis of award, interview requirements, price weighting, technical scoring, and experience scoring in this RFP. Explain how the evaluation method affects Cloudpoint’s chance of success.
```

### Expected V3 Behavior

The assistant should find and summarize award criteria if present.

If missing, it should say:

```text
Award criteria were not found in the provided RFP.
```

---

## Test Case 6 — Page-Limit Review

### Prompt

```text
Review this RFP for page limits, formatting rules, attachment limits, resume limits, cover letter limits, required forms, and file upload restrictions. Explain whether the page limit creates proposal strategy risk.
```

---

## Test Case 7 — Geography and Drive-Time Risk

### Prompt

```text
Evaluate the geography and drive-time risk for this RFP using Cloudpoint’s priority state logic and distance from Metamora, Illinois. Explain whether the project location creates travel, onsite, or delivery risk.
```

---

## Test Case 8 — Historical Go/No-Go Comparison

### Prompt

```text
Evaluate this RFP using Cloudpoint’s knowledge base and any prior Go, No-Go, Won, or Lost examples available.

Compare this opportunity against the most similar past examples. Explain why they are similar, what decision was made before, what is different now, and what lesson applies to the current opportunity.

Do not automatically copy the past decision.
```

---

## Test Case 9 — Compliance Matrix Generation

### Prompt

```text
Create a compliance matrix for this RFP with requirement, owner, status, risk level, and notes. Include deadlines, submission method, page limits, required forms, insurance requirements, bonding requirements, technical response items, pricing, references, field work, subcontractor needs, and award criteria.
```

---

## Test Case 10 — Full Appraisal Test

### Prompt

```text
Please review this RFP using Cloudpoint’s knowledge base and any prior Go/No-Go examples available.

Do not only summarize the RFP. Evaluate whether Cloudpoint should pursue, decline, or further review this opportunity.

In your review, include:

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

Important:
If the actual RFP document is not provided, do not invent an appraisal. Clearly say that the RFP is missing, explain what reference files were found, and state what document is needed before completing the review.
```
