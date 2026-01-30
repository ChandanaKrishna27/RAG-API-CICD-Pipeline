# RAG API CI/CD Pipeline with Docker, Kubernetes, and GitHub Actions

<p align="center">
  <img src="RAG-API.png" alt="CI/CD Architecture" width="750"/>
</p>


This project demonstrates a complete end-to-end CI/CD pipeline for a Retrieval-Augmented Generation (RAG) API.  
The pipeline automates testing, containerization, and validation of an AI-powered API using modern DevOps practices.

The system is designed to ensure data quality, reproducibility, and reliable deployments for AI workloads by combining containerization, Kubernetes, and automated CI workflows.

---

## 📌 Project Overview

The objective of this project was to build a production-style AI API and automate its testing and validation workflow.

With this pipeline in place:

- The RAG API answers questions using a custom knowledge base
- Docker ensures the application runs consistently across environments
- Kubernetes enables scalable container deployment
- GitHub Actions automatically tests changes before deployment
- Data quality issues are caught early through semantic testing

---

## 🛠️ Tools & Technologies Used

- **FastAPI** – API framework
- **Uvicorn** – ASGI server
- **ChromaDB** – Vector database for document retrieval
- **Ollama (tinyllama)** – Local LLM inference
- **Docker** – Containerization
- **Kubernetes** – Container orchestration
- **GitHub Actions** – CI/CD automation
- **GitHub** – Source code management
- **Python** – Application and test development

---

## ⚙️ CI/CD Pipeline Breakdown

### API & Retrieval Layer
- Documents embedded into ChromaDB
- Queries retrieve relevant context from the knowledge base
- LLM generates responses using retrieved context
- Mock LLM mode added for deterministic testing

### Testing Stage
- Semantic tests validate answer quality instead of exact text
- Tests verify presence of required concepts in responses
- Mock mode ensures consistent test results without LLM randomness

### CI Automation
- GitHub Actions workflow triggered on:
  - Knowledge base updates
  - API logic changes
  - Embedding script changes
- Workflow performs:
  - Dependency installation
  - Embedding rebuild
  - API startup in mock mode
  - Automated semantic tests

  <p align="center">
  <img src="GitHub Actions.png" alt="GitHub Actions" width="750"/>
</p>

---

## 🏗️ Containerization & Deployment

- API packaged into a Docker image
- Containerized API runs identically across environments
- Kubernetes used to deploy and manage containers
- Enables scalability and production-style deployment

  <p align="center">
  <img src="ci-cd-architecture.png" alt="Kubernetes Deployment" width="750"/>
</p>

---

## ✅ Final Result

The RAG API successfully:
- Responds to queries using multiple documents
- Runs consistently in Docker containers
- Deploys through Kubernetes
- Automatically validates data quality through CI

CI pipelines reliably catch data quality issues before deployment, ensuring stable and trustworthy AI behavior.

---

## 📚 What I Learned

- Building a RAG API using FastAPI and vector search
- Handling LLM non-determinism in automated testing
- Designing semantic tests for AI systems
- Implementing mock modes for reliable CI/CD
- Containerizing AI workloads with Docker
- Deploying and managing containers with Kubernetes
- Automating quality checks using GitHub Actions
- Applying DevOps practices to AI applications

---

## 🎯 Why This Project Matters

This project reflects real-world AI + DevOps workflows:

- Automated validation for AI systems
- Deterministic testing for non-deterministic models
- Scalable and containerized deployments
- CI pipelines that protect data quality
- Production-ready design for AI services

---

## 👤 Author

**Chandana Krishna**  
Cloud & DevOps Enthusiast
