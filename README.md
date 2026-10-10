# 🎯 InterviewGPT: AI-Powered Interview Preparation and Evaluation System Using RAG

## 📌 Project Overview

InterviewGPT is an 🤖 AI-powered interview preparation and evaluation system designed to help students prepare for technical interviews. It analyzes a candidate's resume, identifies technical skills, generates interview questions from an uploaded question-bank PDF, and evaluates answers using a Large Language Model (LLM).

The system provides personalized feedback, including technical scores, communication scores, strengths, weaknesses, missing concepts, improved answers, and recommendations.

## 🎯 Objectives

- 📄 Analyze resumes in PDF format.
- 💡 Extract technical skills using keyword matching.
- 🔍 Retrieve interview questions using Retrieval-Augmented Generation (RAG).
- 🤖 Evaluate candidate answers using the Groq API.
- 📊 Generate structured feedback and scores.
- 🚀 Help students improve their interview performance.

## 🛠️ Technologies Used

- 🐍 **Programming Language:** Python
- 🖥️ **Frontend:** Streamlit
- ⚡ **LLM API:** Groq API
- 🧠 **Language Model:** Llama 3.3 70B Versatile
- 🔗 **RAG Framework:** LangChain
- 📑 **PDF Processing:** pdfplumber, PyPDF
- 🧬 **Embeddings:** Hugging Face Sentence Transformers
- 🗄️ **Vector Database:** ChromaDB
- 🔐 **Environment Management:** python-dotenv

## 📂 Project Structure

```text
InterviewGPT/
├── 📄 app.py
├── 📄 evaluator.py
├── 📄 rag.py
├── 📄 resume_parser.py
├── 📄 skill_extractor.py
├── 📄 requirements.txt
├── 📄 .env.example
├── 📄 .gitignore
├── 📄 README.md
├── 📄 Interview Questions.pdf
└── 📁 data/
    └── 📄 .gitkeep
```

## 🔄 System Workflow

1. 📤 Upload a resume in PDF format.
2. 📃 Extract resume text using pdfplumber.
3. 💡 Identify technical skills using keyword matching.
4. 📚 Upload the interview question-bank PDF.
5. ✂️ Split the document into text chunks and generate embeddings.
6. 🗄️ Store document chunks in ChromaDB.
7. 🔍 Retrieve relevant text and generate an interview question.
8. ✍️ Enter an answer to the question.
9. 🤖 Evaluate the answer using the Groq API.
10. 📊 Display the evaluation report with scores and improvement suggestions.

## ⚙️ Installation and Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/InterviewGPT.git
cd InterviewGPT
```

🔹 Replace `YOUR_USERNAME` with your GitHub username.

### 2️⃣ Create a Virtual Environment

```bash
python -m venv .venv
```

Activate it on Windows:

```bash
.venv\Scripts\activate
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 4️⃣ 🔑 Configure the Groq API Key

Create a `.env` file in the project root directory and add:

```text
GROQ_API_KEY=your_actual_groq_api_key
```

🔐 Replace the placeholder with your own API key from the [Groq Console](https://console.groq.com/keys).

⚠️ **Security:** Never upload your `.env` file or expose your API key on GitHub.

### 5️⃣ 🚀 Run the Application

```bash
streamlit run app.py
```

🌐 The application will open in your browser.

## 🧩 Main Modules

- 🖥️ **app.py:** Provides the Streamlit interface for resume uploads, question-bank processing, interview practice, and evaluation reports.
- 📄 **resume_parser.py:** Extracts readable text from uploaded resume PDFs.
- 💡 **skill_extractor.py:** Identifies technical skills using predefined keywords.
- 🔍 **rag.py:** Loads the question-bank PDF, splits text into chunks, creates embeddings, stores them in ChromaDB, and retrieves question candidates.
- 🤖 **evaluator.py:** Uses the Groq API and Llama model to evaluate candidate answers and generate feedback.

## 📚 Interview Questions

The project includes **`Interview Questions.pdf`**, which serves as the question-bank document for technical interview practice.

### 🧠 Topics

- 🐍 Python Programming
- 🗄️ SQL and Database Management
- 🤖 Machine Learning
- 🧠 Deep Learning
- 💬 Natural Language Processing (NLP)
- ✨ Generative AI
- 🔗 RAG and LangChain

### 📝 How to Use

1. Open InterviewGPT in your browser.
2. Upload `Interview Questions.pdf` in the Interview Question Bank section.
3. Click **Process Question Bank**.
4. Click **Generate Interview Question**.
5. Enter your answer and click **Evaluate Answer**.
6. Review your scores and personalized feedback.

## 📊 Expected Output

The evaluation report includes:

- 🎯 Technical Score out of 10
- 💬 Communication Score out of 10
- ✅ Strengths
- ❌ Weaknesses
- 📌 Missing Concepts
- ✨ Improved Answer
- 💡 Final Recommendation

## ⚠️ Current Limitations

- 🔤 Skill extraction depends on predefined keywords.
- 🖼️ Scanned PDFs may require OCR support.
- 📑 Question extraction depends on PDF formatting.
- 🤖 AI-generated scores and feedback may contain errors.
- 💾 Interview history is not stored persistently in the current implementation.

## 🔮 Future Enhancements

- 🎯 Improve resume-based question personalization.
- 🖼️ Add OCR support for scanned PDFs.
- 🌐 Support additional interview domains.
- 📈 Store interview history and track progress.
- 🔐 Add authentication and candidate dashboards.
- 🧠 Improve question extraction and retrieval accuracy.

## 📌 Project Status

🚧 **Initial Implementation** — Developed for academic learning and interview preparation. Test the application and its modules before presenting it as a fully validated system.

## ⚖️ Disclaimer

InterviewGPT is an educational practice tool. Its AI-generated scores and recommendations are not official hiring decisions.

## 👩‍💻 Author

Developed as an academic project to explore **Generative AI, Retrieval-Augmented Generation (RAG), and automated interview evaluation**.

⭐ If you find this project useful, consider giving the repository a star on GitHub!

