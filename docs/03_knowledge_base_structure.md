# Knowledge Base Structure

## Purpose

The knowledge base gives the assistant the reference material it needs to evaluate RFPs in a Cloudpoint-specific way.

The knowledge base should be organized by function so the assistant understands what each file is supposed to do.

A clean knowledge base helps the assistant:

- avoid hallucination
- separate reference files from active RFP files
- compare scopes accurately
- apply consistent Go/No-Go logic
- use historical examples correctly
- produce consistent outputs

---

## Recommended Structure

```text
LG_RFP_GPT_Knowledge_Base/
│
├── 01_Company_Context/
├── 02_Service_Catalogs/
├── 03_Decision_Rules/
├── 04_Geography_Drive_Time/
├── 05_Historical_RFP_Examples/
├── 06_Output_Templates/
└── 07_Test_Cases/
```

---

## 01 Company Context

Purpose:

This folder explains who Cloudpoint is, what types of clients it serves, what types of work it prefers, and what style/tone should be used.

Recommended files:

```text
Cloudpoint_Overview.pdf
Preferred_Client_Profile.pdf
Company_Service_Positioning.pdf
Local_Government_Context.pdf
Internal_Proposal_Tone_Guidance.pdf
```

Important contents:

- company overview
- preferred client types
- preferred project types
- preferred geographies
- proposal tone
- business development positioning
- services to prioritize
- services to be careful about

---

## 02 Service Catalogs

Purpose:

This folder defines Cloudpoint’s service capabilities.

Recommended files:

```text
Local_Government_GIS_Services.pdf
Managed_GIS_Services.pdf
Indoor_GIS_Services.pdf
Data_Collection_Services.pdf
Asset_Management_Services.pdf
Utility_Network_Services.pdf
Parcel_Fabric_Services.pdf
ArcGIS_Enterprise_Services.pdf
ArcGIS_Online_Services.pdf
GIS_Dashboard_and_Web_Map_Services.pdf
```

The assistant uses these files to evaluate scope fit.

---

## 03 Decision Rules

Purpose:

This folder defines how the assistant decides Go, Conditional Go, or No-Go.

Recommended files:

```text
Go_NoGo_Decision_Criteria.pdf
Red_Flag_Detection_Rules.pdf
Field_Work_Detection_Rules.pdf
Subcontractor_Need_Rules.pdf
Insurance_Liability_Risk_Rules.pdf
Security_Risk_Rules.pdf
Low_Value_Opportunity_Rules.pdf
Page_Limit_Review_Rules.pdf
Award_Criteria_Review_Rules.pdf
```

This is the most important folder for consistent decision-making.

---

## 04 Geography and Drive-Time

Purpose:

This folder helps the assistant evaluate location risk.

Recommended files:

```text
Priority_States.pdf
Metamora_Drive_Time_Logic.pdf
Travel_Risk_Categories.pdf
Out_Of_Region_Risk_Rules.pdf
Onsite_Travel_Burden_Rules.pdf
```

Important contents:

- priority states
- preferred service region
- drive-time categories from Metamora, IL
- out-of-region risk rules
- onsite travel burden rules
- recurring meeting risk

---

## 05 Historical RFP Examples

Purpose:

This folder gives the assistant examples of past Go, Conditional Go, No-Go, Won, and Lost opportunities.

Recommended files:

```text
Prior_Go_Examples.pdf
Prior_Conditional_Go_Examples.pdf
Prior_NoGo_Examples.pdf
Won_RFP_Examples.pdf
Lost_RFP_Examples.pdf
Historical_RFP_Decision_Log.pdf
```

Each historical example should include:

- RFP title
- client type
- state
- service area
- decision
- risk level
- field-work status
- subcontractor status
- outcome
- lesson learned

Important rule:

```text
Historical examples should guide the recommendation, not automatically determine it.
```

---

## 06 Output Templates

Purpose:

This folder gives the assistant consistent report formats.

Recommended files:

```text
Executive_Summary_Template.pdf
Compliance_Matrix_Template.pdf
PDF_Ready_Report_Template.pdf
Risk_Review_Template.pdf
Scorecard_Template.pdf
Go_NoGo_Summary_Template.pdf
```

---

## 07 Test Cases

Purpose:

This folder stores prompts and expected behaviors used to validate the assistant.

Recommended files:

```text
Missing_RFP_Test.pdf
Knowledge_Base_Only_Test.pdf
Field_Work_Detection_Test.pdf
Subcontractor_Detection_Test.pdf
Geography_Risk_Test.pdf
Award_Criteria_Test.pdf
Page_Limit_Test.pdf
Compliance_Matrix_Test.pdf
Historical_Comparison_Test.pdf
Full_RFP_Appraisal_Test.pdf
```

---

## Recommended Metadata Tags

Use these tags for historical examples:

```text
Decision: Go / Conditional Go / No-Go
Outcome: Won / Lost / Pending / Unknown
Client Type: City / County / Utility / State Agency / School District / Other
State: IL / WI / IA / MO / KS / OH / IN / MI / KY / Other
Service Area: Managed GIS / Utility Network / Parcel Fabric / Indoor GIS / Data Collection / Asset Management / ArcGIS Enterprise / Other
Risk Level: Low / Medium / High / Critical
Field Work: Yes / No / Possible / Unknown
Subcontractor Needed: Yes / No / Possible / Unknown
Page Limit Risk: Low / Medium / High / Unknown
Insurance Risk: Low / Medium / High / Unknown
Geography Risk: Low / Medium / High / Unknown
```

---

## Best Practice Summary

```text
Company Knowledge = who we are
Service Catalogs = what we do
Decision Rules = how we decide
Geography Logic = where we prefer to work
Historical Examples = what happened before
Templates = how outputs should look
Test Cases = how we validate the assistant
```
