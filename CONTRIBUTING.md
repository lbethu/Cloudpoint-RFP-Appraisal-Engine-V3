# Contributing Guide

## Purpose

This repository should stay clean, structured, and easy for another person to understand.

Any update to the prompt, knowledge base structure, templates, or examples should be made carefully because these files affect how the AI assistant behaves.

---

## Recommended Workflow

1. Create a branch for changes.
2. Update the relevant file.
3. Run the sample test cases.
4. Compare the output against the expected behavior matrix.
5. Update the changelog.
6. Commit with a clear message.

Example commit messages:

```text
Improve hidden field-work detection rules
Add subcontractor need detection examples
Update Gemini Gem setup guide
Add V2 vs V3 test case results
Refine compliance matrix template
```

---

## Do Not

- Do not mix active RFPs with knowledge base documentation.
- Do not add confidential client documents to a public repo.
- Do not store private pricing or contract information unless the repo is private and approved.
- Do not remove missing RFP detection logic.
- Do not allow the assistant to invent subcontractor names.
- Do not simplify V3 into only a summarizer.

---

## When Updating the Master Prompt

If you update:

```text
prompts/v3_master_instruction_prompt.md
```

also review:

```text
docs/02_v3_instruction_logic.md
examples/sample_test_cases.md
tests/expected_behavior_matrix.md
CHANGELOG.md
```

---

## Quality Standard

A good update should improve one or more of the following:

- accuracy
- risk detection
- output consistency
- maintainability
- knowledge-base clarity
- testability
- user experience
- decision quality
