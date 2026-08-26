Sure — here is the **raw `README.md` code**, ready to copy directly into your GitHub profile repository.

````markdown
# Hi, I'm Aaradhya Mehra 👋

### AI/ML Engineer · Backend Engineer · Computer Science @ BIT Bengaluru

I build **production-oriented AI systems** that go beyond simply calling an LLM.

My focus is on **RAG systems, LLM reliability, semantic caching, ML pipelines, backend engineering, and AI system design** — with an emphasis on measurable performance, evaluation, and safe deployment.

Currently pursuing a **B.Tech in Computer Science Engineering at Bangalore Institute of Technology** with an **8.5/10 CGPA**, graduating in June 2027.

---

## 🧠 What I Build

My engineering interests sit at the intersection of **AI/ML and backend systems**.

```text
                 AI Engineering
                      │
        ┌─────────────┼─────────────┐
        │             │             │
       RAG        LLM Systems    ML Systems
        │             │             │
  Retrieval      Caching        Prediction
  Evaluation     Reliability    Explainability
  Citations      Latency        Risk Scoring
        │             │             │
        └─────────────┼─────────────┘
                      │
                 Backend APIs
                      │
              FastAPI · Docker
````

I enjoy working on the engineering problems around AI systems — not just model inference, but **retrieval quality, evaluation, caching, latency, failure handling, and deployment**.

---

# 🚀 Featured Projects

## 01. Support Knowledge Copilot

### RAG-based support assistant with verified citations

**Python · FastAPI · Streamlit · Docker · RAG · BM25 · Dense Retrieval · LLM-as-Judge**

A RAG-based support assistant that answers questions from internal documentation while verifying whether the retrieved sources actually support the generated answer.

### Why I built it

Traditional RAG systems can retrieve relevant documents but still produce answers that are:

* poorly supported by retrieved context
* overly confident when retrieval quality is low
* difficult to evaluate systematically

Instead of treating retrieval + generation as a black box, I designed the system around **retrieval quality, citation verification, confidence scoring, and evaluation**.

### Architecture

```text
                    User Query
                        │
                        ▼
               ┌─────────────────┐
               │ Query Processing│
               └────────┬────────┘
                        │
              ┌─────────┴─────────┐
              ▼                   ▼
       Dense Retrieval         BM25
              │                   │
              └─────────┬─────────┘
                        ▼
              Reciprocal Rank Fusion
                        │
                        ▼
                 Retrieved Context
                        │
                        ▼
                  LLM Generation
                        │
              ┌─────────┴─────────┐
              ▼                   ▼
        Confidence Score     LLM-as-Judge
              │                   │
              └─────────┬─────────┘
                        ▼
             Verified Final Answer
                        │
                        ▼
             Citation + Response
```

### Key Engineering Work

**Hybrid Retrieval**

Combined dense semantic retrieval with **BM25 lexical retrieval**, then fused the rankings using **Reciprocal Rank Fusion (RRF)**.

**Result:**

> **72% → 88% accuracy**

**Citation Verification**

Implemented an **LLM-as-Judge verification layer** that checks whether retrieved citations actually support the claims made in the final response.

**Confidence & No-Answer Detection**

Designed confidence scoring and no-answer detection so the system can avoid confidently answering questions when retrieval evidence is insufficient.

**Evaluation**

Created a hand-built **50–75 question golden evaluation set** to measure retrieval and answer quality.

**Deployment**

Built the application using:

* FastAPI backend
* Streamlit frontend
* Docker containerization

---

### Results

| Metric                    |          Result |
| ------------------------- | --------------: |
| Baseline accuracy         |             72% |
| Hybrid retrieval accuracy |         **88%** |
| Evaluation dataset        | 50–75 questions |
| Citation verification     |    LLM-as-Judge |
| Backend                   |         FastAPI |
| UI                        |       Streamlit |
| Deployment                |          Docker |

---

## 02. Semantic Cache Gateway for LLM APIs

### Semantic caching layer for reducing LLM latency and API cost

**Python · FastAPI · Qdrant · ChromaDB · Redis · Docker · Locust · Embeddings**

A caching proxy that identifies **semantically similar LLM requests** and serves previously generated responses instead of repeatedly calling the underlying LLM API.

### Why I built it

Traditional caching depends heavily on exact string matching.

For example:

```text
"What is the refund policy?"

"Can you explain your refund rules?"
```

An exact-match cache treats these as different requests.

A semantic cache can recognize that the two requests may have the same intent and reuse a previous response when the similarity and policy conditions are satisfied.

### Architecture

```text
                  Client Request
                        │
                        ▼
                 ┌──────────────┐
                 │ FastAPI Proxy│
                 └──────┬───────┘
                        │
                        ▼
                  Generate Embedding
                        │
                        ▼
                Vector Store Search
                        │
                 ┌──────┴──────┐
                 │             │
              Cache Hit     Cache Miss
                 │             │
                 ▼             ▼
          Validate Hit      LLM API
                 │             │
                 │             ▼
                 │       Store Response
                 │             │
                 └──────┬──────┘
                        ▼
                  Return Response
```

### Key Engineering Work

**Embedding-Based Semantic Matching**

Converted incoming requests into embeddings and searched a vector store for semantically similar previous requests.

**Cache Correctness**

A cache hit does not automatically mean a correct cache hit.

I added:

* similarity threshold tuning
* LLM-as-Judge validation
* cache correctness checks

to reduce incorrect reuse of cached responses.

**Performance Optimization**

The system achieved:

* **40% reduction in simulated LLM API cost**
* **65% reduction in P95 latency**
* Validation across **2,000 requests**

**Policy Isolation**

Designed policy tags and TTL rules to prevent cached responses from leaking across users or sensitive query boundaries.

**Load Testing**

Load-tested the FastAPI proxy using **Locust**, with Redis and a vector-store backend.

---

### Results

| Metric                       |                     Result |
| ---------------------------- | -------------------------: |
| Simulated API cost reduction |                    **40%** |
| P95 latency reduction        |                    **65%** |
| Requests validated           |                  **2,000** |
| Cache matching               | Semantic / embedding-based |
| Correctness validation       |               LLM-as-Judge |
| Load testing                 |                     Locust |

---

# 🛠️ Technical Stack

## AI / GenAI

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square\&logo=python\&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square)
![LangGraph](https://img.shields.io/badge/LangGraph-000000?style=flat-square)
![Hugging Face](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat-square\&logo=huggingface\&logoColor=black)
![RAG](https://img.shields.io/badge/RAG-8A2BE2?style=flat-square)
![Qdrant](https://img.shields.io/badge/Qdrant-D63AFF?style=flat-square)
![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6B6B?style=flat-square)

**RAG · LangChain · LangGraph · Hugging Face · Vector Databases · Prompt Engineering · LLM-as-Judge**

---

## Machine Learning & Data

![Scikit Learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square\&logo=scikit-learn\&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square\&logo=pandas\&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square\&logo=numpy\&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat-square)

**Scikit-learn · Pandas · NumPy · Matplotlib**

---

## Backend

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square\&logo=fastapi\&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square\&logo=node.js\&logoColor=white)
![REST](https://img.shields.io/badge/REST_APIs-02569B?style=flat-square)

**FastAPI · Node.js · REST APIs · Backend System Design**

---

## Databases

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square\&logo=postgresql\&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square\&logo=mongodb\&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square\&logo=redis\&logoColor=white)

**PostgreSQL · MongoDB · Redis · Qdrant · ChromaDB**

---

## Cloud & DevOps

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square\&logo=docker\&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square\&logo=amazonaws\&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square\&logo=github-actions\&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square\&logo=linux\&logoColor=black)

**Docker · AWS S3 · GitHub Actions · Render · Vercel · Linux**

---

## Languages

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square\&logo=python\&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square\&logo=cplusplus\&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square\&logo=javascript\&logoColor=black)
![SQL](https://img.shields.io/badge/SQL-336791?style=flat-square)

**Python · C++ · JavaScript · SQL**

---

# 📊 Engineering Focus

I'm currently going deeper into the areas where AI meets real-world software engineering:

```text
LLM Applications
      │
      ├── RAG
      │    ├── Hybrid Retrieval
      │    ├── Reranking
      │    └── Evaluation
      │
      ├── Reliability
      │    ├── Hallucination Detection
      │    ├── Citation Verification
      │    ├── Confidence Scoring
      │    └── Guardrails
      │
      ├── Performance
      │    ├── Semantic Caching
      │    ├── Latency Optimization
      │    └── Load Testing
      │
      └── Production AI
           ├── APIs
           ├── Docker
           ├── Monitoring
           └── System Design
```

---

# 🏆 Achievements

### 🥈 2nd Place — Augmentix Hackathon, NMIT Bangalore

Built **MolGenix** in 36 hours with a 3-member team, owning the FastAPI backend and ML-based molecular docking pipeline.

### 🏆 Smart India Hackathon — Internal Qualifier

Qualified the institute-level selection by designing a **federated learning solution**, leading system architecture and the technical presentation.

### 💻 Competitive Programming

Solved **250+ algorithmic problems** across LeetCode and Codeforces and achieved **Pupil rating** through rated contests.

---

# 🎓 Education

### Bangalore Institute of Technology — Bengaluru, India

**B.Tech in Computer Science Engineering**

**CGPA: 8.5/10**

September 2023 – June 2027

---

# 📚 Certifications

### Full Stack Generative & Agentic AI with Python — Udemy

* RAG pipelines with LangChain and vector databases
* Stateful multi-node agents using LangGraph

### Machine Learning A–Z — Udemy

* Regression
* Classification
* Clustering
* NLP pipelines using Scikit-learn

### C++ DSA — Abdul Bari, Udemy

* Graph algorithms
* Dynamic programming
* Trees
* Time and space complexity analysis

---

# 📈 GitHub Stats

<p align="center">

<img src="https://github-readme-stats.vercel.app/api?username=aaradhya177&show_icons=true&hide_border=true&count_private=true" height="170"/>

<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=aaradhya177&layout=compact&hide_border=true" height="170"/>

</p>

---

# 🔥 Contribution Streak

<p align="center">

<img src="https://streak-stats.demolab.com?user=aaradhya177&hide_border=true" />

</p>

---

# 📫 Let's Connect

I'm open to:

* AI/ML internships
* Software engineering internships
* AI engineering collaborations
* Hackathons
* Open-source projects
* Technical discussions around AI systems and backend engineering

<p align="center">

<a href="https://www.linkedin.com/in/aaradhya-mehra-07a46537b/">
<img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>

<a href="https://github.com/aaradhya177">
<img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white"/>
</a>

<a href="mailto:aaradhyamehra240@gmail.com">
<img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white"/>
</a>

<a href="https://codeforces.com/profile/YoullNeverCodeAlone17">
<img src="https://img.shields.io/badge/Codeforces-1F8ACB?style=for-the-badge&logo=codeforces&logoColor=white"/>
</a>

</p>

---

<p align="center">

<i>Building AI systems that are useful, measurable, and reliable.</i>

</p>
```
