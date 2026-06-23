# V2 vs V3 Evaluation Checklist

Use this checklist when comparing model outputs.

| Evaluation Area | V2 Behavior | V3 Expected Behavior | Pass / Fail |
|---|---|---|---|
| Missing RFP detection | May ask generally | Clearly separates knowledge base from active RFP |  |
| Knowledge-base awareness | May be generic | Identifies service catalogs and reference files |  |
| Scope fit | General summary | Compares against Cloudpoint services |  |
| Red flags | Basic risks | Expanded red-flag categories |  |
| Field work | May only check onsite | Detects hidden field-work language |  |
| Geography | May be limited | Uses priority state and Metamora logic |  |
| Subcontractor need | May be generic | Detects partner need and avoids invented names |  |
| Award criteria | May miss details | Required review section |  |
| Page limits | May miss details | Required strategy section |  |
| Historical examples | May ignore or overuse | Uses as comparison only |  |
| Compliance matrix | May be absent | Required matrix |  |
| Final output | Summary style | PDF-ready appraisal report |  |
| Hallucination control | May assume details | Marks missing information clearly |  |

## Pass Standard

V3 passes if it:

- identifies missing RFPs correctly
- avoids hallucination
- separates knowledge base from active RFP
- detects hidden field-work language
- identifies subcontractor needs
- checks geography
- checks award criteria
- checks page limits
- builds a compliance matrix
- provides a scorecard
- gives a clear recommendation
- creates a PDF-ready output
