# 🌟 GemDocs

GemDocs is a powerful application that allows users to upload and query multiple PDF documents with the help of **Google Gemini Pro** and **LangChain**. It leverages **FAISS (Facebook AI Similarity Search)** for creating vector embeddings, enabling highly efficient semantic search across large document sets. This project aims to simplify document retrieval by turning PDFs into searchable content and providing intelligent answers to user queries.

---

## 📜 **Overview**

GemDocs transforms how you interact with PDF documents by making them **searchable** and **queryable** through natural language. By using **Google Gemini Pro**, the application can intelligently respond to queries based on the content of the uploaded documents. FAISS handles the document embeddings, ensuring fast and accurate retrieval of relevant document sections. This is ideal for researchers, professionals, or anyone who needs to extract specific information from multiple PDF documents.

---

## 🛠️ **Technologies and Libraries Used**

- **Google Gemini Pro**: Large Language Model (LLM) for generating smart answers based on PDF content.
- **LangChain**: Framework that integrates LLMs with document processing and querying.
- **FAISS**: Vector similarity search for fast and accurate document embeddings.
- **PyPDF2**: Library used to extract text from PDF documents.
- **Python 3.10+**: The programming language used for the backend.
- **dotenv**: Manages environment variables like API keys securely.

---

## 🔧 How It Works

### 1. PDF Uploading and Parsing:
  - The application allows users to upload multiple PDF files.
  - The PyPDF2 library extracts text from these PDFs.
### 2. Vector Embedding Creation:
  - The text content from each document is converted into vector embeddings using FAISS. These embeddings are numerical representations of the document content, enabling efficient similarity searches.
### 3. Querying with Google Gemini Pro:
  - Once the PDF text is stored as vector embeddings, users can query the system. The query is embedded into a vector, and FAISS retrieves the most similar document vectors.
  - The retrieved results are then passed to Google Gemini Pro, which uses the retrieved text data to answer user queries accurately.
### 4. Search Results:
  - The system returns relevant sections of the documents that match the query, allowing users to get precise answers from the uploaded PDFs.

---

## 🧑‍💻 **Installation Instructions**

### 1. Clone the Repository
   Clone the GemDocs repository to your local machine:
   ```
   git clone https://github.com/yourusername/gemdocs.git
  ```
### 2.Set Up Virtual Environment
  Navigate to the project directory and create a virtual environment:
  ```
    cd llm-pdf-faiss-langchain
    python3 -m venv myenv
  ```
### 3. Install Required Dependencies
  Install all the necessary libraries by running:
  ```
    pip install -r requirements.txt
  ```
### 4. Set Up API Keys
  You will need to configure API keys for Google Gemini Pro or any other language model for the embeddings and query generation:
  ```
    GOOGLE_GEMINI_API_KEY=your_google_gemini_api_key
  ```
### 5. Run the Application
  Once everything is set up, run the application using:
  ```
    python app.py
  ```

---

## 💡 Use Case: Real-World Scenario

Imagine a researcher who needs to analyze multiple PDFs related to a particular topic. Instead of manually reading each document, they can upload them to CarZone, which then processes and indexes the documents. The researcher can ask specific questions, and the system will return the most relevant sections from all the uploaded PDFs. This use case shows how Google Gemini Pro, FAISS, and LangChain can streamline document retrieval and analysis.
