# rag-watsonx-chatbot
Retrieval-Augmented QA Bot using LangChain and IBM Watsonx

# 🧠 RAG Chatbot with IBM Watsonx & LangChain

A Retrieval-Augmented Generation (RAG) chatbot that answers questions based on the contents of a user-uploaded PDF document. It integrates IBM Watsonx LLM and embeddings with LangChain, ChromaDB, and Gradio.

---

## 🔧 Features

- 📝 Upload any PDF file
- 🔍 Retrieves relevant document chunks using embeddings
- 💬 Uses IBM Watsonx LLM to generate answers based on retrieved content
- 🌐 Interactive Gradio web interface
- 🔐 Secure API key handling via environment variables

---

## 🚀 Demo

Coming soon (to be deployed on Hugging Face Spaces or Render).

---

## 🧰 Tech Stack

- **LangChain** – for RAG pipeline and QA chain
- **IBM Watsonx.ai** – for LLM & embeddings (`WatsonxLLM`, `WatsonxEmbeddings`)
- **ChromaDB** – for vector similarity search
- **Gradio** – for the frontend interface
- **Python**, **PyPDFLoader**, **Pydantic**

---

## 🗂️ How It Works

1. **User uploads a PDF**
2. **Document is chunked** using `RecursiveCharacterTextSplitter`
3. **Chunks are embedded** using Watsonx Embeddings and stored in Chroma
4. **LangChain Retriever** finds relevant chunks
5. **Watsonx LLM** is prompted with the retrieved content to generate the answer

---

## 📦 Setup Instructions

1. Clone the repo
2. Create a virtual environment and activate it
3. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```
4. Set the following environment variables:
    ```bash
    export WATSONX_APIKEY=your_api_key
    export WATSONX_PROJECT_ID=your_project_id
    export WATSONX_URL=https://us-south.ml.cloud.ibm.com
    ```
5. Run the app:
    ```bash
    python qabot.py
    ```

---

## 📚 Future Improvements

- Add chat memory (ConversationalRetrievalChain)
- Deploy the app publicly
- Add support for other document types (DOCX, TXT)

---

## 🤝 Acknowledgements

- IBM Watsonx for powerful enterprise-grade LLMs
- LangChain for flexible integration patterns
- Gradio for rapid prototyping

---

## 📧 Contact

Built by **Gladson Jacob**. For internship inquiries, reach out via www.linkedin.com/in/gladson-jacob-ba563325a or gladsonjacob814@gmail.com
