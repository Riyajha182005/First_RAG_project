# 🧠 RAG Agent with Calculator + Knowledge Base

### Powered by LangGraph + Claude

This is my first **Retrieval-Augmented Generation (RAG)** project that combines:

* 📚 Semantic search over documents
* 🧮 A calculator tool for precise math
* 🔗 Agent workflows using LangGraph
* 🤖 Claude for reasoning and response generation

---

## 🚀 Features

* 🔍 **Knowledge Base Search**

  * Uses FAISS for fast vector similarity search
  * Supports querying custom documents

* 🧮 **Calculator Tool**

  * Handles numerical queries accurately
  * Avoids LLM hallucinations in math

* 🔄 **LangGraph Agent Workflow**

  * Routes queries intelligently between tools
  * Supports multi-step reasoning

* 🤖 **Claude Integration**

  * Generates context-aware, high-quality responses

---

## 🏗️ Project Structure

```bash
.
├── faiss_index/        # Stored vector database
├── sample_docs/        # Input documents for RAG
├── agent.py            # LangGraph agent logic
├── ingest.py           # Document processing & embedding
├── app.py              # Main app entry point
├── main.py             # Alternate runner / testing
├── experiments.ipynb   # Experiments & testing
├── .env                # API keys
├── requirements.txt / pyproject.toml
└── README.md
```

---

## ⚙️ Setup

### 1. Clone the repo

```bash
git clone https://github.com/your-username/rag-agent.git
cd rag-agent
```

### 2. Create virtual environment

```bash
python -m venv .venv
.venv\Scripts\activate   # Windows
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

## 🔑 Environment Variables

Create a `.env` file:

```env
ANTHROPIC_API_KEY=your_claude_api_key
```

(Optional depending on embeddings)

```env
OPENAI_API_KEY=
GOOGLE_API_KEY=
```

---

## 📥 Ingest Documents

```bash
python ingest.py
```

This will:

* Load documents from `sample_docs/`
* Convert them into embeddings
* Store them in `faiss_index/`

---

## ▶️ Run the App

```bash
python app.py
```

---

## 🧪 Example Queries

* “Summarize the documents”
* “What is discussed in the knowledge base?”
* “What is 125 * 48?”
* “Find and calculate key metrics from the data”

---

## 🧠 How It Works

1. User query is passed to the LangGraph agent
2. Agent decides:

   * Use **calculator tool** OR
   * Perform **vector search**
3. Relevant context is retrieved from FAISS
4. Claude generates the final response

---

## 🔥 Key Learnings

* Built a full RAG pipeline from scratch
* Integrated tools into an agent workflow
* Learned vector databases (FAISS)
* Handled real-world issues like rate limits
