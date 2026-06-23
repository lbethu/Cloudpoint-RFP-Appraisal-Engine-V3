# Maintenance and Versioning

## Purpose

This file explains how to maintain the RFP Appraisal Engine V3 over time.

---

## Versioning Rule

Use semantic-style labels:

```text
V3.0 = first structured V3 release
V3.1 = small prompt improvements
V3.2 = new test cases or improved output templates
V4.0 = major workflow or architecture change
```

---

## When To Update the Master Prompt

Update the master prompt when:

- the assistant misses important risks
- new red-flag categories are identified
- knowledge base organization changes
- output format needs improvement
- leadership wants a new decision rule
- historical examples reveal a new pattern

---

## Files To Update Together

When changing the master prompt, review these files:

```text
prompts/v3_master_instruction_prompt.md
docs/02_v3_instruction_logic.md
examples/sample_test_cases.md
tests/expected_behavior_matrix.md
CHANGELOG.md
```

---

## Testing After Updates

After any major update, run:

- Missing RFP test
- Knowledge base classification test
- Hidden field-work detection test
- Subcontractor detection test
- Award criteria test
- Page-limit test
- Full appraisal test

---

## Recommended Commit Style

```text
Add page-limit strategy detection
Improve historical RFP comparison logic
Refine subcontractor detection trigger terms
Update compliance matrix template
Add missing RFP expected behavior test
```
