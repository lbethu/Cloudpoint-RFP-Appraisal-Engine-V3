# Quickstart Guide

## Purpose

This quickstart explains how to use the Cloudpoint RFP Appraisal Engine V3 files in a Gemini Gem, custom GPT, Claude Project, or similar AI assistant.

---

## Fast Setup

### 1. Open the repo in VS Code

Unzip the folder and open it in VS Code.

### 2. Copy the master instruction prompt

Open:

```text
prompts/v3_master_instruction_prompt.md
```

Copy the full contents into the custom instructions area of the Gemini Gem or other assistant.

### 3. Add the Gem description

Use the description from:

```text
GEMINI_SETUP_GUIDE.md
```

### 4. Upload knowledge base files

Use this structure:

```text
01_Company_Context
02_Service_Catalogs
03_Decision_Rules
04_Geography_Drive_Time
05_Historical_RFP_Examples
06_Output_Templates
07_Test_Cases
```

### 5. Run a missing RFP test

Before uploading an RFP, test the assistant with:

```text
Please review this RFP and provide a Go/No-Go recommendation for Cloudpoint. Include red flags, field work, subcontractor needs, geography risk, award criteria, page limits, a compliance matrix, and a PDF-ready summary.
```

Expected behavior:

The assistant should say that no actual RFP was provided and should not invent an appraisal.

### 6. Upload a real RFP and run the full prompt

Use:

```text
prompts/full_rfp_appraisal_prompt.md
```

---

## What Good Output Looks Like

A strong V3 output should include:

- opportunity overview
- Go / Conditional Go / No-Go recommendation
- scorecard
- scope fit review
- red-flag review
- hidden field-work review
- geography review
- subcontractor review
- award criteria review
- page-limit review
- similar past RFP comparison
- compliance matrix
- PDF-ready executive summary
- final next steps

---

## What Bad Output Looks Like

A weak output usually:

- only summarizes the RFP
- ignores missing RFP detection
- confuses the knowledge base with the active RFP
- misses hidden field-work language
- does not create a compliance matrix
- ignores award criteria
- ignores page limits
- gives a Go/No-Go decision without evidence
- invents information not found in the RFP
