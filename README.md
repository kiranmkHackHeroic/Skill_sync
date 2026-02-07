# Skill_sync
SkillSync is an AI-powered Enterprise Knowledge Graph platform. It uses Neo4j and BERT (NLP) to automatically map employee expertise from Jira, Slack, and GitHub metadata, enabling intelligent talent matching and identifying hidden subject matter experts within an organization.
SkillSync: Enterprise Knowledge Graph & Workforce Intelligence Platform
PythonNeo4jLicense

SkillSync is a B2B SaaS platform designed to solve the "Talent Blindness" problem in large enterprises. It transforms unstructured organizational data (activity logs, commits, messages) into a queryable Knowledge Graph, allowing companies to discover hidden experts, match talent to projects intelligently, and detect employee burnout risks.

🚀 The Problem
In large organizations, expertise is often siloed. Managers hire external contractors because they don't know an expert already exists in a different department. Furthermore, traditional HR databases are static and quickly become outdated as employees learn new skills.

💡 The Solution
SkillSync builds a living "Talent Map" by:

Ingesting: Synthetic data generated from Jira tickets, Slack messages, and GitHub commits.
Extracting: Using NLP to identify technical skills and context from unstructured text.
Mapping: Storing these relationships in a Neo4j Graph Database to visualize connections between people, skills, and projects.
Recommending: A hybrid recommendation engine that matches employees to internal projects based on real-world proficiency, not just job titles.
✨ Key Features
Automated Skill Extraction: Fine-tuned BERT-based NLP pipeline for Named Entity Recognition (NER) to extract skills from technical logs with ~80% precision.
Expert Discovery (Graph Algorithms): Uses PageRank and Louvain Community Detection to identify informal subject matter experts and natural talent clusters.
Talent Matching Engine: Hybrid recommendation system combining Collaborative Filtering and Content-Based Similarity over skill embeddings.
Burnout Detection: "Bandwidth Score" dashboard that analyzes passive activity signals (overtime trends, focus consistency) to flag employees at risk of burnout.
Taxonomy Standardization: Maps extracted raw skills to standard industry taxonomies (ESCO, O*NET).
Privacy by Design: Implements cryptographic hashing and metadata-only processing to ensure employee privacy compliance.
🏗️ Architecture
The system is built on a microservices architecture:

Ingestion Layer: Python scripts to generate and normalize synthetic data.
Processing Layer: NLP Pipeline (spaCy/BERT) for entity linking and disambiguation.
Storage Layer: Neo4j Knowledge Graph for relationship storage.
API Layer: FastAPI serving RESTful endpoints for search and recommendations.
Frontend: Streamlit dashboard for visualization.
🛠️ Tech Stack
Graph Database: Neo4j, Cypher Query Language
Backend: Python, FastAPI, Pydantic
AI / ML: PyTorch, HuggingFace Transformers (BERT), spaCy, Scikit-learn
Data Manipulation: Pandas, NumPy
Frontend: Streamlit (Demo), NeoVis.js (Graph Viz)
📊 Project Highlights
Scalability: Designed to handle organizational graphs with thousands of nodes and edges.
Context Awareness: Distinguishes between "Apple" (the fruit) and "Apple" (the tech company) using entity disambiguation.
Actionable Insights: Provides "Bandwidth Scores" to prevent over-utilization of top performers.
🚀 Getting Started
Prerequisites
Python 3.9+
Neo4j Desktop (running local instance)
Docker (optional, for containerization)
Installation
Clone the repo:
git clone https://github.com/your-repo/SkillSync.gitcd SkillSync
Install dependencies:
pip install -r requirements.txt
Start Neo4j:
Open Neo4j Desktop and start the database (default bolt url: bolt://localhost:7687).
Run the Ingestion Pipeline:
python data_pipeline/generate_synthetic_data.py
Run the Skill Extraction NLP:
python nlp/run_extraction.py
Launch the API:
uvicorn api.main:app --reload
View the Dashboard:
streamlit run dashboard/app.py
🤝 Contributing
This is a portfolio project demonstrating full-stack data science and engineering capabilities. Suggestions and pull requests are welcome!

