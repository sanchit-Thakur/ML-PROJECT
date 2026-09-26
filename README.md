# 🛡️ AI Government & Exam Form Error Predictor

[![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://www.python.org/)
[![Colab](https://img.shields.io/badge/Jupyter-Colab-orange.svg)](https://colab.research.google.com/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-F7931E.svg)](https://scikit-learn.org/)
[![Pandas](https://img.shields.io/badge/Pandas-150458.svg)](https://pandas.pydata.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-blueviolet.svg)](https://seaborn.pydata.org/)
[![Build Status](https://img.shields.io/badge/Build-Passing-brightgreen.svg)]()

*A proactive Machine Learning pre-flight check engine that detects application discrepancies, predicts rejection risk, and flags compliance issues before final exam/job portal submission.*

---

## 📌 Problem Overview

Every year, millions of students and competitive exam aspirants submit forms for major government recruitment and entrance tests (e.g., UPSC, SSC, State PSCs, JEE, NEET). A massive percentage face automatic disqualification due to avoidable submission errors:

```text
┌────────────────────────────────────────────────────────────────────────┐
│                   COMMON APPLICATION REJECTION TRAPS                   │
├────────────────────────────────────────────────────────────────────────┤
│  ❌ Document Incompleteness  : Missing mandatory category / quota proof │
│  ❌ Eligibility Mismatches   : Age limits, board requirements missed   │
│  ❌ Upload Formatting Errors : Photo/signature resolution & DPI flaws  │
│  ❌ Deadline & Criteria Lapses: Category validity after cutoff dates   │
└────────────────────────────────────────────────────────────────────────┘

[ Applicant Data & Checklist ]
         │
         ▼
[ Feature Extraction & Preprocessing ]
   ├── Categorical Encoding
   ├── Missing Value Handling (dropna/imputation)
   └── Standard Feature Scaling
         │
         ▼
[ Regression & Risk Estimation Model ]
   ├── Target: Continuous Evaluation Index (G3/Risk Index)
   ├── Loss Optimization: MSE / MAE Minimization
   └── Coefficient Analysis (Factor Impact)
         │
         ▼
[ Risk Calibration & Diagnostics ]
   ├── ⚠️ Risk Level: HIGH / MEDIUM / LOW
   ├── 📊 Risk Score: 82%
   └── 🔍 Error Breakdown & Remediation Action Items

{
  "applicant_id": "CAND-2026-9041",
  "exam_target": "XYZ Recruitment Exam",
  "demographics": {
    "age": 19,
    "qualification": "12th Standard",
    "category": "OBC",
    "domicile_state": "Himachal Pradesh"
  },
  "document_verification": {
    "identity_proof": true,
    "academic_marksheet": true,
    "category_certificate": false
  },
  "media_compliance": {
    "photograph_valid_format": false,
    "signature_valid_format": true
  }
}

══════════════════════════════════════════════════════════════════════
                   PRE-SUBMISSION FORM AUDIT REPORT
══════════════════════════════════════════════════════════════════════
 ⚠️  RISK LEVEL : HIGH
 📊  RISK SCORE : 82%  [████████████████░░░░]
──────────────────────────────────────────────────────────────────────
 CRITICAL ERRORS & COMPLIANCE WARNINGS
──────────────────────────────────────────────────────────────────────
 [ 1 ] Required Certificate Missing: Category declared as 'OBC', but 
       supporting reservation certificate is marked FALSE/UNATTACHED.
 [ 2 ] Educational Qualification Verification: Candidate qualification 
       status requires verification against the specific minimum cutoff 
       criteria of the target recruitment.
 [ 3 ] Media Specifications Non-Compliant: Uploaded candidate photograph 
       does not adhere to portal dimension and DPI parameters.
──────────────────────────────────────────────────────────────────────
 RECOMMENDED ACTION PLAN
──────────────────────────────────────────────────────────────────────
 ✔ Attach a valid Central/State OBC certificate issued prior to cutoff.
 ✔ Re-upload photograph conforming to standard portal specs (20KB–50KB).
══════════════════════════════════════════════════════════════════════

# Clone repository
git clone [https://github.com/sanchit-Thakur/ML-PROJECT.git](https://github.com/sanchit-Thakur/ML-PROJECT.git)
cd ML-PROJECT

# Install dependencies
pip install -r requirements.txt

# Run notebook
jupyter notebook
