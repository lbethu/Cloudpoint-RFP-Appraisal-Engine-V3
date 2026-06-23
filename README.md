# Cloudpoint RFP Appraisal Engine V3

## Tagline

**Turning RFP review into a structured, repeatable, and decision-ready appraisal workflow.**

## Repository Description

Cloudpoint RFP Appraisal Engine V3 is an AI-powered Local Government RFP appraisal framework designed to support Go / Conditional Go / No-Go decision-making using structured instruction logic, Cloudpoint-specific knowledge-base organization, red-flag detection, compliance matrix generation, and PDF-ready executive summaries.

This repository is designed to be opened directly in VS Code, reviewed by leadership, and used as the source package for building or maintaining a Gemini Gem, custom GPT, Claude Project, or any other LLM-based internal assistant.

---

## What This Project Does

This project provides a complete instruction and documentation framework for an internal AI assistant that reviews RFPs, RFQs, bid opportunities, and solicitation documents.

The assistant is designed to help answer:

- Is this RFP a good fit for Cloudpoint?
- Does the scope match Cloudpoint’s GIS and geospatial services?
- Are there hidden field-work or onsite obligations?
- Does the RFP require surveying, drone, LiDAR, GPS collection, field inspection, or civil engineering work?
- Is a subcontractor or partner likely needed?
- Is the opportunity geographically reasonable from Metamora, Illinois?
- Are there insurance, liability, security, bonding, or contract risks?
- Are there page limits or proposal strategy constraints?
- How will the client evaluate the proposal?
- What compliance items must be prepared?
- Is this similar to past Go, No-Go, Won, or Lost opportunities?
- Should the team pursue, decline, or further review the opportunity?

---

## Why V3 Exists

Earlier versions of the RFP GPT were useful for summarizing and identifying basic risks. V3 changes the assistant into a more structured appraisal engine.

V3 is designed to avoid three common AI failure modes:

1. Treating company knowledge-base documents as if they are the active RFP.
2. Summarizing documents without producing a decision-ready recommendation.
3. Missing hidden risk language such as field verification, data collection, asset inventory, inspection, surveying, drone, LiDAR, GPS collection, or onsite delivery.

---

## Core V3 Capabilities

1. Document classification
2. Missing RFP detection
3. Opportunity intake extraction
4. Scope fit review
5. Red-flag detection
6. Hidden field-work detection
7. Geography and drive-time review
8. Subcontractor need detection
9. Award criteria review
10. Page-limit and proposal strategy review
11. Historical Go/No-Go comparison
12. Scorecard-based recommendation
13. Compliance matrix generation
14. PDF-ready executive summary
15. Test prompts for comparing model versions

---

## Recommended Repository Structure

```text
Cloudpoint-RFP-Appraisal-Engine-V3/
│
├── README.md
├── QUICKSTART.md
├── GEMINI_SETUP_GUIDE.md
├── CHANGELOG.md
├── CONTRIBUTING.md
├── LICENSE_PLACEHOLDER.md
│
├── docs/
│   ├── 01_project_overview.md
│   ├── 02_v3_instruction_logic.md
│   ├── 03_knowledge_base_structure.md
│   ├── 04_user_guide.md
│   ├── 05_maintenance_and_versioning.md
│   └── 06_future_roadmap.md
│
├── prompts/
│   ├── v3_master_instruction_prompt.md
│   ├── quick_test_prompt.md
│   ├── full_rfp_appraisal_prompt.md
│   └── customization_template.md
│
├── templates/
│   ├── compliance_matrix_template.md
│   ├── pdf_ready_summary_template.md
│   ├── rfp_intake_form_template.md
│   └── scoring_template.md
│
├── examples/
│   ├── sample_test_cases.md
│   ├── sample_missing_rfp_response.md
│   ├── sample_conditional_go_output.md
│   └── sample_compliance_matrix.md
│
├── knowledge_base_structure/
│   ├── README.md
│   ├── 01_company_context_README.md
│   ├── 02_service_catalogs_README.md
│   ├── 03_decision_rules_README.md
│   ├── 04_geography_drive_time_README.md
│   ├── 05_historical_rfp_examples_README.md
│   ├── 06_output_templates_README.md
│   └── 07_test_cases_README.md
│
└── tests/
    ├── v2_vs_v3_evaluation_checklist.md
    └── expected_behavior_matrix.md
```

---

## How To Use This Repo

### Step 1: Open in VS Code

Download this folder, unzip it, and open the folder in VS Code.

### Step 2: Review the Master Prompt

Open:

```text
prompts/v3_master_instruction_prompt.md
```

This is the main instruction block to paste into Gemini Gem, custom GPT, Claude Project instructions, or another LLM assistant setup.

### Step 3: Build the Knowledge Base

Open:

```text
docs/03_knowledge_base_structure.md
knowledge_base_structure/README.md
```

Use these files to organize the knowledge base into company context, service catalogs, decision rules, geography logic, historical RFP examples, output templates, and test cases.

### Step 4: Add Test Cases

Use:

```text
examples/sample_test_cases.md
```

Run the same prompts in V2 and V3 to compare output quality.

### Step 5: Maintain Version Control

Use GitHub to track changes to instruction logic, test cases, knowledge base structure, and prompt improvements.

---

## Recommended GitHub Repo

Repository URL:

```text
https://github.com/lbethu/Cloudpoint-RFP-Appraisal-Engine-V3
```

Suggested Git commands:

```bash
git clone https://github.com/lbethu/Cloudpoint-RFP-Appraisal-Engine-V3.git
cd Cloudpoint-RFP-Appraisal-Engine-V3

# Copy these generated files into the repo folder

git add .
git commit -m "Add V3 RFP appraisal engine documentation and prompt framework"
git push origin main
```

---

## Main Files for Non-Technical Users

If someone only wants to understand and use the system, start with:

1. `QUICKSTART.md`
2. `GEMINI_SETUP_GUIDE.md`
3. `prompts/v3_master_instruction_prompt.md`
4. `examples/sample_test_cases.md`
5. `docs/03_knowledge_base_structure.md`

---

## Main Files for Technical / AI Workflow Users

If someone wants to maintain or improve the AI assistant, start with:

1. `docs/02_v3_instruction_logic.md`
2. `tests/v2_vs_v3_evaluation_checklist.md`
3. `tests/expected_behavior_matrix.md`
4. `templates/scoring_template.md`
5. `CHANGELOG.md`

---

## Current Status

```text
Version: V3 Draft
Status: Repo-ready documentation and prompt framework
Primary platform: Gemini Gem
Compatible platforms: Gemini, ChatGPT/GPTs, Claude Projects, internal LLM assistants
Primary workflow: Local Government RFP appraisal
```

---

## Important Notes

This system supports decision-making but does not replace leadership, legal, contract, finance, or proposal review.

The assistant should identify risks, missing information, and likely decision factors, but final Go / No-Go decisions should remain with the appropriate internal reviewers.
