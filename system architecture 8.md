COMPLETE SYSTEM ARCHITECTURE

Put this diagram into your PPT.

                         CASETWIN
                            │
                            ▼
                  ┌─────────────────┐
                  │ React Frontend  │
                  │ TypeScript      │
                  │ Tailwind        │
                  └────────┬────────┘
                           │ HTTPS
                           ▼
                  ┌─────────────────┐
                  │ FastAPI Backend │
                  └────────┬────────┘
                           │
       ┌───────────────────┼────────────────────┐
       │                   │                    │
       ▼                   ▼                    ▼
   MedSigLIP            MedGemma             Gemini
       │                   │                    │
       ▼                   ▼                    ▼
   Embedding          Medical AI         Agentic Tasks
       │
       ▼
    Qdrant
       │
       ▼
 Similar Cases
       │
       ▼
 Case Comparison
       │
       ▼
 CrewAI Agents
       │
       ▼
Hospital + Specialist
       │
       ▼
 Doctor Review
       │
       ▼
 Referral Memo
20. DEPLOYMENT ARCHITECTURE

Your current deployment is:

                Internet
                    │
                    ▼
          ┌──────────────────┐
          │ Cloud Run        │
          │ Frontend         │
          │ React + Nginx    │
          └────────┬─────────┘
                   │ REST
                   ▼
          ┌──────────────────┐
          │ Cloud Run        │
          │ FastAPI Backend  │
          └────────┬─────────┘
                   │
       ┌───────────┼────────────┐
       ▼           ▼            ▼
 HuggingFace     Qdrant       Gemini
 MedGemma       Vector DB      API
 MedSigLIP

Additional:

Backend
 │
 ├── You.com
 ├── Jina
 ├── OSRM
 ├── Nominatim
 └── CrewAI
