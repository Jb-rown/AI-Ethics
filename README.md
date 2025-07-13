# AI Ethics Assignment: Designing Responsible and Fair AI Systems

## Overview
This repository contains the deliverables for the AI Ethics Assignment under the theme "Designing Responsible and Fair AI Systems" for the PLP Academy. The project addresses ethical principles in AI, including bias, fairness, transparency, privacy, and social impact. It includes theoretical answers, case study analyses, a practical audit of the COMPAS Recidivism Dataset using AI Fairness 360, an ethical reflection, and a bonus task proposing ethical AI guidelines for healthcare.

**Objective**: Evaluate understanding of AI ethics, identify and mitigate biases, and apply ethical frameworks to real-world scenarios.

**Tools Used**:
- **Libraries**: AI Fairness 360, Pandas, Matplotlib
- **Datasets**: COMPAS Recidivism Dataset (via AIF360 or ProPublica)
- **Frameworks**: EU Ethics Guidelines for Trustworthy AI



## Project Structure
```
AI_Ethics_Assignment/
├── docs/
│   ├── AI_Ethics_Assignment.pdf          # Parts 1, 2, 4: Theoretical answers, case studies, reflection
│   ├── COMPAS_Audit_Report.pdf           # Part 3: 300-word audit report
│   ├── Healthcare_AI_Guideline.pdf       # Bonus Task: Ethical AI guideline for healthcare
├── compas_audit.py                   # Part 3: Python script for COMPAS dataset audit
├── requirements.txt                  # Python dependencies
├── compas_audit.ipynb                      # False positive rate bar chart
├── data/
│   ├── compas_data/                      # Placeholder for COMPAS dataset 
├── README.md                             # This file
                           
```

### Directory Details
- **docs/**: Contains PDF reports:
  - `AI_Ethics_Assignment.pdf`: Answers for Parts 1 (theoretical questions, ethical principles), 2 (case studies on Amazon hiring tool and facial recognition), and 4 (ethical reflection on a healthcare AI project).
  - `COMPAS_Audit_Report.pdf`: 300-word report summarizing the COMPAS dataset audit, including fairness metrics and remediation steps.
  - `Healthcare_AI_Guideline.pdf`: Bonus task with a 1-page ethical AI guideline for healthcare, covering patient consent, bias mitigation, and transparency.
- **code/**: Contains the Python script and dependencies:
  - `compas_audit.py`: Audits the COMPAS dataset for racial bias using AI Fairness 360, computing disparate impact ratio and false positive rate difference, and generating a bar chart.
  - `requirements.txt`: Lists dependencies (aif360, pandas, matplotlib).
- **visualizations/**: Stores the output bar chart (`fpr_plot.png`) showing false positive rates by race.
- **data/**: Placeholder for the COMPAS dataset, accessed via AIF360 or ProPublica (not included in repo due to size).

## Setup Instructions
1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   cd AI_Ethics_Assignment
   ```
2. **Install Dependencies**:
   - Ensure Python 3.8+ is installed.
   - Install required libraries:
     ```bash
     pip install -r code/requirements.txt
     ```
   - `requirements.txt` contents:
     ```
     aif360==0.5.0
     pandas==2.0.3
     matplotlib==3.7.1
     ```
3. **Access the COMPAS Dataset**:
   - The dataset is loaded via AIF360’s `CompasDataset` class. Alternatively, download it from:
     - ProPublica: [https://github.com/propublica/compas-analysis](https://github.com/propublica/compas-analysis)
   - Place the dataset in `data/compas_data/` or let AIF360 handle fetching.

## Running the Audit
1. **Execute the Audit Script**:
   ```bash
   python code/compas_audit.py
   ```
2. **Outputs**:
   - Console: Prints fairness metrics (disparate impact ratio, false positive rate difference).
   - Visualization: Saves `fpr_plot.png` in `visualizations/`, showing false positive rates for Caucasian and African-American groups.
   - Use the output in `COMPAS_Audit_Report.pdf` for Part 3.

## Deliverables
- **Written Answers** (Parts 1, 2, 4):
  - `docs/AI_Ethics_Assignment.pdf`:
    - **Part 1 (30%)**: Defines algorithmic bias, transparency vs. explainability, GDPR’s impact; matches ethical principles (Justice, Non-maleficence, Autonomy, Sustainability).
    - **Part 2 (40%)**: Analyzes Amazon’s biased hiring tool (fixes: diverse data, fairness algorithms, audits) and facial recognition in policing (policies: testing, transparency, oversight).
    - **Part 4 (5%)**: Reflects on a healthcare AI project, ensuring bias mitigation, transparency, and privacy.
- **Practical Audit** (Part 3, 25%):
  - `code/compas_audit.py`: Audits COMPAS dataset for racial bias.
  - `visualizations/fpr_plot.png`: Bar chart of false positive rates.
  - `docs/COMPAS_Audit_Report.pdf`: 300-word report summarizing findings (e.g., disparate impact ratio ~0.65, false positive rate difference ~0.15) and remediation steps (data rebalancing, fairness algorithms, human oversight).
- **Bonus Task** (Extra 10%):
  - `docs/Healthcare_AI_Guideline.pdf`: Proposes ethical AI guidelines for healthcare, covering patient consent, bias mitigation, and transparency.
- **GitHub Repository**: Share `code/` and `visualizations/` via GitHub.
- **PLP Academy Community**: Share `Healthcare_AI_Guideline.pdf` in #AIEthicsAssignment.

## Grading Rubric
- **Theoretical Accuracy** (30%): Clear, accurate definitions and principle matching in `AI_Ethics_Assignment.pdf`.
- **Case Study Depth & Solutions** (40%): Detailed analysis and actionable fixes for hiring and facial recognition cases.
- **Technical Audit Execution** (25%): Correct use of AIF360, meaningful metrics, and clear visualization in `compas_audit.py` and `COMPAS_Audit_Report.pdf`.
- **Reflection & Creativity** (5%): Thoughtful reflection on ethical AI design.
- **Bonus Task** (10%): Comprehensive healthcare guideline.

## Notes for Collaboration
- **Group Workflow**: Assign tasks (e.g., one member per part, one for bonus task). Use GitHub for version control and peer reviews.
- **Dataset Access**: Ensure all members can access the COMPAS dataset via AIF360 or ProPublica.
- **Formatting**: Use LaTeX or Word for PDFs, ensuring professional formatting.
- **Testing**: Verify `compas_audit.py` runs without errors and produces expected outputs.

## Troubleshooting
- **AIF360 Issues**: Ensure `aif360` is installed correctly. Check [AIF360 GitHub](https://github.com/Trusted-AI/AIF360) for documentation.
- **Dataset Errors**: If `CompasDataset` fails, manually download from ProPublica and preprocess using Pandas.
- **Visualization Issues**: Confirm Matplotlib is installed and `visualizations/` folder exists.

## References
- NIST (2019): Facial recognition bias study.
- ProPublica (2016): COMPAS algorithm bias investigation.
- EU GDPR: Right to explanation.
- Pew Research (2021): Data privacy concerns.
- World Economic Forum (2020): AI’s impact on jobs.
- EU Ethics Guidelines for Trustworthy AI.

## Contact
For questions, join the PLP Academy Community discussion (#AIEthicsAssignment) or contact group members via agreed channels.

**Pro Tip**: Start with fairness metrics like disparate impact ratio and equal opportunity difference. Small steps lead to big ethical wins! 🌟