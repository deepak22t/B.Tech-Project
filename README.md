
# AcadBot: Advanced RAG-based Academic Assistant

AcadBot is an intelligent **Retrieval-Augmented Generation (RAG)** platform designed to provide precise, context-aware answers to college-related queries. By leveraging high-density vector embeddings and Large Language Models (LLMs), AcadBot transforms static college documents into an interactive, searchable knowledge base.

## 🚀 Key Features

* **Semantic Search & Retrieval**: Uses **Sentence-Transformers** to convert raw documents into high-dimensional vector embeddings, allowing for context-aware similarity searches rather than simple keyword matching.
* **Contextual Intelligence**: Powered by the **Cohere LLM**, the system generates natural language responses strictly grounded in the retrieved document context to minimize hallucinations.
* **End-to-End RAG Pipeline**:
* **Ingestion**: Processes PDF/Text college documents.
* **Chunking**: Breaks data into optimized segments for better retrieval granularity.
* **Similarity Search**: Performs ranking to find the most relevant "top-k" chunks based on user intent.


* **Secure User Ecosystem**: Complete authentication system with hashed credentials and personalized query history.
* **Task & Query Management**: Integrated dashboard for users to manage specific academic tasks alongside their AI assistant.

## 🛠 Tech Stack

* **LLM**: Cohere (Command Model)
* **Embeddings**: Sentence-Transformers (`all-MiniLM-L6-v2`)
* **Backend**: Flask (Python)
* **Database**: SQLite (Metadata) & Vector-based Similarity Search
* **ORM**: SQLAlchemy
* **Frontend**: HTML5, CSS3 (SCSS), Jinja2 templates

## 🏗 System Architecture

1. **Data Ingestion**: College-specific documents are uploaded and pre-processed.
2. **Embedding Generation**: The `SentenceTransformer` model encodes text chunks into vectors.
3. **User Query**: When a user asks a question, their query is embedded into the same vector space.
4. **Similarity Search**: The system calculates the cosine similarity to retrieve the most relevant chunks from the local knowledge base.
5. **Augmented Generation**: The retrieved chunks and the original query are sent to **Cohere LLM** to produce a concise, factual answer.

## 🔧 Installation & Setup

### Prerequisites

* Python 3.8+
* Cohere API Key

### Setup Steps

1. **Clone the Repository**
```bash
git clone https://github.com/Deepak-Kumar-1764/AcadBot.git
cd AcadBot

```


2. **Environment Configuration**
Create a `.env` file in the root directory:
```env
COHERE_API_KEY=your_api_key_here
SECRET_KEY=your_flask_secret_key
DATABASE_URL=sqlite:///acadbot.db

```


3. **Install Dependencies**
```bash
pip install -r requirements.txt

```


4. **Initialize Database & Migrations**
```bash
flask db init
flask db migrate -m "Setup RAG schema"
flask db upgrade

```


5. **Run the Application**
```bash
flask run

```



## 📈 Future Roadmap

* [ ] Integration with **Qdrant** or **FAISS** for scalable vector storage.
* [ ] Support for multi-modal documents (extracting data from tables/images).
* [ ] Mobile application deployment via **React Native**.

---

**Would you like me to create the shortened LaTeX version of this project for your resume now?**
