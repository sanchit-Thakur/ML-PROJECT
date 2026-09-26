# 🛡️ AI Government & Exam Form Error Predictor

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.9+-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="Scikit-Learn" />
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas" />
  <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" alt="NumPy" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI" />
  <img src="https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge" alt="Status" />
</p>

<p align="center">
  <b>Pre-submission risk scoring & anomaly detection engine designed to prevent government application and entrance exam registration rejections.</b>
</p>

---

## 📌 Executive Summary

Every year, thousands of job applicants and students face automatic rejection during competitive exams (SSC, UPSC, State PSCs, JEE, NEET) due to avoidable clerical mistakes:

| Error Type | Common Mistake | Real-World Impact |
| :--- | :--- | :--- |
| **Missing Certificates** | Forgetting OBC-NCL, EWS, or Domicile proofs | Loss of reservation benefits or immediate cancellation |
| **Eligibility Mismatch** | Underage/overage by cutoff date or wrong degree stream | Disqualification during scrutiny |
| **Media Non-Compliance** | Photo/signature violating dimension, DPI, or size rules | Automated rejection by upload gates |
| **Profile Inconsistencies** | Qualification marks, board roll numbers, or state mismatches | Document verification (DV) failure |

This system acts as a **smart pre-flight check**: applicants submit their profile metadata, and an ML-powered inference engine flags errors, estimates rejection probability, and delivers clear remediation steps before final payment and submission.

---

## 💡 How It Works
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
│   • Specific Error List   │
└───────────────────────────┘


