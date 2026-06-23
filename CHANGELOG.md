# Changelog

## V3 Draft

### Added

- Document classification logic
- Missing RFP detection
- Hidden field-work detection
- Award criteria review
- Page-limit and proposal strategy review
- Compliance matrix generation
- Geography and drive-time risk logic
- Subcontractor need detection
- Historical Go/No-Go comparison
- Scorecard-based recommendation
- PDF-ready report structure
- Gemini Gem setup guide
- Knowledge base folder structure
- V2 vs V3 evaluation checklist
- Prompt customization template

### Changed

- Shifted from general RFP summarization to structured RFP appraisal
- Improved separation between knowledge base files and active RFP files
- Added Conditional Go as a formal decision category
- Added clearer output requirements for professional reporting
- Added explicit missing-information behavior

### Known Limitations

- The assistant depends on the quality and completeness of uploaded RFP documents
- Historical comparison quality depends on properly labeled past examples
- Drive-time logic may require human review unless exact location details are available
- Contract, legal, finance, and insurance risks still require internal review
- The assistant should not be treated as the final decision-maker

### Future Improvements

- Add structured RFP intake form
- Add automated PDF generation
- Add JSON output for dashboard integration
- Add scoring dashboard
- Add historical RFP similarity index
- Add approval workflow
- Add RFP archive with tags and outcomes
- Add human review status tracking
