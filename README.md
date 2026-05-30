# Hi there, I'm Shivnarain Sarin 👋

<div align="center">

### AI Engineer & Researcher

</div>

---

## 🚀 About Me

I'm an AI engineer building systems that reason, plan, and learn, from language model architecture research to autonomous agentic pipelines. Background in electrical engineering and full-stack development.

- Researching **language model architectures**: state space models, masked diffusion, attention mechanisms, and optimizers
- Building **Agentic AI**, **LLM applications**, **Deep Learning**, and **Reinforcement Learning** systems
- Training models from scratch on HPC clusters and shipping production full-stack AI products
- Fun fact: Built an autonomous research agent that discovers papers, runs experiments in Docker sandboxes, and writes weekly reports!

---

## 🛠️ Technical Skills

### Languages
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)

### AI/ML & Deep Learning
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)
![CUDA](https://img.shields.io/badge/CUDA-76B900?style=for-the-badge&logo=nvidia&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)
![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6F61?style=for-the-badge&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)

### Frameworks & Infrastructure
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonwebservices&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

---

## 🔥 Featured Projects

### 🧬 [DiffMamba](https://github.com/shivnarainms22/DiffMamba)
**Masked Diffusion LM Architecture Study | Mamba-2 | PyTorch | A100 HPC**

Controlled reproduction study replacing the Transformer/DiT denoiser in masked diffusion language models (MDLM) with a bidirectional Mamba-2 backbone.

- Trained **5 models (50M to 130M params)** on OpenWebText on an A100 HPC cluster, with hypothesis pinning before results collection
- Full ablation: 130M Transformer vs BiMamba-2 (val PPL 70.45 vs 85.91), scaling study, and LR fairness sweep
- Retrained 130M BiMamba at tuned LR (val PPL 79.26), closing **43% of the quality gap**
- Inference benchmark showing **3.12x throughput speedup** over flash-attn DiT at 32K tokens, reproducing DiffuApriel (arXiv 2511.15927) at small scale

**Tech Stack:** Python • PyTorch • Mamba-2 • MDLM • Flash-Attn • SLURM

---

### 🧠 [TinyLM](https://github.com/shivnarainms22/TinyLM)
**275M Parameter Language Model from Scratch | MLA + Muon | PyTorch**

A 275M parameter language model trained from scratch with Multi-head Latent Attention (MLA) and the Muon optimizer, benchmarked against TinyLlama-1.1B.

- Implemented **Multi-head Latent Attention** and the **Muon optimizer** (Newton-Schulz orthogonalization)
- Trained on **1B tokens** of FineWeb-Edu (20k steps); published to [Hugging Face](https://huggingface.co/Shiv-22/tinylm)
- **53.8% on ARC-Easy**, within 1.9% of TinyLlama-1.1B at roughly 4x fewer parameters
- Full training run tracked on Weights & Biases

**Tech Stack:** Python • PyTorch • Hugging Face • WandB • SLURM

---

### 🔬 [Research Agent](https://github.com/shivnarainms22/Research-Agent)
**Autonomous Research Pipeline | Claude API | Docker**

Autonomous research system that discovers papers from arXiv and Semantic Scholar, analyzes them with AI, runs experiments in Docker sandboxes or Modal cloud GPUs, and generates weekly narrative reports.

- Built a **5-stage pipeline**: Ingestion → Synthesis → Experiments → Analysis → Reporting
- Maintains a **knowledge graph** (NetworkX) with **hybrid retrieval** (BM25 + vector RRF)
- Experiment **safety gates**: AST validation, Bandit scan, auto-fix, human approval, Docker isolation
- Statistical analysis with **confidence intervals**, **t-tests**, and **Cohen's d**
- **Streamlit web UI**, **Typer CLI**, and **APScheduler daemon** for automated research cycles

**Tech Stack:** Python • Claude API • ChromaDB • Docker • Modal • Streamlit • NetworkX • SQLite

---

### 🎙️ [TM Pro](https://github.com/shivnarainms22/TM-Pro)
**Real-Time AI Meeting Copilot | Next.js | Dual-Stream Capture**

Real-time AI meeting copilot that captures both sides of a web meeting, transcribes each stream independently, and surfaces context-aware suggestions live.

- **Dual-stream capture**: microphone and browser tab audio on two parallel MediaRecorder pipelines, flushed and transcribed concurrently every 30s
- **Speaker-labeled transcription** (You / Them) via Groq Whisper Large V3
- **Context-aware suggestions** every 30s using speaker attribution, recency bias, type diversity, and anti-repetition prompting
- Streaming answers via native **fetch + Web Streams SSE** through Next.js API routes, with two Zustand stores and typed per-stream error handling

**Tech Stack:** TypeScript • Next.js • Tailwind CSS • Zustand • Groq API • Web Streams

---

## 🎓 Education

**Northeastern University** | *Master of Science in Artificial Intelligence*
📍 San Jose, CA | Sep 2025 – May 2027

**APJ Abdul Kalam Technological University** | *Bachelor of Technology in Electrical & Electronics Engineering*
📍 Kerala, India | Oct 2020 – May 2024

---

## 📫 Let's Connect!

<div align="center">

[![Portfolio](https://img.shields.io/badge/Portfolio-shivnarainms22.github.io-000000?style=for-the-badge&logo=github-pages&logoColor=white)](https://shivnarainms22.github.io/Portfolio/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Shivnarain_Sarin-0077B5?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/shivnarain-sarin-3a5277269/)
[![Hugging Face](https://img.shields.io/badge/Hugging%20Face-Shiv--22-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)](https://huggingface.co/Shiv-22)
[![Email](https://img.shields.io/badge/Email-shivnarainms22%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:shivnarainms22@gmail.com)

---

</div>
