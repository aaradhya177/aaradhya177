````markdown
# 👋 Hi, I'm Aaradhya Mehra

### AI/ML Engineer · Backend Engineer · CS @ BIT Bengaluru

I build **production-oriented AI systems** with a focus on **RAG, LLM reliability, semantic caching, machine learning, backend engineering, and AI system design**.

Currently pursuing **B.Tech in Computer Science Engineering at Bangalore Institute of Technology** with an **8.5/10 CGPA**, graduating in 2027.

I like building systems where AI is not just a demo — but something that is **measurable, reliable, explainable, and deployable**.

---

<div align="center">

### ⚡ AI Engineering • Backend Systems • Machine Learning

</div>

<br>

<div align="center">

<img src="https://skillicons.dev/icons?i=python,cpp,js,java,react,nextjs,nodejs,fastapi,postgres,mongodb,redis,docker,aws,git,github,linux,tensorflow&perline=9" />

</div>

<br>

<div align="center">

`RAG` · `LLM Systems` · `Machine Learning` · `FastAPI` · `Vector Databases` · `System Design`

</div>

---

# 🚀 Featured Projects

## 🧠 Support Knowledge Copilot

### RAG-based support assistant with verified citations

**Python · FastAPI · Streamlit · Docker · RAG · BM25 · Dense Retrieval · LLM-as-Judge**

A RAG-based support assistant that answers questions from internal documentation while verifying whether retrieved sources actually support the generated answer.

### 🔍 What I Built

- Hybrid retrieval using **dense embeddings + BM25**
- **Reciprocal Rank Fusion (RRF)** to combine retrieval results
- **LLM-as-Judge** citation verification
- Confidence scoring for retrieved context
- No-answer detection for low-confidence queries
- Hand-built **50–75 question golden evaluation set**
- FastAPI backend with Streamlit interface
- Dockerized deployment

### 📈 Results

| Metric | Result |
|---|---:|
| Baseline Accuracy | 72% |
| Improved Accuracy | **88%** |
| Evaluation Dataset | 50–75 questions |
| Citation Verification | LLM-as-Judge |
| Backend | FastAPI |
| UI | Streamlit |
| Deployment | Docker |

### 🏗️ Architecture

```text
                         USER QUERY
                              │
                              ▼
                    ┌──────────────────┐
                    │ Query Processing  │
                    └─────────┬────────┘
                              │
                 ┌────────────┴────────────┐
                 ▼                         ▼
          Dense Retrieval               BM25
                 │                         │
                 └────────────┬────────────┘
                              ▼
                  Reciprocal Rank Fusion
                              │
                              ▼
                     Retrieved Context
                              │
                              ▼
                       LLM Generation
                              │
                 ┌────────────┴────────────┐
                 ▼                         ▼
          Confidence Score            LLM-as-Judge
                 │                         │
                 └────────────┬────────────┘
                              ▼
                    Verified Final Answer
                              │
                              ▼
                       Citations + Answer
````

### 💡 Engineering Focus

The main challenge wasn't simply generating an answer.

It was making the answer **trustworthy**.

The system therefore treats:

```text
Retrieval
    ↓
Ranking
    ↓
Generation
    ↓
Citation Verification
    ↓
Confidence
    ↓
Evaluation
```

as one complete pipeline.

---

# ⚡ Semantic Cache Gateway for LLM APIs

### Semantic caching layer for reducing LLM latency and API cost

**Python · FastAPI · Qdrant · ChromaDB · Redis · Docker · Locust**

A caching proxy that detects **semantically similar LLM requests** and reuses previously generated responses instead of repeatedly calling the underlying LLM API.

### 🧠 The Problem

Traditional caching relies on exact string matching.

```text
"What is the refund policy?"

"Can you explain your refund rules?"
```

These are different strings but can represent the same intent.

The gateway uses embeddings to identify semantic similarity and determine whether an existing response can safely be reused.

### 🔧 What I Built

* Embedding-based semantic cache
* Vector similarity search
* Similarity threshold tuning
* LLM-as-Judge cache validation
* Cache correctness checks
* Policy tags for cache isolation
* TTL-based cache policies
* Redis-backed caching
* Vector database backend
* Locust load testing
* Dockerized FastAPI service

### 📈 Results

| Metric                       |       Result |
| ---------------------------- | -----------: |
| Simulated API Cost Reduction |      **40%** |
| P95 Latency Reduction        |      **65%** |
| Requests Validated           |    **2,000** |
| Cache Type                   |     Semantic |
| Validation                   | LLM-as-Judge |
| Load Testing                 |       Locust |

### 🏗️ Architecture

```text
                       CLIENT REQUEST
                              │
                              ▼
                    ┌──────────────────┐
                    │   FastAPI Proxy  │
                    └─────────┬────────┘
                              │
                              ▼
                     Generate Embedding
                              │
                              ▼
                     Vector Store Search
                              │
                    ┌─────────┴─────────┐
                    │                   │
                    ▼                   ▼
                CACHE HIT          CACHE MISS
                    │                   │
                    ▼                   ▼
             Validate Cache          LLM API
                    │                   │
                    │                   ▼
                    │             Store Response
                    │                   │
                    └─────────┬─────────┘
                              ▼
                       RETURN RESPONSE
```

---

# 🛠️ Tech Stack

## 🤖 AI / Generative AI

<div align="center">

<img src="https://skillicons.dev/icons?i=python,tensorflow&perline=10" />

<br><br>

<img src="https://img.shields.io/badge/RAG-8A2BE2?style=for-the-badge" />
<img src="https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge" />
<img src="https://img.shields.io/badge/LangGraph-000000?style=for-the-badge" />
<img src="https://img.shields.io/badge/HuggingFace-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black" />
<img src="https://img.shields.io/badge/LLM--as--Judge-6C47FF?style=for-the-badge" />

<br>

<img src="https://img.shields.io/badge/Qdrant-D63AFF?style=for-the-badge" />
<img src="https://img.shields.io/badge/ChromaDB-FF6B6B?style=for-the-badge" />
<img src="https://img.shields.io/badge/Prompt_Engineering-412991?style=for-the-badge" />

</div>

---

## 🧪 Machine Learning & Data

<div align="center">

<img src="https://skillicons.dev/icons?i=python&perline=10" />

<br><br>

<img src="https://img.shields.io/badge/Scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" />
<img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" />
<img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" />
<img src="https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge" />
<img src="https://img.shields.io/badge/XGBoost-FF6600?style=for-the-badge" />
<img src="https://img.shields.io/badge/SHAP-000000?style=for-the-badge" />

</div>

---

## ⚙️ Backend & APIs

<div align="center">

<img src="https://skillicons.dev/icons?i=python,fastapi,nodejs,express&perline=10" />

<br><br>

<img src="https://img.shields.io/badge/REST_APIs-02569B?style=for-the-badge" />
<img src="https://img.shields.io/badge/Microservices-FF6F00?style=for-the-badge" />
<img src="https://img.shields.io/badge/System_Design-5C2D91?style=for-the-badge" />

</div>

---

## 🌐 Frontend

<div align="center">

<img src="https://skillicons.dev/icons?i=react,nextjs,html,css,tailwind&perline=10" />

<br><br>

<img src="https://img.shields.io/badge/React_Native-61DAFB?style=for-the-badge&logo=react&logoColor=black" />
<img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white" />

</div>

---

## 🗄️ Databases & Caching

<div align="center">

<img src="https://skillicons.dev/icons?i=postgres,mongodb,redis&perline=10" />

<br><br>

<img src="https://img.shields.io/badge/Qdrant-D63AFF?style=for-the-badge" />
<img src="https://img.shields.io/badge/ChromaDB-FF6B6B?style=for-the-badge" />

</div>

---

## ☁️ Cloud & DevOps

<div align="center">

<img src="https://skillicons.dev/icons?i=docker,aws,github,git,linux&perline=10" />

<br><br>

<img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white" />
<img src="https://img.shields.io/badge/AWS_S3-569A31?style=for-the-badge&logo=amazonaws&logoColor=white" />
<img src="https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white" />
<img src="https://img.shields.io/badge/Render-46E3B7?style=for-the-badge&logo=render&logoColor=black" />

</div>

---

# 💻 Programming Languages

<div align="center">

<img src="https://skillicons.dev/icons?i=python,cpp,js,java&perline=10" />

<br><br>

<img src="https://img.shields.io/badge/SQL-336791?style=for-the-badge" />

</div>

---

# 🔬 What I'm Exploring

```text
                         AI SYSTEMS
                              │
        ┌─────────────────────┼─────────────────────┐
        │                     │                     │
       RAG              LLM RELIABILITY        ML SYSTEMS
        │                     │                     │
   Hybrid Search        Hallucination          Prediction
   Reranking            Detection              Evaluation
   Embeddings           Guardrails             Explainability
   Evaluation           Citations              Risk Scoring
        │                     │                     │
        └─────────────────────┼─────────────────────┘
                              │
                       PRODUCTION AI
                              │
             ┌────────────────┼────────────────┐
             │                │                │
            APIs           Caching         Deployment
             │                │                │
          FastAPI           Redis            Docker
             │                │                │
             └────────────────┼────────────────┘
                              │
                       SYSTEM DESIGN
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

### Bangalore Institute of Technology

**B.Tech in Computer Science Engineering**

📍 Bengaluru, India

**CGPA: 8.5/10**

`September 2023 – June 2027`

---

# 📚 Certifications

### Full Stack Generative & Agentic AI with Python — Udemy

* RAG pipelines with LangChain
* Vector databases
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

# 📊 GitHub Stats

<div align="center">

<img height="170" src="https://github-readme-stats.vercel.app/api?username=aaradhya177&show_icons=true&hide_border=true&count_private=true&rank_icon=github" />

<img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=aaradhya177&layout=compact&hide_border=true" />

</div>

---

# 🔥 Contribution Streak

<div align="center">

<img src="https://streak-stats.demolab.com?user=aaradhya177&hide_border=true" />

</div>

---

# 📫 Let's Connect

<div align="center">

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

</div>

---

<div align="center">

### 🚀 Building AI systems that are useful, measurable, and reliable.

</div>
```
