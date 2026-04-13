# 📄 Talk2PDF Pro: The Production-Grade Semantic Assistant

Most "Chat with your PDF" apps are just local scripts that forget everything the moment you close the tab. **Talk2PDF Pro** is different. It’s built for 2026 standards: it’s persistent, private, and uses actual semantic intelligence to understand your documents.

## 🚀 What makes this "Pro"?

I built this version to solve the three biggest headaches in RAG (Retrieval-Augmented Generation):

1. **It has a Long-Term Memory:** This uses **Pinecone Cloud**. You can close the app, come back tomorrow, and your document's "brain" is still there.
2. **It Respects Privacy:** Every user gets a unique, isolated "namespace."
3. **It's Actually Smart (Semantic Chunking):** No more cutting sentences in half because of a character limit. It uses math to detect "topic shifts," ensuring the AI gets the full context of a thought before it tries to answer.
4. **Lightning Speed:** Using **Groq's Llama 3.3 70B**, you get enterprise-level reasoning with near-zero latency.

## 🛠️ The Professional Stack

* **Orchestration:** LangChain (2026 LCEL Modular Standard)
* **The Model:** Llama 3.3 70B via Groq
* **The DB:** Pinecone (Serverless Cloud Vector Store)
* **The Logic:** SemanticChunker (Experimental)
* **The UI:** Streamlit

## 🏁 Getting Started

### 1. Prerequisites
You’ll need Python 3.10+ and two free API keys:
* [Groq Cloud Console](https://console.groq.com) (For the AI)
* [Pinecone](https://www.pinecone.io/) (For the Memory)

### 2. The Setup
```bash
# Clone the project
git clone [https://github.com/yourusername/Talk2PDF-Pro.git](https://github.com/yourusername/Talk2PDF-Pro.git)
cd Talk2PDF-Pro

# Build the environment
python -m venv .venv
# Windows: .venv\Scripts\activate | Mac/Linux: source .venv/bin/activate

# Install the 2026 Production Stack
pip install streamlit pypdf2 langchain-huggingface langchain-pinecone \
langchain-groq langchain-experimental langchain-core \
sentence-transformers python-dotenv

# Run the app!
streamlit run app.py
