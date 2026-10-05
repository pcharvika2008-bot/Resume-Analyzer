# 📄 AI Resume Analyzer

An interactive local web application built with Python and Streamlit that helps job seekers analyze their resumes against specific job descriptions. The application calculates text similarity, extracts matched/missing keywords, and uses a local **Ollama LLM (Llama 3.2)** to generate structured feedback and actionable optimization suggestions.

## 🚀 Features

- **Local PDF Parsing**: Extracts text securely from uploaded PDF resumes.
- **Text Similarity Metric**: Computes a basic text overlap percentage using `scikit-learn`'s TF-IDF Vectorizer and Cosine Similarity.
- **Keyword Matching Engine**: Compares words in the resume against the job description to find missing and matching industry keywords.
- **Privacy-First AI Feedback**: Connects to your local Ollama instance running `llama3.2` to generate comprehensive resume critiques without sending your data to external APIs.
- **Downloadable Reports**: Export your text similarity results, keyword breakdowns, and AI feedback into a plain text report (`.txt`).

---

## 🛠️ Prerequisites

Before running the application, make sure you have the following installed on your machine:

1. **Python 3.8 or higher**
2. **Ollama** (Download from [ollama.com](https://ollama.com))

### Setting up Ollama
Ensure you have downloaded and pulled the correct model locally. Run the following command in your terminal:

```bash
ollama pull llama3.2
```

---

## 📦 Installation & Setup

1. **Clone or download** this repository to your local machine.

2. **Navigate** into the project directory:
   ```bash
   cd ai-resume-analyzer
   ```

3. **Install the required Python dependencies**:
   ```bash
   pip install streamlit ollama pypdf scikit-learn
   ```

---

## 🖥️ How to Run the App

1. Make sure your local **Ollama** application is open and running in the background.
2. Launch the Streamlit application by running:
   ```bash
   streamlit run app.py
   ```
   *(Replace `app.py` with the actual filename of your script if it is named differently)*
3. The app will automatically open in your default browser at `http://localhost:8501`.

---

## 💡 How to Use

1. **Upload Resume**: Drag and drop your resume in `.pdf` format.
2. **Paste Job Description**: Copy and paste the text of the job description you are targeting into the text box.
3. **Analyze**: Click the **🔍 Analyze Resume** button.
4. **Review Results**: View your text matching statistics, check missing keywords, read structured suggestions from the AI, and click **📥 Download Analysis** to keep a local copy of your report.

---

## 🛡️ Privacy & Disclaimer

- **Privacy**: All text extraction, metric math, and AI analysis happen entirely on your computer. No data is sent over the internet.
- **Disclaimer**: This tool provides generic text analytics and AI insights. It does not guarantee or mimic exact Applicant Tracking System (ATS) parsing rules or hiring results.
