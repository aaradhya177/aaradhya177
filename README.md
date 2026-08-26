# Aaradhya Mehra

**CS Student @ BIT Bengaluru · Full-Stack & AI/ML Developer · Hackathon Builder**

I build and ship production-grade software — from AI-powered drug discovery pipelines to multi-service athlete intelligence platforms. Currently in my 7th semester (CGPA: 8.5/10), targeting AI/ML and SWE internships where engineering depth matters.

---

## Tech Stack

<table>
  <tr>
    <td align="center"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" width="40" height="40"/><br/>Java</td>
    <td align="center"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" width="40" height="40"/><br/>Python</td>
    <td align="center"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/cplusplus/cplusplus-original.svg" width="40" height="40"/><br/>C++</td>
    <td align="center"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" width="40" height="40"/><br/>JavaScript</td>
    <td align="center"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" width="40" height="40"/><br/>React</td>
    <td align="center"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nextjs/nextjs-original.svg" width="40" height="40"/><br/>Next.js</td>
    <td align="center"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg" width="40" height="40"/><br/>Node.js</td>
    <td align="center"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/fastapi/fastapi-original.svg" width="40" height="40"/><br/>FastAPI</td>
    <td align="center"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" width="40" height="40"/><br/>HTML5</td>
    <td align="center"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" width="40" height="40"/><br/>CSS3</td>
    <td align="center"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tailwindcss/tailwindcss-original.svg" width="40" height="40"/><br/>Tailwind</td>
    <td align="center"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original.svg" width="40" height="40"/><br/>PostgreSQL</td>
    <td align="center"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mongodb/mongodb-original.svg" width="40" height="40"/><br/>MongoDB</td>
    <td align="center"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/firebase/firebase-plain.svg" width="40" height="40"/><br/>Firebase</td>
    <td align="center"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/redis/redis-original.svg" width="40" height="40"/><br/>Redis</td>
    <td align="center"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg" width="40" height="40"/><br/>Docker</td>
    <td align="center"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" width="40" height="40"/><br/>Git</td>
    <td align="center"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg" width="40" height="40"/><br/>GitHub</td>
    <td align="center"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linux/linux-original.svg" width="40" height="40"/><br/>Linux</td>
    <td align="center"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/amazonwebservices/amazonwebservices-original-wordmark.svg" width="40" height="40"/><br/>AWS</td>
    <td align="center"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vercel/vercel-original.svg" width="40" height="40"/><br/>Vercel</td>
    <td align="center"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tensorflow/tensorflow-original.svg" width="40" height="40"/><br/>TensorFlow</td>
    <td align="center"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/scikitlearn/scikitlearn-original.svg" width="40" height="40"/><br/>scikit-learn</td>
    <td align="center"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/pandas/pandas-original.svg" width="40" height="40"/><br/>Pandas</td>
    <td align="center"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/numpy/numpy-original.svg" width="40" height="40"/><br/>NumPy</td>
  </tr>
</table>

---

## 🚀 Featured Projects

### 🤖 Support Knowledge Copilot — Verified RAG Support Assistant
[Source →](https://github.com/aaradhya177/Build-citation-verified-RAG-copilot)

A RAG-based support assistant that answers questions from internal documentation with **verified, hallucination-checked citations**.

- Built a **hybrid retrieval pipeline** combining dense embeddings and BM25 using Reciprocal Rank Fusion, improving accuracy from **72% → 88%**.
- Added **LLM-as-Judge** verification to ensure citations actually support generated claims.
- Implemented **confidence scoring and no-answer detection** to prevent unreliable responses.
- Evaluated retrieval and answer quality using a **50–75 question golden evaluation set**.
- Deployed with **FastAPI + Streamlit + Docker**.

`Python` `FastAPI` `RAG` `BM25` `Embeddings` `LLM-as-Judge` `Streamlit` `Docker`

---

### ⚡ Semantic Cache Gateway — LLM Cost & Latency Optimizer
[Source →](https://github.com/aaradhya177/Build-semantic-cache-gateway)

An embedding-based caching proxy that detects **semantically similar LLM requests** and reuses existing responses to reduce unnecessary API calls.

- Built an **embedding-based semantic caching layer** using vector similarity search.
- Reduced simulated LLM API cost by **40%** and P95 latency by **65%**.
- Validated cache correctness across **2,000 requests**.
- Added **similarity threshold tuning and LLM-as-Judge validation** to prevent incorrect cache hits.
- Designed **policy tags and TTL rules** to prevent cross-user leakage and stale responses.
- Load-tested the FastAPI proxy using **Locust**, with Redis and a vector-store backend.

`Python` `FastAPI` `Qdrant` `ChromaDB` `Redis` `Embeddings` `LLM-as-Judge` `Locust` `Docker`

## Achievements

- 🥈 **2nd Place — Augmentix Hackathon, NMIT Bangalore** — Built MolGenix with a 3-person team in 36 hours; owned the FastAPI backend, DeepChem integration, and docking pipeline end to end
- 🏆 **Smart India Hackathon — Internal Qualifier** — Shortlisted at BIT for a federated learning solution; led architecture design and presented to faculty judges
- 💻 **Competitive Programming** — Active on Codeforces and LeetCode; strong in graphs, DP, trees
- 👥 **Under 25 Community** — Managed a team of 8; restructured content strategy, contributing to a 35% engagement increase in one quarter

---

## What I'm Working On

- Shipping the **InjuryGuard ML pipeline** as the first production module of Eklavya
- Building **HoldIt** end-to-end with a clean, backend-first approach
- Deepening expertise in LLMs, RAG pipelines, and AI system design

---

## Open To

AI/ML internships · SWE internships · Hackathon collaborations · Technical conversations on system design and AI engineering

---

## Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/aaradhya-mehra-07a46537b/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)](https://github.com/aaradhya177)
[![Email](https://img.shields.io/badge/Email-D14836?style=flat&logo=gmail&logoColor=white)](mailto:aaradhyamehra240@gmail.com)
[![Codeforces](https://img.shields.io/badge/Codeforces-1F8ACB?style=flat&logo=codeforces&logoColor=white)](https://codeforces.com/profile/YoullNeverCodeAlone17)
