# Personalised Learning System
![2025-02-10 22_01_42-](https://github.com/user-attachments/assets/14f66ac4-8fb5-409f-9f27-10188d8b3f57)

## Overview

The **Personalised Learning System** is an AI-powered application designed to assist users in extracting information from educational materials such as books, syllabi, and question papers. It leverages **LangChain, FAISS, Google Generative AI (Gemini), and Streamlit** to provide features like **question answering, syllabus summarization, quiz generation, and answer key generation**.

---

## Features

### 1. **Question Answering**
- Users can upload a **PDF book**.
- The system **embeds** the content using **GoogleGenerativeAIEmbeddings** and stores it in a **FAISS vector database**.
- Users input a **question**, and the system retrieves the most relevant content from the book to generate an answer.

### 2. **Syllabus Summary**
- Users can upload a **PDF syllabus document**.
- The system extracts **subtopics** from the syllabus using **regular expressions**.
- It then retrieves **relevant content** from the uploaded book to summarize each subtopic.

### 3. **Quiz Generation**
- The system generates **10 multiple-choice questions** based on the uploaded book.
- The questions, answer choices, and correct answers are formatted in **JSON**.
- Users can attempt the quiz within the app and receive a **final score**.

### 4. **Answer Key Generation**
- Users upload a **question paper PDF**.
- The system **extracts questions** from the document and categorizes them into **1-mark, 3-mark, and 15-mark** questions.
- It then searches for **relevant answers** in the book and generates a **detailed answer key**.

---

## Tech Stack

- **Python**
- **Streamlit** (Frontend)
- **LangChain** (LLM orchestration)
- **FAISS** (Vector Database)
- **Google Generative AI (Gemini 2.0)** (LLM & embeddings)
- **PyPDF2** (PDF processing)
- **Regular Expressions (Regex)** (Text extraction)
- **OS & JSON** (File handling & data formatting)

---

## Installation & Setup

### **1. Clone the Repository**
```sh
git clone <repo-url>
cd personalised-learning-system
```

### **2. Install Dependencies**
```sh
pip install -r requirements.txt
```

### **3. Set Up API Keys**
- Create a `.env` file in the project root.
- Add your **Google API Key**:
  ```
  GOOGLE_API_KEY=your_api_key_here
  ```

### **4. Run the Application**
```sh
streamlit run app.py
```

---

## File Structure
```
📂 personalised-learning-system
│── 📂 main_book_files         # Stores uploaded book PDFs
│── 📂 Syllabus_book_files     # Stores uploaded syllabus PDFs
│── 📂 Question_paper_files    # Stores uploaded question papers
│── app.py                     # Main Streamlit app
│── requirements.txt            # Required dependencies
│── .env                        # API keys
│── README.md                   # Documentation
```

---

## Usage Guide

### **Uploading Documents**
1. Upload a **book PDF** under the **"Question Answer"** tab.
2. (Optional) Upload a **syllabus PDF** to summarize course topics.
3. (Optional) Upload a **question paper PDF** for answer key generation.

### **Generating Answers**
- Enter a **question** in the "Question Answer" tab and click **Generate**.
- For **syllabus topics**, click **Generate** under the "Syllabus Summary" tab.

### **Taking a Quiz**
- Click **"Generate Quiz"** under the "Quiz" tab.
- Answer the generated **MCQs** and view your score.

### **Creating an Answer Key**
- Upload a **question paper PDF** under the "Answer Key Generator" tab.
- Click **"Generate Answer Key"** to retrieve answers.

---

## Notes
- Ensure all uploaded files are in **PDF format**.
- The system works best with **well-structured books & question papers**.
- API calls to **Google Gemini** may have usage limits.

---
