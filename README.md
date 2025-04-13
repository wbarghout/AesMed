# AesMed
A Context-Aware Post-Treatment Assistant for Aesthetic Medicine
# 🧠 AesMed: Context-Aware Assistant for Aesthetic Medicine

AesMed is a smart assistant that provides post-treatment guidance, safety warnings, and procedure explanations in the field of aesthetic medicine. Built entirely in Kaggle using Google's Gemini 2.0 API, it simulates how healthcare professionals might answer typical patient questions after treatments like Botox, microneedling, or chemical peels — without diagnosing or prescribing.

---

## 🎯 Project Goals

- ✅ Deliver reliable, medically grounded answers using retrieval-augmented generation (RAG)
- ✅ Use Gemini’s function calling to route queries to proper "intents" (post-care, explainers, safety alerts)
- ✅ Self-evaluate AI answers using structured rubric scoring
- ✅ Keep everything Kaggle-compatible (no billing, no external secrets)

---

## 🛠️ Technologies Used

| Stack              | Tool                          |
|--------------------|-------------------------------|
| LLM API            | Gemini 2.0 Flash (`google-genai`) |
| Environment        | Kaggle Kernel (Python 3.11)    |
| Retrieval Logic    | Simulated RAG (keyword match)  |
| Function Calling   | Prompt-classified dispatch     |
| Evaluation         | Gemini scoring with rubric     |

---

## ⚙️ How It Works

### 🧾 User Input:
> *"Can I use retinol after a peel?"*

### 🔍 RAG Search:
Searches internal knowledge base for related info:
```text
"Retinol can increase skin sensitivity. Avoid using it immediately after a chemical peel."
🧠 Gemini Responds:
"Retinol can increase skin sensitivity. Avoid using it immediately after a chemical peel."

🛠️ Function Call (routed):
safety_warning("retinol")
Returns: "Warning: Retinol may cause irritation if used after skin treatments."

📊 Self-Evaluation:
Score: 5
Explanation: "Excellent — grounded, fluent, instruction-following."

💬 Example Output
text
Copy
Edit
💬 User: What should I do after laser treatment?

📚 Contextual Reply:
Sunscreen is critical after peels or laser treatments. Use SPF 50+ daily.

⚙️ Routed Intent:
post_care_recommendation()

🧠 Assistant Response:
Apply soothing agents like aloe vera. Avoid sun. Use SPF 50+.

📊 Evaluation:
Score: 5 (Accurate, readable, safety-aligned)
📁 File Structure
plaintext
Copy
Edit
├── aesmed_final.ipynb         # Main Kaggle notebook
├── README.md                  # Project overview
├── project_proposal.pdf       # Initial project scope
├── whitepapers/               # Course PDFs from Google
├── training_notebooks/        # Day 1–5 HTML code labs
🚀 Run This Project
Go to Kaggle.com

Create a new notebook

Install Gemini SDK:

python
Copy
Edit
!pip install -U google-genai==1.7.0
Add your API Key under Add-ons → Secrets as GOOGLE_API_KEY

Paste in the final notebook blocks (modular steps)

Run all → Start chatting!

🧪 Demo Ready Use Cases
Patient onboarding chatbot

Pre/post-laser guidance assistant

Internal triage tool for aesthetic clinics

Proof-of-concept for fine-tuned medical Gemini LLM

👨‍⚕️ Ethical Notes
No medical diagnosis or prescription

Knowledge base reviewed for alignment with common dermatology guidance

User is reminded to consult certified professionals

📌 Future Work
Move to Colab + Vertex AI for full embedding support

Integrate FAISS/Vector DB for dynamic search

Add Streamlit interface for real deployment

👋 Author
Walid Barghout
Data Analyst & Public Relations Manager at Sesderma Skin Center
