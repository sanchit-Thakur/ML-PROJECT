# 🛡️ AI Government & Exam Form Error Predictor

[![Python](https://img.shields.io/badge/Python-3.9%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.110%2B-009688?style=for-the-badge&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com)
[![Scikit-Learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org)
[![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org)
[![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)](https://numpy.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)

An intelligent pre-submission risk assessment and anomaly detection engine designed to prevent candidate disqualifications and registration rejections across competitive examinations and government recruitments (e.g., SSC, UPSC, State PSCs, JEE, NEET).

---

## 📌 Executive Summary

Every year, millions of applicants register for competitive exams and public sector recruitments. A significant percentage face outright rejection or cancellation during scrutiny and Document Verification (DV) due to clerical errors and oversight:

| Error Category | Common Mistake | Direct Impact |
| :--- | :--- | :--- |
| **Missing Certificates** | Omitting OBC-NCL, EWS, PwD, or State Domicile proofs | Loss of reservation quota or immediate cancellation |
| **Eligibility Mismatch** | Age outside criteria on cutoff date, invalid degree/stream | Scrutiny failure before admit card release |
| **Media Non-Compliance** | Photo/signature defying aspect ratio, file size, or DPI limits | Rejection by automated upload gates |
| **Data Inconsistencies** | Name discrepancies across matriculation records vs. ID | Disqualification during final document verification |

This tool functions as a **smart pre-flight checker**: applicants input their profile details, and the hybrid machine learning and rule-based pipeline evaluates inconsistencies, scores rejection probability, and provides actionable remediation steps before final submission.

---

## 💡 System Architecture

```text
┌──────────────────────────┐
│  Applicant Form Payload  │
│  (Age, Category, Docs)   │
└────────────┬─────────────┘
             │
             ▼
┌──────────────────────────┐
│ Feature Vectorization &  │
│ Categorical Encoding     │
└────────────┬─────────────┘
             │
             ▼
┌────────────────────────────────────────────────────────┐
│               Hybrid Inference Pipeline                │
│ ┌────────────────────────┐  ┌────────────────────────┐ │
│ │  Deterministic Rules   │  │   Trained ML Model     │ │
│ │  (Eligibility Criteria)│  │   (Risk Probability)   │ │
│ └───────────┬────────────┘  └───────────┬────────────┘ │
└─────────────┼───────────────────────────┼──────────────┘
              │                           │
              └─────────────┬─────────────┘
                            │
                            ▼
              ┌───────────────────────────┐
              │     Diagnostic Report     │
              │   • Risk Tier (High/Med)  │
              │   • Calibrated Score (%)  │
              │   • Actionable Fixes      │
              └───────────────────────────┘

ML-PROJECT/
├── data/
│   ├── raw/                  # Raw simulated form submissions
│   └── processed/            # Cleaned, vectorized training data
├── models/
│   ├── model.pkl             # Serialized inference model
│   └── preprocessor.pkl      # Column transformers and encoders
├── notebooks/
│   └── exploratory_eda.ipynb # EDA, feature engineering, and model training
├── src/
│   ├── __init__.py
│   ├── config.py             # Feature configurations and threshold values
│   ├── preprocessing.py      # Input transformation and payload validation
│   ├── rules.py              # Statutory rule-checking algorithms
│   └── predictor.py          # Unified inference pipeline
├── app.py                    # FastAPI application server
├── requirements.txt          # Python dependencies
└── README.md
