# 🧠 Naive and Parent RAG with LangChain and OpenAI

This project demonstrates two different approaches to Retrieval-Augmented Generation (RAG) using [LangChain](https://www.langchain.com/) and OpenAI's GPT models to answer questions about the classic Brazilian book *"Os Sertões"* by Euclides da Cunha.

## 📚 Project Overview

The notebooks:
- `naive_rag.ipynb`: Implements a basic RAG pipeline using direct vector retrieval from ChromaDB.
- `parent_rag.ipynb`: Uses the ParentDocumentRetriever from LangChain for hierarchical retrieval, improving document structure understanding.

Both notebooks load and parse the PDF file of the book, convert its contents into vector representations, and then use GPT-3.5 to answer pre-defined questions based on context retrieved from the document.

---

## 🛠️ Setup Instructions

1. **Clone the Repository** and navigate to the project folder:

```bash
git clone https://github.com/your-username/langchain-sertoes.git
cd langchain-sertoes
```

2. **Create a `.env` file** in the same directory as the notebooks:

```
OPENAI_API_KEY=your_openai_api_key_here
```

3. **Install required dependencies** (run inside each notebook if using Jupyter):

```python
%pip install python-dotenv langchain openai chromadb
```

---

## 📄 File Descriptions

- `naive_rag.ipynb`: Uses a basic `Retriever` from Chroma and answers questions via a prompt template.
- `parent_rag.ipynb`: Uses LangChain's `ParentDocumentRetriever` for hierarchical chunking and more structured retrieval.
- `os-sertoes.pdf`: The source document used for all question answering.
- `.env`: Contains your `OPENAI_API_KEY` to authenticate with the OpenAI API.

---

## 🤖 Key Technologies

- **LangChain** for building the RAG pipelines
- **OpenAI GPT-3.5** as the language model
- **ChromaDB** for vector store and retrieval
- **python-dotenv** to securely load API keys from `.env`
- **RecursiveCharacterTextSplitter** for chunking documents
- **PromptTemplate** and **RunnableSequence** for consistent prompt-response logic

---

## ❓ Questions Answered

The system is capable of answering questions like:

- What is Euclides da Cunha's view of the northeastern backlands and its people?
- What are the main social and political critiques in *Os Sertões*?
- Who was Antônio Conselheiro and what was his role in the Canudos War?

---

## ✅ Example Output

```json
{
  "numero": 0,
  "pergunta": "What is Euclides da Cunha's view of the northeastern backlands?",
  "resposta": "Euclides describes the harshness of the environment as shaping the resilience of its people..."
}
```

---

## 📌 Notes

- This project is academic and educational in nature.
- Make sure your `.env` file is **never shared** or committed to version control.
