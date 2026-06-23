# Project Overview

## Project Name

**Cloudpoint RFP Appraisal Engine V3**

This project may also be referenced as:

- LG RFP GPT V3
- Local Government RFP Review Assistant
- Cloudpoint Go/No-Go Assistant
- RFP Appraisal Decision Engine

Recommended name for documentation and GitHub:

```text
Cloudpoint RFP Appraisal Engine V3
```

---

## Objective

The objective of this project is to create a structured AI assistant that reviews Local Government RFPs, RFQs, bids, and solicitation documents and helps determine whether Cloudpoint should pursue, decline, or further review an opportunity.

The assistant should support faster and more consistent RFP review by identifying:

- scope fit
- hidden risks
- geography concerns
- field-work obligations
- subcontractor needs
- award criteria
- page limits
- compliance requirements
- historical Go/No-Go similarities
- final recommended action

---

## Problem Statement

Public-sector RFPs are often lengthy, inconsistent, and difficult to review quickly. Critical requirements may be spread across multiple sections, attachments, addenda, legal terms, and proposal instructions.

A general AI assistant may summarize the document but miss decision-critical issues such as:

- hidden field-work language
- mandatory onsite work
- GPS or asset inventory requirements
- survey, drone, LiDAR, or civil engineering needs
- strict insurance or indemnification language
- bonding requirements
- cybersecurity or CJIS requirements
- page limits
- unclear award criteria
- low deal value
- out-of-region travel burden
- required forms and compliance items

V3 is designed to solve this by forcing a repeatable appraisal workflow.

---

## Main Design Principle

The assistant should not behave like a normal document summarizer.

It should behave like an internal RFP appraisal analyst.

The assistant should always move through this chain:

```text
Document Classification → Risk Detection → Scope Fit → Compliance → Score → Recommendation → Next Steps
```

---

## Target Users

This system is designed for:

- proposal reviewers
- leadership reviewers
- GIS technical leads
- project managers
- business development staff
- internal AI/GIS support staff
- anyone responsible for deciding whether an RFP is worth pursuing

---

## Target Documents

The assistant is designed to review:

- RFPs
- RFQs
- bid solicitations
- local government procurement documents
- GIS services RFPs
- managed GIS RFPs
- ArcGIS implementation RFPs
- Utility Network RFPs
- Parcel Fabric RFPs
- Indoor GIS RFPs
- asset management RFPs
- data collection RFPs
- public works GIS support RFPs

---

## V3 Operating Flow

```text
Uploaded Files
    ↓
Document Classification
    ↓
Missing RFP Check
    ↓
Opportunity Intake
    ↓
Scope Fit Review
    ↓
Red-Flag Detection
    ↓
Hidden Field-Work Detection
    ↓
Geography / Drive-Time Review
    ↓
Subcontractor Need Review
    ↓
Award Criteria Review
    ↓
Page-Limit Review
    ↓
Historical RFP Comparison
    ↓
Scorecard
    ↓
Compliance Matrix
    ↓
PDF-Ready Executive Summary
```

---

## Success Criteria

The system is successful if it can:

- identify when an actual RFP is missing
- separate knowledge base files from the active RFP
- avoid hallucinating missing opportunity details
- detect hidden field-work language
- detect subcontractor needs
- review award criteria
- review page limits
- generate a practical compliance matrix
- compare against historical Go/No-Go examples
- produce a clear Go / Conditional Go / No-Go recommendation
- create a PDF-ready final report

---

## Product Positioning

Suggested positioning statement:

```text
Cloudpoint RFP Appraisal Engine V3 helps transform RFP review from manual document reading into a structured, repeatable, and decision-ready appraisal workflow.
```
