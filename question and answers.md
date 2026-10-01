PART 1 — BASIC PROJECT QUESTIONS
Q1 ⭐ What is your project?
🎓 Viva Answer

Our project is CaseTwin, a multimodal agentic clinical decision-support system for similar case retrieval and specialist referral.

The system accepts a patient's chest X-ray along with clinical information such as symptoms, medical history, laboratory information and previous diagnosis. It uses MedSigLIP to retrieve historically similar chest X-ray cases and MedGemma to analyze and compare the current case with historical cases. It then assists in identifying suitable specialist hospitals and generates a structured referral memo. The final decision remains with the clinician.

🧑‍💻 Beginner Explanation

Think of CaseTwin as a smart assistant for a doctor.

A doctor gives:

Patient information
+
Chest X-ray

CaseTwin does:

Understand X-ray
        ↓
Find similar old cases
        ↓
Compare current and old cases
        ↓
Find suitable specialist/hospital
        ↓
Prepare referral

It does not replace the doctor.

Q2 ⭐ Why did you choose this project?
🎓 Viva Answer

We selected this problem because clinical information is often distributed across multiple sources, and finding historically similar cases manually can be time-consuming. This becomes particularly challenging for rare or atypical chest presentations. Our objective is to bring image analysis, clinical information retrieval, historical case comparison and specialist referral assistance into a unified workflow.

🧑‍💻 Beginner Explanation

Suppose a doctor sees an unusual X-ray.

They may need to:

Look at X-ray
Search old records
Search literature
Compare cases
Find specialist
Find hospital
Prepare referral

This takes time.

CaseTwin tries to put those activities into one system.

Q3 ⭐ What is the main problem you are solving?
🎓 Viva Answer

The main problem is the difficulty and time involved in retrieving and comparing historically similar clinical cases when medical information is distributed across images, clinical notes, laboratory reports and previous records.

🧑‍💻 Beginner Explanation

The problem is not simply:

“Doctors cannot diagnose X-rays.”

The problem is:

Relevant information exists, but finding and comparing it efficiently is difficult.

Q4 ⭐ What is the objective of the project?
🎓 Viva Answer

Our objectives are:

Process multimodal clinical information.
Retrieve historically similar cases.
Compare current and previous chest X-rays.
Compare clinical information between cases.
Provide evidence that can assist clinical investigation.
Assist specialist and hospital referral.
Generate a structured referral summary.
Maintain a doctor-in-the-loop workflow.
🧑‍💻 Beginner Explanation

Your project answers five basic questions:

What does the current case contain?
             ↓
What old cases look similar?
             ↓
How are they similar/different?
             ↓
Where can the patient be referred?
             ↓
How can the doctor review everything?
Q5 ⭐ What does “CaseTwin” mean?
🎓 Viva Answer

“CaseTwin” refers to finding a historical clinical case that is sufficiently similar to the current patient case to serve as a comparison or reference point.

🧑‍💻 Beginner Explanation

Imagine:

Current Patient = Case A

Historical Patient = Case B

If their clinical and imaging characteristics are similar, Case B becomes the twin case.

It doesn't mean they are medically identical.

Q6 ⭐ What does multimodal mean?
🎓 Viva Answer

Multimodal means that the system can process multiple forms of information rather than relying on only one data type. In CaseTwin, these include chest X-ray images, clinical notes, symptoms, laboratory information, medical history and structured patient information.

🧑‍💻 Beginner Explanation

Mono-modal:

Only X-ray

Multimodal:

X-ray
+
Text
+
Symptoms
+
Labs
+
Vitals

So your system doesn't look at only one piece of information.

Q7 ⭐ What does “agentic” mean in your project?
🎓 Viva Answer

Agentic refers to AI components that can perform a sequence of tasks toward a defined objective rather than simply generating a single response. In CaseTwin, agentic workflows are used particularly for hospital and physician discovery, where one agent performs research and another extracts and structures the relevant information.

🧑‍💻 Beginner Explanation

Normal AI:

Question → Answer

Agentic AI:

Goal
 ↓
Search
 ↓
Analyze
 ↓
Find information
 ↓
Process information
 ↓
Produce result

For example:

Find pulmonologists at a suitable hospital
        ↓
Search hospital
        ↓
Find doctor directory
        ↓
Find doctors
        ↓
Extract credentials
        ↓
Return structured result
PART 2 — EXISTING SYSTEM
Q8 ⭐ What is the existing system?
🎓 Viva Answer

The existing workflow generally depends on manual examination of patient records, individual X-ray review, clinician experience, separate laboratory and symptom analysis, manual historical case searching and external consultation or referral.

🧑‍💻 Beginner Explanation

Today, information may be separated:

X-ray → one place
Lab → another
History → another
Previous diagnosis → another
Hospital information → internet

The doctor has to combine these manually.

Q9 ⭐ What are the disadvantages of the existing system?
🎓 Viva Answer

The main disadvantages are:

Time-consuming manual search.
Fragmented medical information.
Manual X-ray comparison.
Difficult historical case retrieval.
Lack of integrated multimodal analysis.
Dependence on individual clinical experience.
Difficulty presenting current and historical information together.
🧑‍💻 Beginner Explanation

The biggest issue is:

Too much manual work and fragmented information.

Q10 Why can't doctors simply search Google or PubMed?
🎓 Viva Answer

General search engines and literature databases are useful resources, but they do not automatically perform multimodal comparison between the current patient's X-ray, clinical information and historical cases. CaseTwin focuses on integrating image similarity with clinical case information and referral support within one workflow.

🧑‍💻 Beginner Explanation

Google/PubMed can help find information.

But they don't naturally do:

Your X-ray
+
Your symptoms
+
Old X-rays
+
Old outcomes
+
Hospital routing

inside one clinical workflow.

PART 3 — PROPOSED SYSTEM
Q11 ⭐ What is your proposed system?
🎓 Viva Answer

Our proposed system, CaseTwin, combines multimodal clinical information processing, medical image similarity retrieval, historical case comparison, specialist routing and referral generation into a single clinical decision-support workflow.

🧑‍💻 Beginner Explanation

Your proposed system is basically:

INPUT
 ↓
AI ANALYSIS
 ↓
SIMILAR CASES
 ↓
COMPARISON
 ↓
SPECIALIST ROUTING
 ↓
DOCTOR REVIEW
 ↓
REFERRAL
Q12 ⭐ What are the major modules?
🎓 Viva Answer

The current core system contains:

Case upload.
Clinical information extraction.
Similar case retrieval.
X-ray comparison.
Clinical case comparison.
Clinical Q&A.
Hospital routing.
Physician discovery.
Referral memo generation.

Planned extensions include health-risk screening, vital monitoring, lab analysis, medication intelligence, patient timelines and FHIR-based records.

🧑‍💻 Beginner Explanation

Your project has a core and an expanded version.

Core:

X-ray → Similar Cases → Referral

Expanded:

Complete Patient Health Platform
PART 4 — MEDGEMMA
Q13 ⭐ What is MedGemma?
🎓 Viva Answer

MedGemma is a medical AI model from Google's Health AI Developer Foundations collection designed for medical text and multimodal healthcare tasks. In CaseTwin, we use it for clinical information extraction, medical image analysis, case comparison, clinical question answering and medical term explanation.

🧑‍💻 Beginner Explanation

Think of MedGemma as the medical reasoning component.

It understands:

Medical text
+
Medical images

and helps generate structured clinical information.

Q14 ⭐ Why did you choose MedGemma?
🎓 Viva Answer

The project requires medical-domain reasoning rather than only general language understanding. MedGemma is specifically designed for healthcare-related multimodal tasks, making it suitable for clinical text and medical imaging workflows.

🧑‍💻 Beginner Explanation

A normal chatbot is trained for general conversations.

Your project needs:

Medical terminology
+
Clinical notes
+
Medical images

Therefore, a medical-focused model is more appropriate for the clinical reasoning component.

Q15 What are you using MedGemma for?
🎓 Viva Answer

We use MedGemma for:

Clinical note extraction.
Multimodal X-ray comparison.
Abnormality localization.
Clinical synthesis.
Dual-context clinical Q&A.
Medical term explanation.
🧑‍💻 Beginner Explanation

MedGemma performs several jobs.

For example:

Doctor's notes
 ↓
MedGemma
 ↓
Patient profile

or:

Current X-ray + Historical X-ray
 ↓
MedGemma
 ↓
Comparison
Q16 ⭐ Is MedGemma giving the final diagnosis?
🎓 Viva Answer

No. CaseTwin is a clinical decision-support system and not an autonomous diagnostic system. MedGemma generates supporting analysis and recommendations. The clinician reviews the information and makes the final clinical decision.

🧑‍💻 Beginner Explanation

Very important:

AI → Suggestion
Doctor → Decision

Not:

AI → Diagnosis → Treatment
PART 5 — MEDSIGLIP
Q17 ⭐ What is MedSigLIP?
🎓 Viva Answer

MedSigLIP is a medical vision-language model whose image encoder can generate representations or embeddings for medical images. CaseTwin uses those image embeddings for chest X-ray similarity retrieval.

🧑‍💻 Beginner Explanation

MedSigLIP converts an X-ray into numbers.

Example:

X-ray
 ↓
MedSigLIP
 ↓
[0.12, 0.42, 0.87, 0.21, ...]

These numbers represent features of the image.

Q18 ⭐ What is an embedding?
🎓 Viva Answer

An embedding is a numerical vector representation of an input such as an image or text. Similar inputs tend to have similar vector representations, which allows us to perform similarity search efficiently.

🧑‍💻 Beginner Explanation

Suppose:

X-ray A → [0.1, 0.8, 0.3]
X-ray B → [0.1, 0.7, 0.3]
X-ray C → [0.9, 0.1, 0.8]

A and B are mathematically closer.

Therefore:

A ≈ B
Q19 ⭐ Why do you need embeddings?
🎓 Viva Answer

We cannot efficiently compare every new X-ray directly against a large historical image collection using raw images. Embeddings convert images into numerical vectors, allowing efficient similarity search using a vector database.

🧑‍💻 Beginner Explanation

Without embeddings:

New X-ray
 ↓
Compare raw image against thousands of images

With embeddings:

New X-ray
 ↓
Vector
 ↓
Search vector database
 ↓
Top similar cases
PART 6 — QDRANT
Q20 ⭐ What is Qdrant?
🎓 Viva Answer

Qdrant is a vector database used to store and retrieve high-dimensional embeddings efficiently. In CaseTwin, historical chest X-ray embeddings are stored in Qdrant and searched using similarity metrics.

🧑‍💻 Beginner Explanation

Think of Qdrant as:

Google Search, but for vectors.

Instead of searching:

"lung disease"

you search using:

[0.12, 0.45, 0.78, ...]
Q21 ⭐ Why not use MySQL or PostgreSQL for similarity search?
🎓 Viva Answer

Traditional relational databases are excellent for structured records, but vector databases are specifically optimized for nearest-neighbor searches over high-dimensional embeddings. Qdrant is therefore more appropriate for our image similarity retrieval component.

🧑‍💻 Beginner Explanation

SQL database:

Patient ID
Name
Age
Diagnosis

Vector database:

X-ray embedding
      ↓
Find nearest embeddings

You can eventually use both:

PostgreSQL → patient records
Qdrant → image embeddings
Q22 ⭐ What similarity algorithm are you using?
🎓 Viva Answer

We use cosine similarity to compare the medical image embeddings.

🧑‍💻 Beginner Explanation

Cosine similarity checks how close the direction of two vectors is.

Conceptually:

Same direction → high similarity
Different direction → low similarity
Q23 Does 94% similarity mean the patient has the same disease with 94% probability?
🎓 Viva Answer

No. Similarity score and disease probability are different concepts. A similarity score indicates how close the representation of two cases is according to the retrieval model. It should not be interpreted as diagnostic probability.

🧑‍💻 Beginner Explanation

Very important.

94% similarity

does not mean:

94% chance of disease

It only means:

The retrieved case is highly similar according to the embedding similarity measure.

PART 7 — COMPLETE RETRIEVAL PIPELINE
Q24 ⭐ Explain your similar-case retrieval process.
🎓 Viva Answer

First, the clinician uploads a chest X-ray. The image is passed to MedSigLIP to generate a medical image embedding. The embedding is then sent to Qdrant, where it is compared with stored historical case embeddings using cosine similarity. The system retrieves the top-ranked historical cases and presents them to the clinician.

🧑‍💻 Beginner Explanation

Remember this:

X-ray
 ↓
MedSigLIP
 ↓
Embedding
 ↓
Qdrant
 ↓
Cosine Similarity
 ↓
Top-K Cases

That's one of your most important technical pipelines.

Q25 What is Top-K retrieval?
🎓 Viva Answer

Top-K retrieval means returning the K most similar cases according to the selected similarity metric. For example, if K is 5, the system returns the five most similar historical cases.

🧑‍💻 Beginner Explanation

If there are 10,000 historical cases:

10,000 cases
      ↓
Similarity search
      ↓
Top 5

You don't show all 10,000 to the doctor.

PART 8 — MEDGEMMA COMPARISON
Q26 ⭐ How do you compare the current X-ray and historical X-ray?
🎓 Viva Answer

After a historical twin case is selected, the current and historical X-rays are provided to the multimodal analysis component. MedGemma generates a structured comparison covering relevant similarities, differences and imaging findings. It can also return coordinates for selected findings, which are rendered as visual overlays.

🧑‍💻 Beginner Explanation

You have:

Current X-ray       Historical X-ray
      │                    │
      └────────┬───────────┘
               ↓
           MedGemma
               ↓
       Similarities
       Differences
       Findings
Q27 What is bounding-box localization?
🎓 Viva Answer

Bounding-box localization identifies a region of interest in an image using coordinates such as x, y, width and height. CaseTwin can use these coordinates to render visual overlays around selected findings.

🧑‍💻 Beginner Explanation

Imagine the X-ray is:

┌──────────────────────┐
│                      │
│       ┌──────┐       │
│       │Finding│      │
│       └──────┘       │
│                      │
└──────────────────────┘

The AI provides the coordinates of that rectangle.

Your frontend then draws the box.

Q28 Why is visual comparison useful?
🎓 Viva Answer

Visual comparison allows clinicians to inspect the regions considered relevant by the model instead of relying only on textual descriptions. This improves interpretability of the comparison workflow.

🧑‍💻 Beginner Explanation

Instead of AI saying:

“There is an abnormality.”

You can show:

Where the AI is referring to.

PART 9 — CLINICAL INFORMATION
Q29 ⭐ What is a CaseProfile?
🎓 Viva Answer

A CaseProfile is a structured representation of the patient's relevant clinical information. It can contain demographics, symptoms, vitals, findings, diagnoses, assessment and plan.

🧑‍💻 Beginner Explanation

Instead of storing:

"Patient has cough and fever..."

you convert it into:

Age: 45
Symptoms: cough, fever
Duration: 5 days
Finding: ...
Diagnosis: ...

This makes information easier for software to process.

Q30 Why do you convert unstructured clinical notes into structured information?
🎓 Viva Answer

Structured information is easier to search, compare, validate and pass between different system components. It also allows clinical information from different cases to be compared using consistent fields.

🧑‍💻 Beginner Explanation

Unstructured:

“Patient has been experiencing cough for five days with mild fever...”

Structured:

Symptom = Cough
Duration = 5 days
Symptom = Fever
Severity = Mild

Computers can work with the second form more easily.

PART 10 — AGENTIC COPILOT
Q31 What is the Agentic Copilot?
🎓 Viva Answer

The Agentic Copilot allows the clinician to provide patient information through natural-language interaction. Gemini progressively converts this information into a structured CaseProfile.

🧑‍💻 Beginner Explanation

Doctor can type:

“Patient is 45 years old and has cough for five days.”

Instead of filling ten forms manually, the AI extracts the information.

Q32 Why are you using Gemini instead of MedGemma for the Copilot?
🎓 Viva Answer

The Copilot primarily performs general conversational information collection and structured case construction. Gemini is used for this general agentic task, while MedGemma is reserved for medical-domain multimodal reasoning and medical information processing.

🧑‍💻 Beginner Explanation

Think:

Gemini → General assistant
MedGemma → Medical specialist
PART 11 — HOSPITAL ROUTING
Q33 ⭐ How does hospital routing work?
🎓 Viva Answer

The system receives clinical requirements, location and routing criteria. It searches for candidate hospitals, enriches and cleans the results, determines geographic coordinates, calculates travel estimates and presents suitable facilities to the clinician.

🧑‍💻 Beginner Explanation

The system asks:

What specialty?
Where is patient?
What hospital capabilities are needed?
How far can patient travel?

Then:

Search hospitals
 ↓
Find coordinates
 ↓
Calculate distance/travel time
 ↓
Show results on map
Q34 What is the role of You.com?
🎓 Viva Answer

You.com is used as a web-search and retrieval component for discovering relevant hospital information and supporting live information retrieval.

🧑‍💻 Beginner Explanation

It helps CaseTwin search the web for current hospital information.

Q35 What happens if the hospital search fails?
🎓 Viva Answer

The system includes fallback mechanisms. It can retry with a simplified search query, and where the primary search service is unavailable, a Gemini-based fallback can generate candidate facilities for further processing.

🧑‍💻 Beginner Explanation

Instead of:

API fails → whole system fails

you try:

Search
 ↓
Retry
 ↓
Fallback
Q36 ⭐ What is CrewAI doing?
🎓 Viva Answer

CrewAI orchestrates specialized AI agents for physician discovery. One agent performs medical and hospital research, while another agent extracts and structures the relevant physician information.

🧑‍💻 Beginner Explanation

Two AI workers:

Agent 1
Researcher
 ↓
Find information

Agent 2
Extractor
 ↓
Convert information to structured data
Q37 Why use two agents instead of one?
🎓 Viva Answer

Separating research and extraction reduces task complexity and makes the workflow easier to control and validate. The researcher focuses on finding evidence, while the extractor focuses on producing structured output.

🧑‍💻 Beginner Explanation

One person:

Search + analyze + format everything.

Two people:

Person 1 → Research
Person 2 → Organize

Specialization makes the workflow easier to manage.

PART 12 — REFERRAL
Q38 ⭐ How is the referral memo generated?
🎓 Viva Answer

The referral memo combines structured information generated during the previous stages, including the patient's summary, imaging findings, relevant historical case information and selected referral destination. It then produces a structured document that can be reviewed and printed by the clinician.

🧑‍💻 Beginner Explanation

The system collects everything:

Patient
+
X-ray
+
Similar case
+
Clinical findings
+
Hospital

and puts it into one referral document.

Q39 Why is referral generation useful?
🎓 Viva Answer

It reduces repetitive documentation and ensures that important information gathered during the workflow can be transferred into a structured referral format for clinician review.

🧑‍💻 Beginner Explanation

Instead of typing the same information again:

CaseTwin already has it
        ↓
Referral document
PART 13 — DOCTOR-IN-THE-LOOP
Q40 ⭐ Why do you need a doctor-in-the-loop?
🎓 Viva Answer

Healthcare decisions are high-impact decisions. AI outputs may contain errors or uncertainty, so CaseTwin is designed to provide recommendations and supporting evidence while keeping the clinician responsible for the final decision.

🧑‍💻 Beginner Explanation

AI can make mistakes.

Therefore:

AI → Helps
Doctor → Decides
Q41 What happens when the doctor disagrees with AI?
🎓 Viva Answer

The doctor should be able to modify or reject the recommendation. The decision can also be stored as feedback for later system evaluation and improvement.

🧑‍💻 Beginner Explanation

Example:

AI: Pulmonology

Doctor:
❌ Reject

Doctor selects:
Cardiology

The doctor's decision becomes useful evaluation data.

PART 14 — FUTURE FEATURES
Q42 ⭐ What future features are you planning?
🎓 Viva Answer

We plan to expand CaseTwin with AI-assisted health risk screening, vital-sign monitoring, longitudinal health trend analysis, laboratory report analysis, medication intelligence, symptom intelligence, emergency red-flag detection, personal health records, doctor dashboards, patient timelines, appointment management and FHIR-based healthcare interoperability.

🧑‍💻 Beginner Explanation

Currently:

Chest Case → Similar Cases → Referral

Future:

Complete Patient Health Record
        ↓
X-rays
Labs
Vitals
Medications
Symptoms
Timeline
Appointments
Referrals
Q43 What is the Health Trend Analyzer?
🎓 Viva Answer

It analyzes repeated measurements over time to identify meaningful changes or trends rather than evaluating a value from only a single visit.

🧑‍💻 Beginner Explanation

One SpO₂ value:

96%

doesn't tell much about a trend.

But:

97 → 96 → 95 → 94 → 93

shows a downward trend that should be brought to clinical attention.

Q44 What is the Personal Health Record?
🎓 Viva Answer

It is a unified patient profile containing medical history, imaging, laboratory results, medications, vitals, diagnoses, referrals and other relevant healthcare information.

🧑‍💻 Beginner Explanation

Think of it as:

One digital folder containing the patient's healthcare history.

Q45 What is FHIR?
🎓 Viva Answer

FHIR, or Fast Healthcare Interoperability Resources, is a healthcare interoperability standard for representing and exchanging healthcare information using standardized resources.

🧑‍💻 Beginner Explanation

Imagine Hospital A uses one software and Hospital B uses another.

FHIR helps them communicate using common healthcare data structures.

For example:

Patient
Observation
DiagnosticReport
MedicationRequest
ImagingStudy
Condition
ServiceRequest
Q46 Why do you want to use FHIR?
🎓 Viva Answer

FHIR can make the system more interoperable with healthcare information systems and provide standardized representations for patient, observation, diagnostic, medication and referral data.

🧑‍💻 Beginner Explanation

Without a standard:

Hospital A → Format A
Hospital B → Format B

FHIR provides a common structure.

PART 15 — LAB ANALYSIS
Q47 ⭐ How will your Lab Report Analyzer work?
🎓 Viva Answer

A laboratory report can be uploaded as an image or document. The system extracts the relevant laboratory values, maps them to structured fields, compares them against appropriate reference ranges and highlights potentially unusual values for clinician review.

🧑‍💻 Beginner Explanation

Example:

Uploaded CBC
 ↓
Extract:
Hemoglobin = 10.2
WBC = ...
Platelets = ...
 ↓
Compare with reference range
 ↓
Highlight unusual values

It should not automatically diagnose the patient.

Q48 Can AI diagnose disease from a laboratory report?
🎓 Viva Answer

Our system is intended to support interpretation and organization of laboratory information rather than autonomously diagnose disease. Any clinical interpretation should be reviewed by a qualified healthcare professional.

🧑‍💻 Beginner Explanation

The system can say:

“This value is outside the configured reference range.”

It shouldn't independently say:

“You definitely have disease X.”

PART 16 — VITAL MONITORING
Q49 What vitals will you monitor?
🎓 Viva Answer

The planned system can track heart rate, SpO₂, blood pressure, temperature and respiratory rate.

🧑‍💻 Beginner Explanation

These are common measurements that can be stored repeatedly.

Monday
Tuesday
Wednesday
Thursday

Then the system can show a graph.

Q50 Why is longitudinal monitoring important?
🎓 Viva Answer

A single measurement provides only a snapshot, whereas repeated measurements allow the system to identify changes and trends over time.

🧑‍💻 Beginner Explanation

One photo:

Snapshot.

Many photos:

Story.

Healthcare is often about understanding that story over time.

PART 17 — EMERGENCY RED FLAGS
Q51 ⭐ What is emergency red-flag detection?
🎓 Viva Answer

It is a safety-oriented module that checks predefined warning patterns in symptoms and vital signs and provides an escalation warning when those patterns are detected. It is intended for triage support and not autonomous diagnosis.

🧑‍💻 Beginner Explanation

Suppose the system sees a predefined combination of concerning information.

It can display:

⚠️ Potential red-flag indicators detected. Immediate medical evaluation may be appropriate.

The AI isn't declaring a diagnosis.

PART 18 — SECURITY
Q52 ⭐ How will you protect patient data?
🎓 Viva Answer

For a production healthcare deployment, we would use HTTPS, authentication and authorization, role-based access control, encrypted storage, secure secret management, audit logging, controlled access to patient records and appropriate data-retention policies. Sensitive information sent to external services should also be minimized or de-identified where appropriate.

🧑‍💻 Beginner Explanation

Healthcare data is sensitive.

So:

Who can see data?
Who can edit?
Where is data stored?
Is it encrypted?
Are API keys protected?
Can we track access?

must all be controlled.

Q53 Where are your API keys stored?
🎓 Viva Answer

API keys should be stored as environment variables or, preferably in production, in a secure secret-management system. They should never be hard-coded into the frontend or committed to the repository.

🧑‍💻 Beginner Explanation

Never do:

const API_KEY = "my-secret-key";

in GitHub.

Instead:

Environment variable
        ↓
Backend
        ↓
API
PART 19 — DEPLOYMENT
Q54 ⭐ How will you deploy your project?
🎓 Viva Answer

We use Docker to containerize the application. The React frontend is built and served using Nginx, while the FastAPI backend runs separately. Both services can be deployed on Google Cloud Run. The medical AI models are accessed through Hugging Face inference endpoints, while Qdrant provides vector search.

🧑‍💻 Beginner Explanation

Think of your project as two applications:

Frontend
React + Nginx
        ↓
Cloud Run

Backend
FastAPI
        ↓
Cloud Run

They communicate using APIs.

Q55 ⭐ Why Cloud Run?
🎓 Viva Answer

Cloud Run allows us to deploy containerized services without managing traditional servers. It can automatically scale services according to incoming requests and integrates well with container-based deployments.

🧑‍💻 Beginner Explanation

Instead of buying and managing a server:

Build Docker container
        ↓
Upload to Cloud Run
        ↓
Google runs it
Q56 Why Docker?
🎓 Viva Answer

Docker provides a consistent environment for development and deployment. It packages the application and its dependencies together, reducing environment-related deployment problems.

🧑‍💻 Beginner Explanation

Developer's computer:

Python version
Libraries
Node
System dependencies

may differ from server.

Docker packages the required environment.

Q57 ⭐ What deployment problems can you face?
🎓 Viva Answer

Potential challenges include model inference latency, Cloud Run cold starts, external API failures, request timeouts, memory and CPU requirements, network connectivity, API quota limits, secret management, CORS configuration and healthcare data security.

🧑‍💻 Beginner Explanation

Possible problems:

AI takes too long
API stops responding
Cloud Run starts slowly
External service fails
Wrong API key
Memory insufficient
CORS error
Q58 What is a Cloud Run cold start?
🎓 Viva Answer

A cold start occurs when Cloud Run needs to start a new container instance because there is no currently active instance available to handle the request.

🧑‍💻 Beginner Explanation

Imagine your server is sleeping.

User requests:

Request
 ↓
Start server
 ↓
Load application
 ↓
Answer

That startup delay is a cold start.

Q59 How can you reduce cold-start problems?
🎓 Viva Answer

We can optimize container startup, reduce unnecessary dependencies, use appropriate resource allocation and, where required for latency-sensitive production workloads, configure minimum instances.

🧑‍💻 Beginner Explanation

Instead of starting from zero every time:

Keep one instance ready

But that increases cost.

PART 20 — ARCHITECTURE
Q60 ⭐ Explain your complete architecture.
🎓 Viva Answer

The frontend is developed using React and TypeScript. It communicates with a FastAPI backend through REST APIs. The backend handles medical AI inference, vector retrieval, clinical comparison and agentic workflows. MedSigLIP generates medical image embeddings which are stored and searched in Qdrant. MedGemma performs multimodal clinical reasoning. Gemini handles general agentic tasks. CrewAI orchestrates physician discovery agents. External services provide web search, geocoding and routing. The application can be containerized using Docker and deployed to Google Cloud Run.

🧑‍💻 Beginner Explanation

The complete flow:

                    USER
                     ↓
              React Frontend
                     ↓
              FastAPI Backend
                     ↓
       ┌─────────────┼─────────────┐
       ↓             ↓             ↓
   MedSigLIP      MedGemma      Gemini
       ↓             ↓             ↓
    Qdrant       Clinical AI   Agents
       │             │             │
       └─────────────┼─────────────┘
                     ↓
              CaseTwin Result
                     ↓
                 Doctor
PART 21 — API QUESTIONS
Q61 What is an API?
🎓 Viva Answer

An API, or Application Programming Interface, allows different software components to communicate with each other through defined requests and responses.

🧑‍💻 Beginner Explanation

Frontend asks:

Give me similar cases.

Backend:

POST /search

Backend processes it and sends the result back.

Q62 Why FastAPI instead of directly calling AI models from React?
🎓 Viva Answer

Sensitive credentials and business logic should remain on the backend. The backend also provides a controlled layer for validation, orchestration, model calls, database access and security.

🧑‍💻 Beginner Explanation

Don't do:

React
 ↓
Secret API key
 ↓
AI

Instead:

React
 ↓
FastAPI
 ↓
AI

The backend protects secrets and controls the workflow.

Q63 Why do you need separate frontend and backend?
🎓 Viva Answer

Separation of frontend and backend improves modularity, security, maintainability and scalability. The frontend handles presentation and user interaction, while the backend handles business logic, AI inference, data processing and external integrations.

🧑‍💻 Beginner Explanation

Frontend:

What the user sees.

Backend:

What happens behind the screen.

PART 22 — DATABASE
Q64 Where will patient information be stored?
🎓 Viva Answer

The architecture can use a structured database for patient and clinical records, while Qdrant is specifically used for vector embeddings and similarity retrieval. The exact production database layer can be selected based on deployment and interoperability requirements.

🧑‍💻 Beginner Explanation

You need different kinds of storage.

Patient data → Structured database

X-ray embeddings → Qdrant

Images/documents → Object storage
Q65 Why can't Qdrant store everything?
🎓 Viva Answer

Qdrant is primarily designed for vector similarity search. It can store payload metadata, but it should not be treated as a complete transactional healthcare database. Structured patient records, permissions and transactional workflows are better handled by an appropriate relational or healthcare data store.

🧑‍💻 Beginner Explanation

Qdrant's main job:

Find similar vectors.

It shouldn't become your entire hospital database.

PART 23 — LITERATURE SURVEY
Q66 ⭐ What did you learn from your literature survey?
🎓 Viva Answer

The literature indicates that AI can assist chest X-ray analysis, medical image retrieval can support case comparison, multimodal information can improve similarity retrieval, medical foundation models can support healthcare tasks, and healthcare AI systems require strong attention to privacy, security and explainability.

🧑‍💻 Beginner Explanation

Your papers collectively tell you:

AI can analyze X-rays
        +
Similar cases are useful
        +
Images alone aren't enough
        +
Clinical text matters
        +
Healthcare AI needs safety

That led to CaseTwin.

Q67 ⭐ What is the research gap?
🎓 Viva Answer

Existing approaches often focus on individual tasks such as disease classification, image retrieval or clinical question answering. Our project attempts to integrate multimodal case retrieval, clinical comparison, specialist routing and referral support into a single clinician-centered workflow.

🧑‍💻 Beginner Explanation

Existing projects may do:

Project A → X-ray classification
Project B → Image retrieval
Project C → Chatbot
Project D → Hospital search

Your idea is:

A + B + C + D
       ↓
CaseTwin workflow
PART 24 — PERFORMANCE
Q68 How will you evaluate your system?
🎓 Viva Answer

Different components require different evaluation metrics. For image retrieval we can evaluate Top-K retrieval quality using metrics such as precision@K or recall@K. For information extraction we can compare extracted fields against ground-truth annotations. For structured outputs we can evaluate field-level accuracy. For system performance we can measure latency, failure rate and successful workflow completion.

🧑‍💻 Beginner Explanation

Don't use one score for everything.

Image Retrieval
→ Precision@K / Recall@K

Information Extraction
→ Accuracy / F1

System
→ Response time

Agents
→ Valid structured outputs
Q69 What is Precision@K?
🎓 Viva Answer

Precision@K measures how many of the top K retrieved results are relevant to the query.

🧑‍💻 Beginner Explanation

Suppose you retrieve 5 cases:

Case 1 → Relevant
Case 2 → Relevant
Case 3 → Not relevant
Case 4 → Relevant
Case 5 → Not relevant

Then:

Relevant = 3
Retrieved = 5

Precision@5 = 3/5 = 60%
Q70 What is Recall?
🎓 Viva Answer

Recall measures how much of the relevant information or relevant cases available in the evaluation set were successfully retrieved.

🧑‍💻 Beginner Explanation

Precision asks:

“Of what I found, how much was correct?”

Recall asks:

“Of everything relevant, how much did I find?”

PART 25 — LIMITATIONS
Q71 ⭐ What are the limitations of your project?
🎓 Viva Answer

The major limitations include dependence on external model and search services, possible hallucination or extraction errors, limitations in the historical dataset, differences between research datasets and real clinical populations, inference latency, and the need for extensive clinical validation before real-world deployment.

🧑‍💻 Beginner Explanation

Your project is a prototype.

It doesn't automatically mean:

“This is ready for a hospital.”

You need:

More data
More testing
Clinical validation
Security testing
Privacy controls
Regulatory evaluation
Q72 What happens if the historical case is not actually similar?
🎓 Viva Answer

Similarity retrieval is treated as supporting evidence rather than a definitive clinical conclusion. The retrieved cases should be reviewed by the clinician, and the system should expose the basis and limitations of the retrieval rather than treating the result as a diagnosis.

🧑‍💻 Beginner Explanation

AI can find a case that looks similar but isn't actually medically equivalent.

So:

Similar Case
≠
Same Disease
PART 26 — SAFETY
Q73 ⭐ Is your system safe for medical use?
🎓 Viva Answer

The current system is a research and academic prototype. It is not being presented as an autonomous medical diagnostic system. Real clinical deployment would require clinical validation, privacy and security controls, regulatory assessment, monitoring and integration with hospital workflows.

🧑‍💻 Beginner Explanation

Your project can demonstrate:

Technical feasibility.

But real hospital deployment needs much more validation.

Q74 What happens if MedGemma gives an incorrect answer?
🎓 Viva Answer

The system treats model output as decision-support information rather than ground truth. The clinician reviews the output, and future versions can incorporate confidence indicators, source grounding, structured validation and doctor feedback mechanisms.

🧑‍💻 Beginner Explanation

AI isn't always correct.

Therefore:

AI result
 ↓
Doctor checks
 ↓
Accept / Modify / Reject
PART 27 — VERY TRICKY GUIDE QUESTIONS
Q75 ⭐ “Why is your project AI and not just a normal web application?”
🎓 Viva Answer

The application uses AI models for medical image representation, clinical information extraction, multimodal comparison and agentic information retrieval. The web application acts as the interface and orchestration layer for these AI capabilities.

🧑‍💻 Beginner Explanation

Website alone:

Forms + Database

Your project:

Website
+
Medical AI
+
Vector Search
+
Agents
+
Clinical Workflow
Q76 ⭐ “Why don't you just use ChatGPT?”
🎓 Viva Answer

A general-purpose language model alone is not sufficient for the complete workflow. CaseTwin requires medical image embeddings for similarity search, specialized medical multimodal reasoning, vector retrieval and structured agentic workflows. Therefore, we use specialized components for different tasks.

🧑‍💻 Beginner Explanation

Chatbot ≠ complete system.

You need:

Image Encoder
+
Medical Model
+
Vector DB
+
Agents
+
Backend
+
Frontend
Q77 ⭐ “What is the biggest innovation in your project?”
🎓 Viva Answer

The key innovation is not a single model but the integration of multimodal medical image retrieval, historical case comparison, agentic specialist routing and clinician review into one continuous workflow.

🧑‍💻 Beginner Explanation

Don't say:

“Our innovation is MedGemma.”

Instead:

“Our innovation is how we combine the technologies into one workflow.”

Q78 ⭐ “What happens from the moment the doctor uploads an X-ray?”
🎓 Viva Answer

The X-ray is received by the backend, processed through MedSigLIP to generate an embedding, and searched against historical embeddings in Qdrant. The top similar cases are returned. The clinician can select a case for deeper comparison, where MedGemma analyzes the current and historical images and generates structured insights. The workflow can then continue to specialist and hospital routing and referral generation.

🧑‍💻 Beginner Explanation

Memorize:

Upload
 ↓
Embedding
 ↓
Qdrant
 ↓
Similar Cases
 ↓
Select Twin
 ↓
MedGemma Comparison
 ↓
Hospital
 ↓
Referral
Q79 ⭐ “Why do you call it a Clinical Decision Support System?”
🎓 Viva Answer

Because the system does not make the final clinical decision. It collects and analyzes relevant information, retrieves historical evidence, presents recommendations and assists the clinician in making an informed decision.

🧑‍💻 Beginner Explanation

CDSS means:

Computer helps doctor decide.

Not:

Computer decides instead of doctor.

Q80 ⭐ “What is the difference between diagnosis and decision support?”
🎓 Viva Answer

Diagnosis attempts to identify a medical condition, whereas decision support provides relevant information, evidence, analysis or recommendations that can assist a healthcare professional in making a clinical decision.

🧑‍💻 Beginner Explanation

Diagnosis:

“What disease does the patient have?”

Decision support:

“Here is relevant information that may help the doctor decide what to investigate or do next.”

PART 28 — QUESTIONS ABOUT YOUR FUTURE SYSTEM
Q81 How will all your new features connect to CaseTwin?
🎓 Viva Answer

The current CaseTwin workflow will remain the core clinical intelligence layer. The additional modules will contribute structured patient information to the same patient profile and timeline. For example, laboratory values, vitals, medication history and symptoms can become additional inputs to the clinical analysis and longitudinal comparison components.

🧑‍💻 Beginner Explanation

Don't make 15 separate applications.

Make:

                    Patient
                       │
       ┌───────────────┼───────────────┐
       ↓               ↓               ↓
     X-ray            Labs           Vitals
       ↓               ↓               ↓
       └────────── CaseTwin ───────────┘
                       │
                       ↓
                Patient Timeline
Q82 ⭐ Which features will you implement first?
🎓 Viva Answer

We will prioritize the core CaseTwin workflow first: clinical case input, chest X-ray processing, similar-case retrieval, multimodal comparison, specialist routing and referral generation. After validating the core workflow, we plan to incrementally add laboratory analysis, vitals, longitudinal trends, medication intelligence, patient records and FHIR interoperability.

🧑‍💻 Beginner Explanation

Don't try to build everything simultaneously.

First:
X-ray
 ↓
Similar Cases
 ↓
Comparison
 ↓
Referral
Then:
Labs
Vitals
Medications
Timeline
FHIR
Q83 ⭐ If your guide says “This is too big. How will you complete it?”
🎓 Viva Answer

We have divided the project into a core implementation and incremental modules. The core system is limited to the clinically meaningful workflow of multimodal case retrieval, comparison and referral. Additional features are modular extensions that can be implemented and evaluated independently.

🧑‍💻 Beginner Explanation

This answer is important.

You're saying:

We aren't building everything at once.

You have:

CORE
CaseTwin

EXTENSIONS
Labs
Vitals
Medication
FHIR
Timeline
PART 29 — FINAL 15 QUESTIONS YOU MUST MEMORIZE

If you have very little time before the review, memorize these first:

1.

What is CaseTwin?

A multimodal agentic clinical decision-support system for historical case retrieval, comparison and specialist referral.

2.

What problem does it solve?

Fragmented and time-consuming retrieval and comparison of relevant clinical cases.

3.

What is multimodal?

Processing multiple data types such as X-rays, text, symptoms and laboratory information.

4.

Why MedGemma?

Medical multimodal reasoning and clinical information processing.

5.

Why MedSigLIP?

Medical image embeddings and similarity retrieval.

6.

Why Qdrant?

Efficient vector similarity search.

7.

What is an embedding?

A numerical representation of information used for similarity comparison.

8.

How do you retrieve similar cases?

X-ray → MedSigLIP → embedding → Qdrant → cosine similarity → Top-K cases.

9.

What is agentic AI?

AI that performs a sequence of tasks toward a goal, rather than simply returning one response.

10.

What is CrewAI doing?

Orchestrating specialized research and extraction agents for physician discovery.

11.

Is this an autonomous diagnostic system?

No. It is a clinical decision-support system with clinician oversight.

12.

Why doctor-in-the-loop?

To ensure AI recommendations are reviewed by a qualified clinician before final decisions.

13.

How is it deployed?

Dockerized React frontend and FastAPI backend deployed on Cloud Run, with external AI inference and vector-search services.

14.

What is the main innovation?

Integration of medical image retrieval, multimodal comparison, agentic specialist routing and referral into one clinician-centered workflow.

15.

What is the future scope?

Longitudinal patient records, vitals, laboratory analysis, medication intelligence, health timelines, doctor dashboards and FHIR interoperability.


If your guide suddenly asks:

“Explain your entire project from beginning to end.”

Say this:

“A clinician uploads a chest X-ray and provides clinical information. MedSigLIP converts the X-ray into a medical embedding, which is searched against historical case embeddings stored in Qdrant using cosine similarity. The system retrieves the most similar historical cases. The clinician selects a relevant case, and MedGemma performs multimodal comparison between the current and historical X-rays and their clinical context. The system can then assist in identifying suitable hospitals and specialists using agentic web research, geographic routing and capability-based filtering. Finally, all relevant information is assembled into a structured referral memo. Throughout the workflow, CaseTwin acts as a decision-support system, while the clinician reviews and makes the final decision.”




