
PROJECT IN ONE MINUTE
Project Title

CaseTwin: A Multimodal Agentic Clinical Decision Support System for Similar Case Retrieval and Specialist Referral

One-line explanation

CaseTwin helps clinicians analyze a patient's chest X-ray and clinical information, retrieve historically similar cases, compare them, identify appropriate specialist facilities, and generate a structured referral memo.

Simple workflow
Patient / Clinician
        │
        ▼
Clinical Notes + Chest X-ray + Labs
        │
        ▼
┌──────────────────────────┐
│ Multimodal AI Analysis   │
│ MedGemma + MedSigLIP     │
└────────────┬─────────────┘
             │
             ▼
      Similar Case Search
             │
             ▼
      Historical Comparison
             │
             ▼
      Specialist Routing
             │
             ▼
       Doctor Review
             │
             ▼
      Referral Generation

Your strongest concept is:

AI should assist the doctor, not replace the doctor.

So your final architecture should become:

AI Analysis
     ↓
AI Recommendation
     ↓
Doctor Review
     ↓
Final Clinical Decision

That is much stronger academically and safer clinically.
