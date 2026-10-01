# CASETWIN / MEDMIND AI

## Project Zeroth Review — Top 20 Questions & Answers

### 1. What is the title of your project?

**Answer to Guide:**
Our project title is **“A Multimodal Agentic Clinical Decision Support System for Similar Case Retrieval and Specialist Referral.”**
The system is called **CaseTwin / MedMind AI**.

**Beginner Explanation:**
Our project uses AI to understand **medical images like chest X-rays and clinical information**, find similar previous cases, and help identify suitable specialist hospitals for referral.

---

### 2. What is your project about?

**Answer to Guide:**
Our project is a **multimodal clinical decision support system**. It takes a patient's chest X-ray and clinical information, retrieves historically similar cases, compares the current case with the selected historical case, and helps identify suitable specialist facilities for referral.

**Beginner Explanation:**
Instead of a doctor manually searching many old medical records, our system helps bring **similar previous cases and useful clinical information together in one place**.

---

### 3. Why did you choose this project?

**Answer to Guide:**
We chose this project because finding relevant historical medical cases manually can be time-consuming, especially for rare or atypical presentations. We wanted to develop an AI-assisted system that can combine **medical images and clinical information** to make relevant historical evidence easier to retrieve and review.

**Beginner Explanation:**
Suppose a doctor sees an unusual chest X-ray. There may be an old patient with a similar case, but finding that case manually can take a lot of time. Our system tries to make that search faster.

---

### 4. What is the problem statement?

**Answer to Guide:**
The main problem is that historical clinical information is often distributed across different records and documents. Manual searching and comparing previous X-rays, symptoms, laboratory information, diagnoses, and treatments is time-consuming. Existing workflows also lack an integrated multimodal approach for retrieving and comparing similar cases.

**Beginner Explanation:**
The information exists, but it is scattered. The doctor may have to check **X-rays separately, reports separately, and previous records separately**. Our project brings these pieces together.

---

### 5. What is the existing system?

**Answer to Guide:**
The existing system mainly depends on manual examination of patient records, individual X-ray review, medical document searching, comparison of symptoms and laboratory results, and consultation with specialists when required.

**Beginner Explanation:**
Currently, much of the process depends on the **doctor manually reviewing information and using their experience**.

---

### 6. What are the disadvantages of the existing system?

**Answer to Guide:**
The major disadvantages are:

* Time-consuming historical search
* Fragmented medical information
* Difficult manual X-ray comparison
* Limited retrieval of relevant historical cases
* No integrated multimodal comparison
* Dependence on individual experience
* Difficulty in structured comparison of previous cases

**Beginner Explanation:**
The biggest issue is that the doctor has to do many things manually. Our project attempts to reduce the **information retrieval and comparison effort**, not replace the doctor.

---

### 7. What is your proposed system?

**Answer to Guide:**
Our proposed system, CaseTwin, combines **medical image understanding, clinical information extraction, similarity-based historical case retrieval, case comparison, and specialist referral support** into one workflow.

**Beginner Explanation:**
The basic flow is:

**Upload case → Understand information → Find similar cases → Compare cases → Find suitable specialist facility → Generate referral summary**

---

### 8. What are the main objectives of your project?

**Answer to Guide:**
Our main objectives are:

1. Process multimodal medical information.
2. Retrieve historically similar cases.
3. Compare current and historical chest X-rays.
4. Compare clinical information such as symptoms, laboratory results, diagnosis, treatment, and outcomes.
5. Provide structured evidence to assist clinical investigation and referral.

**Beginner Explanation:**
We want the system to understand **both the X-ray and the patient's medical information**, rather than depending only on an image.

---

### 9. What do you mean by “multimodal”?

**Answer to Guide:**
Multimodal means working with **multiple types of data**. In our project, the main modalities are medical images such as chest X-rays and clinical text such as symptoms, patient history, laboratory information, diagnosis, and treatment details.

**Beginner Explanation:**
“Multi” means many and “modal” refers to types of information.

For example:

**X-ray + symptoms + lab reports + medical history = multimodal data.**

---

### 10. What do you mean by “Agentic AI”?

**Answer to Guide:**
Agentic AI refers to AI systems that can perform a sequence of tasks toward a goal rather than simply generating a single response. In our project, agentic components help with tasks such as building a structured case profile, researching hospitals, finding physician information, enriching hospital data, and supporting referral preparation.

**Beginner Explanation:**
A normal chatbot mainly answers a question.

An agent can perform multiple steps:

**Search → collect information → analyze → filter → organize → produce result.**

That is why we use the term **agentic**.

---

### 11. Why did you choose chest X-rays?

**Answer to Guide:**
Chest X-rays are widely used in clinical practice for examining thoracic and respiratory conditions. They are also suitable for our project because medical image similarity can help retrieve historically comparable cases.

**Beginner Explanation:**
Chest X-rays contain important visual information about the lungs and chest. If two cases look similar, the previous case can provide useful historical context for review.

---

### 12. Are you trying to diagnose the patient?

**Answer to Guide:**
No. Our system is designed as a **clinical decision support system**, not an autonomous diagnostic system. It retrieves similar cases, provides comparisons, organizes clinical information, and supports referral. The final clinical decision remains with a qualified healthcare professional.

**Beginner Explanation:**
The AI is an **assistant**, not a doctor.

It can say:

> “These historical cases have similarities.”

But it should not independently say:

> “This patient definitely has this disease.”

The doctor makes the final decision.

---

### 13. What is similar case retrieval?

**Answer to Guide:**
Similar case retrieval is the process of finding historical medical cases that are similar to the current case based on available medical information. In our project, chest X-ray features are converted into embeddings and compared with historical case embeddings using vector similarity.

**Beginner Explanation:**
Imagine we have thousands of old cases. Instead of searching each one manually, the system finds the cases that are **closest to the current case**.

---

### 14. What is CBIR?

**Answer to Guide:**
CBIR stands for **Content-Based Image Retrieval**. It retrieves images based on their visual or learned features rather than relying only on filenames or manually assigned keywords.

Our project uses this concept for retrieving similar chest X-rays.

**Beginner Explanation:**
Instead of searching:

> “patient123.jpg”

the system looks at the **actual visual features of the X-ray** and finds images that are visually similar.

---

### 15. What is MedGemma and why are you using it?

**Answer to Guide:**
**MedGemma** is a medical-domain AI model designed for healthcare-related multimodal and language tasks. In our project, we use it for tasks such as clinical information extraction, medical image analysis, case comparison, clinical question answering, and medical term explanation.

**Beginner Explanation:**
MedGemma is like the **medical reasoning and understanding component** of our system.

It helps the system understand:

* Medical notes
* X-ray information
* Clinical questions
* Case comparisons
* Medical terminology

---

### 16. What is MedSigLIP and why are you using it?

**Answer to Guide:**
MedSigLIP is used as the **medical image encoder** in our system. It converts a chest X-ray into a numerical representation called an embedding. We then use these embeddings to perform similarity search against historical cases.

**Beginner Explanation:**
MedSigLIP converts an image into numbers that represent its learned visual features.

For example:

**X-ray → MedSigLIP → numerical embedding → similarity search**

---

### 17. What is an embedding?

**Answer to Guide:**
An embedding is a numerical representation of information that captures meaningful features in a mathematical vector space. In our project, a chest X-ray is converted into a **512-dimensional embedding** using MedSigLIP.

**Beginner Explanation:**
A computer cannot directly compare two X-ray images the way humans do.

So the model converts each image into numbers.

For example:

**X-ray A → [0.12, 0.81, 0.32, ...]**

**X-ray B → [0.14, 0.79, 0.35, ...]**

The system can mathematically compare these representations.

---

### 18. What is Qdrant and why are you using it?

**Answer to Guide:**
**Qdrant is a vector database** used to store and search embeddings efficiently. In our project, historical chest X-ray embeddings are stored in Qdrant, and when a new X-ray is uploaded, its embedding is compared against stored embeddings to retrieve similar cases.

**Beginner Explanation:**
A normal database is good for searching things like:

> Patient ID = 1023

A vector database is designed for searches like:

> “Find cases that are mathematically similar to this X-ray.”

---

### 19. What is the basic workflow of your project?

**Answer to Guide:**
The basic workflow is:

**Step 1:** Upload the current chest X-ray and clinical information.
**Step 2:** MedSigLIP generates the image embedding.
**Step 3:** Qdrant searches for similar historical cases.
**Step 4:** MedGemma extracts and analyzes clinical information.
**Step 5:** The user selects a relevant historical case.
**Step 6:** MedGemma compares the current and historical cases.
**Step 7:** The system searches and ranks suitable specialist facilities.
**Step 8:** A structured referral memo is generated.

**Beginner Explanation:**

Think of the entire project as:

**Patient Case**
↓
**AI understands the case**
↓
**Find similar old cases**
↓
**Compare current vs old case**
↓
**Find appropriate specialist facility**
↓
**Prepare referral summary**

---

### 20. What is the main novelty or contribution of your project?

**Answer to Guide:**
The main contribution is integrating **multimodal case understanding, medical image similarity retrieval, historical case comparison, agentic specialist facility discovery, and structured referral support** into a unified workflow.

Rather than using AI only for image analysis, our system connects the stages from **case understanding to similar-case retrieval and referral assistance**.

**Beginner Explanation:**
Many systems may perform only one task, such as:

**“Analyze this X-ray.”**

Our project tries to connect several tasks:

**Understand the case → Find similar cases → Compare them → Find specialist facilities → Prepare referral information.**

That complete workflow is the main idea behind CaseTwin.

---

## ⭐ One-Line Answer If Guide Says: “Explain Your Project in 30 Seconds”

**Answer:**

> “Our project, CaseTwin, is a multimodal agentic clinical decision support system that takes a patient's chest X-ray and clinical information, retrieves historically similar cases using MedSigLIP and Qdrant, uses MedGemma for clinical understanding and case comparison, and finally assists in identifying suitable specialist facilities and generating a structured referral summary. It is designed to support doctors, not replace their clinical decisions.”
