# 📄 Talk2PDF: A Smarter Way to Chat with Documents

Let’s be honest: Most RAG (Retrieval-Augmented Generation) apps feel a bit "broken" because they cut text into arbitrary chunks. This project is my attempt to fix that using Semantic Intelligence.

## 🧐 Why is this different?

Standard RAG apps are like using a paper shredder on a book and trying to glue it back together. **Talk2PDF** is different:

* **It thinks before it splits:** It uses an embedding model to find actual "topic shifts." If you're talking about 'Revenue' in one paragraph and 'Risk' in the next, it knows to separate them.
* **Speed:** Powered by Groq, the responses aren't just fast; they're nearly instant.
* **Clean Code, Modern Stack:** No legacy spaghetti code. This uses the 2026 LCEL (LangChain Expression Language) standard. It’s modular, readable, and easy to tweak.
* **Privacy First:** Your data stays local in a ChromaDB instance on your machine.

## 🛠️ The Gear

* **The Engine:** Llama 3.3 70B (via Groq)
* **The Sorter:** SemanticChunker (the "Topic Finder")
* **The Memory:** ChromaDB (Local Vector Store)
* **The UI:** Streamlit (Clean & Simple)

## 🚀 Getting it Running

### 1. Prep the environment
You'll need Python 3.10+. Grab a free API key from [Groq Cloud](https://console.groq.com) first.

```bash
# Clone and jump in
git clone [https://github.com/yourusername/Talk2PDF.git](https://github.com/yourusername/Talk2PDF.git)
cd Talk2PDF

# Create your little sandbox
python -m venv .venv
source .venv/bin/activate # or .venv\Scripts\activate on Windows

# Install the essentials
pip install streamlit pypdf2 langchain-huggingface langchain-chroma \
langchain-groq langchain-experimental langchain-core sentence-transformers \
python-dotenv

# Run the app!
streamlit run app.py
```
