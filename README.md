# Questionnaires_for_Employees
A collection of employee questionnaires about attitudes toward AI, workplace automation, and AI-assisted decision monitoring. Includes open questionnaire formats (JSON, CSV, DOCX, XLSForm) and fully anonymized response data to support research transparency, replication, and academic publication.


# Questionnaires for Employees — Attitudes Toward AI, Monitoring, and Automation

This repository contains **open-source questionnaires** designed to evaluate employee attitudes toward Artificial Intelligence (AI) in the workplace. The focus is on:

- AI-assisted decision making  
- AI-based monitoring of employee actions  
- Workflow automation  
- Fairness, trust, and perceived risk  
- Acceptance of AI-supported evaluation  
- Transparency and explainability in organizational AI systems

The purpose of this repository is to support **transparent, reproducible, and FAIR-aligned AI research**. All questionnaires, formats, metadata, and anonymized response datasets are openly available to assist researchers, HR teams, AI practitioners, and educators.

---

## 📂 Repository Structure

Questionnaires_for_Employees/
│
├── questionnaires/
│ ├── JSON/ # Machine-readable questionnaire definitions
│ ├── CSV/ # Import-ready CSV questionnaires
│ ├── DOCX/ # Textual questionnaires for form converters
│ ├── XLSForm/ # Survey definitions for ODK/KoboToolbox
│ └── Typeform_JSON/ # Typeform-compatible JSON templates
│
├── data/
│ ├── sample/ # Synthetic or demo datasets
│ └── anonymised_real_responses/
│ ├── YYYY_survey_name/
│ │ ├── raw_anonymised.csv
│ │ ├── metadata.json
│ │ └── README.md
│
├── tools/
│ ├── converter_scripts/ # Utilities for converting formats
│ ├── validation/ # JSON schema and validation scripts
│ └── examples/ # Guides for importing questionnaires into platforms
│
└── docs/
├── methodology/
│ ├── anonymisation_guidelines.md
│ ├── ethics_statement.md
│ └── reproducibility_notes.md
└── publications/
├── references_to_this_repo.md
└── methods_appendix_templates.md



---

## 🎯 Objectives

1. **Provide standardized, reusable questionnaires** for studying employee perceptions of AI.
2. **Increase research transparency** by publishing questionnaire definitions and anonymized datasets.
3. **Support academic reproducibility** through clear metadata and methodological documentation.
4. **Enable cross-study comparison** by using consistent formats and tagging.
5. **Promote responsible AI** by openly sharing insights into worker attitudes about monitoring and automation.

---

## 📦 Questionnaire Formats Included

To ensure broad compatibility with survey tools, each questionnaire may be provided in:

- **JSON** — machine-readable; for custom tools, APIs, Typeform developer import  
- **CSV** — universal structured format, importable to many survey systems  
- **DOCX** — human-readable for review or automatic conversion (e.g., Automagical Forms)  
- **XLSForm** — for ODK, KoboToolbox, and research data collection  
- **Typeform JSON** — compatible with Typeform’s developer import tools  

If you need a format not listed here, feel free to create an issue or PR.

---

## 🔐 Anonymization & Ethics

All real response data published in this repository is:

- Fully **depersonalized**
- GDPR-compliant  
- Free of direct identifiers (name, email, ID, IP, etc.)
- Free of quasi-identifiers (rare job titles, long free-text answers)
- Aggregated where appropriate
- Reviewed manually for re-identification risk

Each dataset includes:

- A `metadata.json` describing the collection context  
- A `README.md` describing the anonymization process  
- Any transformations performed on raw data  

For more details, see:  
📄 `docs/methodology/anonymisation_guidelines.md`

---

## 🧪 Using These Questionnaires

### Import into survey tools  
Guides for various platforms can be found in:

📁 `tools/examples/`

Including instructions for:

- Google Forms (via add-ons)  
- Typeform  
- Qualtrics (QSF import)  
- ODK/KoboToolbox (XLSForm)  
- SurveyMonkey  
- LimeSurvey  

### Using in research workflows

Example Python snippet:

```python
import json

with open("questionnaires/JSON/employee_ai_attitudes_v1.json") as f:
    q = json.load(f)

for item in q["items"]:
    print(item["title"])


[FAIR_VID TEAM]. (2025). Questionnaires_for_Employees. GitHub Repository.
Retrieved from https://github.com/<your-username>/Questionnaires_for_Employees
