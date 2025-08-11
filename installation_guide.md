# 📄 Legal Document Analyzer

This project analyzes uploaded legal `.docx` documents, identifies potential issues, and provides improvement suggestions.
The tool also outputs results in both **human-readable text** and **downloadable JSON format**, and can highlight errors directly in a newly generated `.docx` file.

Built with:

* [Streamlit](https://streamlit.io/) for the user interface
* [LangChain](https://www.langchain.com/) for document processing
* [docx2txt](https://pypi.org/project/docx2txt/) for text extraction
* OpenAI or local LLaMA for analysis

---

## 🚀 Features

* Upload multiple `.docx` legal documents
* Extract and analyze text from documents
* Identify potential issues and suggest improvements
* Export results as a **JSON file**
* Option to download all processed files (including the original docs) as a **ZIP archive**
* Streamlit UI for easy interaction

---

## 📦 Installation

### 1️⃣ Clone the repository

```bash
git clone https://github.com/MarcusV210/ai-engineer-task-MarcusV210.git
cd ai-engineer-task-MarcusV210
```

### 2️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

### 3️⃣ Environment variables

Create a `.env` file in the project root:

```env
OPENAI_API_KEY=your_openai_api_key_here
```

> 💡 If using local LLaMA, adjust the config in `app.py` accordingly.

---

## 📜 Usage

### Run the Streamlit app

```bash
streamlit run frontend.py
```

### Upload documents

* Select one or more `.docx` files
* Wait for the analysis to complete
* View results in a **text area**
* Download the JSON report or all files as a **ZIP**

---

## 📄 Example Output (JSON)

```json
{
  "process": "Company Incorporation",
  "documents_uploaded": 4,
  "required_documents": 5,
  "missing_document": "Register of Members and Directors",
  "issues_found": [
    {
      "document": "Articles of Association",
      "section": "Clause 3.1",
      "issue": "Jurisdiction clause does not specify ADGM",
      "severity": "High",
      "suggestion": "Update jurisdiction to ADGM Courts."
    }
  ]
}
```

---

## ⚠️ Disclaimer

This tool is **not a substitute for professional legal advice**. Always have a qualified legal professional review your documents before making decisions.
