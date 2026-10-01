
2. WHAT EXACTLY ARE YOU BUILDING?

Your project can be explained as 5 major layers.

Layer 1 — Patient Data

The system accepts:

Chest X-ray
Clinical notes
Symptoms
Vitals
Laboratory reports
Previous diagnosis
Medication history
Medical history
Layer 2 — Medical AI

You use different AI models for different tasks.

MedSigLIP

Used for:

Chest X-ray image embedding and similarity retrieval

X-ray
 ↓
MedSigLIP
 ↓
512-dimensional embedding
 ↓
Qdrant
 ↓
Similar historical X-rays
MedGemma

Used for:

Clinical note extraction
Medical image analysis
X-ray comparison
Clinical Q&A
Medical terminology explanation
Clinical synthesis
Gemini

Used for:

Agentic case construction
General reasoning
Hospital information enrichment
Fallback processing

This distinction is important if your guide asks:

“Why are you using three different models?”

Answer:

“We are following a task-specific architecture. MedSigLIP is optimized for medical image representation and similarity search, MedGemma is used for multimodal clinical reasoning, while Gemini is used for general agentic tasks such as structured information collection and web-based hospital information processing.”
