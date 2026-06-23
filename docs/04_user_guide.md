# User Guide

## Purpose

This guide explains how a user should interact with the RFP Appraisal Engine V3.

---

## Before Using the Assistant

Make sure you have:

1. The actual RFP/RFQ/bid document to evaluate
2. Any addenda or attachments
3. The knowledge base files uploaded or available
4. Any historical Go/No-Go examples available

---

## Recommended User Prompt

Use this prompt for a full review:

```text
Please review this RFP using Cloudpoint’s knowledge base and any prior Go/No-Go examples available.

Do not only summarize the RFP. Evaluate whether Cloudpoint should pursue, decline, or further review this opportunity.

Include a Go / Conditional Go / No-Go recommendation, scorecard, scope fit, red flags, hidden field-work review, geography review, subcontractor need detection, award criteria review, page-limit review, similar past RFP comparison, compliance matrix, and PDF-ready executive summary.
```

---

## What To Expect

The assistant should return:

1. Opportunity overview
2. Final recommendation
3. Scorecard
4. Scope fit review
5. Red-flag review
6. Hidden field-work review
7. Geography review
8. Subcontractor review
9. Award criteria review
10. Page-limit review
11. Similar past RFP comparison
12. Compliance matrix
13. PDF-ready summary
14. Final next steps

---

## If the Assistant Says the RFP Is Missing

That is correct behavior when only reference files are uploaded.

The assistant should not invent a recommendation without an actual RFP.

Upload or paste the active solicitation document and run the prompt again.

---

## How To Interpret Recommendations

### Go

The opportunity appears to be a strong fit and worth pursuing.

### Conditional Go

The opportunity may be worth pursuing, but some risks or missing information need review.

### No-Go

The opportunity likely does not fit the preferred business, technical, geographic, or risk profile.

---

## Human Review Still Required

The assistant supports decision-making. It does not replace leadership, legal, contract, finance, or technical review.
