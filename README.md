# Local-RAG-LLM-Chatbot-Ollama-ChromaDB-
A fully local Retrieval-Augmented Generation (RAG) system built using LangChain, ChromaDB, and Ollama.   This project performs semantic search over custom PDF documents and generates grounded responses using a local LLM.  No external APIs. No OpenAI dependency. Fully private and offline.
 Features

- 📄 PDF document ingestion
- ✂️ Intelligent recursive chunking with overlap
- 🔎 Semantic similarity search using vector embeddings
- 🧠 Local embedding model (`nomic-embed-text`)
- 🤖 Local LLM generation (`mistral`)
- 📚 Persistent Chroma vector database
- 🏷 Source attribution with document + page tracking
- 🔐 Fully offline and private

**Tech Stack**
     Python 3.11
     LangChain
     ChromaDB
     Ollama
     Mistral LLM
     Nomic Embeddings

**Install dependencies**
pip install -r requirements.txt

# Pull models
ollama pull nomic-embed-text
ollama pull mistral

# Index documents
python populate_database.py --reset

# Ask question
python query_data.py "Your question here"
Example 
query_data.py "tell me about the overview of the security industry"
Response:The security industry in Ontario provides essential services for public safety and crime prevention. It is primarily composed of security guards who serve as the first line of defense in protecting people, property, and information in various environments such as malls, office buildings, hospitals, and construction sites
Sources:['data\\data.pdf:0:0', 'data\\data.pdf:0:1', 'data\\data.pdf:1:1', 'data\\data.pdf:5:2', 'data\\data.pdf:2:1'] 

# Architecture Diagram

<img width="500" height="350" alt="Architecture" src="https://github.com/user-attachments/assets/e6405e48-3172-4dff-8c40-01530d222e74" />

# Output
<img width="3143" height="354" alt="image" src="https://github.com/user-attachments/assets/c99e98bc-3c0d-4ece-b84d-32e04ab0e8a8" />


