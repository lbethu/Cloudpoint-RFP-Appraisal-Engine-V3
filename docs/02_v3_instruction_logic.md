# V3 Instruction Logic

## Purpose

This file explains the logic behind the V3 assistant instructions.

The master prompt lives in:

```text
prompts/v3_master_instruction_prompt.md
```

This document explains why the instruction modules exist and how each module should behave.

---

## 1. Document Classification Logic

Before reviewing anything, the assistant must classify the available documents.

This prevents the assistant from confusing company reference materials with the active RFP.

Document types:

1. Current RFP/RFQ/bid document to evaluate
2. Company context knowledge base
3. Service catalog or capability reference
4. Historical Go/No-Go/Won/Lost example
5. Decision rule or template document
6. Unknown file

### Required Behavior

If no current RFP is provided, the assistant must not create a fake appraisal.

Correct behavior:

```text
I found reference knowledge base files, but I do not see the actual RFP/RFQ/bid document to evaluate. Please upload or paste the solicitation document before I generate a final Go/No-Go appraisal.
```

---

## 2. Opportunity Intake Logic

The assistant extracts core opportunity metadata.

Required fields:

- client / agency name
- project title
- location
- state
- due date
- submission method
- question deadline
- pre-bid meeting date
- procurement type
- contract type
- project value, if available
- page limit
- required forms
- key deliverables
- insurance requirements
- bonding requirements
- security requirements

If a detail is not found, the assistant should mark it as missing rather than guessing.

---

## 3. Scope Fit Logic

The assistant compares the RFP scope against Cloudpoint capabilities.

Relevant service areas:

- Local Government GIS
- Managed GIS
- ArcGIS Online
- ArcGIS Enterprise
- ArcGIS Pro support
- Utility Network
- Parcel Fabric
- Indoor GIS
- Asset Management
- Data Collection
- GIS database design
- data migration
- web maps
- dashboards
- Field Maps configuration
- QA/QC
- geospatial consulting
- GIS implementation
- documentation and training

Scope fit categories:

```text
Strong Fit
Moderate Fit
Weak Fit
Not Enough Information
```

---

## 4. Red-Flag Detection Logic

The assistant must search for obvious and hidden risks.

Risk categories:

- liability
- indemnification
- insurance
- bonding
- cybersecurity
- CJIS/security requirements
- background checks
- low deal value
- aggressive deadline
- heavy onsite staffing
- unclear deliverables
- unfavorable payment terms
- strict penalties
- mandatory local presence
- broad responsibility language
- required certifications not likely available

Each red flag should include:

```text
Risk:
Evidence:
Risk Level:
Why It Matters:
Recommended Action:
```

Risk levels:

```text
Low
Medium
High
Critical
```

---

## 5. Hidden Field-Work Detection Logic

This is one of the most important V3 improvements.

The assistant must not only search for the word “onsite.”

It must search for hidden field-work language, including:

- data collection
- GPS collection
- field verification
- field investigation
- site visit
- site inspection
- asset inventory
- condition assessment
- inspection
- surveying
- survey control
- drone
- UAS
- LiDAR
- mobile mapping
- photogrammetry
- ground control
- field crew
- as-built verification
- right-of-way review
- measurements
- door-to-door collection
- utility locating
- in-person workshops
- stakeholder meetings

Field-work categories:

```text
No Field Work Detected
Light Field Work
Moderate Field Work
Heavy Field Work
Subcontractor Likely Required
```

---

## 6. Geography and Drive-Time Logic

The assistant should evaluate the opportunity location based on:

- state
- city
- distance from Metamora, Illinois
- priority state logic
- onsite work requirements
- recurring meeting requirements
- field-work requirements
- local presence requirements

Geography risk categories:

```text
Low
Medium
High
Unknown
```

Important logic:

A technically strong opportunity may still become risky if geography, travel, or onsite delivery requirements create too much burden.

---

## 7. Subcontractor Need Logic

The assistant should detect whether a partner may be needed.

Trigger areas:

- surveying
- professional land surveyor requirements
- drone/UAS work
- LiDAR collection
- photogrammetry
- civil engineering
- heavy field data collection
- utility locating
- construction inspection
- traffic engineering
- environmental study
- geotechnical work
- physical asset inspection

Output format:

```text
Subcontractor Need: Yes / No / Possible / Unknown

Reason:
[Explain reasoning]

Recommended Partner Type:
[List partner types only]
```

Do not invent subcontractor names unless an approved list is provided.

---

## 8. Award Criteria Logic

The assistant must search for how the client will judge proposals.

Terms to search:

- evaluation criteria
- scoring criteria
- scoring weights
- selection criteria
- basis of award
- technical score
- price score
- qualifications score
- experience score
- interview requirements
- shortlist process
- best value
- lowest responsible bidder
- local preference

Award criteria categories:

```text
Clear and Favorable
Clear but Competitive
Unclear
Missing
Risky
```

---

## 9. Page-Limit and Proposal Strategy Logic

The assistant must search for:

- total page limit
- section page limits
- resume limits
- cover letter limits
- required form rules
- attachment limits
- font size rules
- margin rules
- file size limits
- upload portal rules

Page-limit categories:

```text
No Page Limit Found
Manageable Page Limit
Tight Page Limit
High-Risk Page Limit
Unknown
```

---

## 10. Historical RFP Comparison Logic

Historical examples should be used for comparison, not automatic decisions.

For each similar historical example, include:

```text
Example:
Similarity Level:
Why Similar:
Previous Decision:
Important Difference:
Lesson for Current RFP:
```

The assistant must never say a new RFP is Go only because an old similar one was Go.

---

## 11. Scorecard Logic

Use a 100-point scale.

| Category | Points |
|---|---:|
| Capability Fit | 25 |
| Geography Fit | 15 |
| Financial / Deal Value Fit | 15 |
| Proposal Effort Fit | 10 |
| Contract / Insurance Risk | 15 |
| Field Work / Subcontractor Risk | 10 |
| Award Criteria Clarity | 10 |
| Total | 100 |

Decision guide:

```text
80–100 = Go
60–79 = Conditional Go
Below 60 = No-Go
```

Automatic Conditional Go triggers:

- missing deadline
- unclear scope
- possible subcontractor need
- moderate field work
- unclear award criteria
- page-limit concern
- insurance review needed
- missing project value

Automatic No-Go triggers:

- major scope mismatch
- heavy field-work requirement
- extreme travel burden
- very low value
- unacceptable liability
- unacceptable insurance or bonding terms
- mandatory services outside capability
- unrealistic schedule
- major security or compliance burden

---

## 12. Compliance Matrix Logic

The assistant must generate a matrix with:

```text
Requirement | Owner | Status | Risk Level | Notes
```

Recommended owners:

- Proposal Lead
- Technical Lead
- Leadership
- Admin / Operations
- Finance
- Legal / Contract Review
- GIS Team
- Subcontractor / Partner

Recommended status values:

```text
Found
Missing
Needed
Needs Review
Not Applicable
Unknown
```

---

## 13. Final Output Logic

Every completed appraisal must end with:

1. Opportunity Overview
2. Final Recommendation
3. Scorecard
4. Scope Fit Review
5. Red-Flag Review
6. Hidden Field-Work Review
7. Geography and Drive-Time Review
8. Subcontractor Need Review
9. Award Criteria Review
10. Page-Limit and Proposal Strategy Review
11. Similar Past RFP Comparison
12. Compliance Matrix
13. PDF-Ready Executive Summary
14. Final Next Steps
