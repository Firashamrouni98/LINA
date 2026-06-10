# 🤖 LINA — AI-Powered IT Infrastructure Management System

An intelligent IT infrastructure management system that transforms reactive operations into 
proactive, AI-driven workflows. Built with LangChain, LangGraph, FastAPI, and Milvus — 
LINA automates log analysis, remote server management, and network design through 
natural language interaction.

![Python](https://img.shields.io/badge/Python-3.11-blue)
![FastAPI](https://img.shields.io/badge/FastAPI-Backend-009688)
![LangChain](https://img.shields.io/badge/LangChain-Agents-orange)
![LangGraph](https://img.shields.io/badge/LangGraph-StatefulAI-purple)
![Milvus](https://img.shields.io/badge/Milvus-VectorDB-00C4CC)
![Docker](https://img.shields.io/badge/Docker-Containerized-2496ED)
![License](https://img.shields.io/badge/License-MIT-green)

---

## 🎯 What is LINA?

LINA is a multi-agent AI system designed to handle the complexity of modern IT infrastructure.
Instead of manually monitoring logs, SSHing into servers, or designing networks from scratch —
LINA lets you interact in natural language and handles the rest autonomously.

---

## 📌 Core Features

### 🔍 Log Analysis & Malfunction Detection
- Ingests logs from diverse sources in real-time
- Converts logs into vector embeddings stored in Milvus
- Detects anomalies by comparing against historical patterns
- Classifies issues by domain: network, server, application
- Generates plain-language summaries of complex log events
- Sends proactive alerts and detailed reports

### 🖥️ Remote Server Management
- Natural language command interpretation via LangGraph agents
- Secure SSH-based server access and task execution
- Supports shell scripts, file operations, and API interactions
- Real-time feedback and execution reporting
- Optional task scheduling for recurring maintenance

### 🌐 Network Design & Optimization Assistant
- Accepts network requirements as natural language input
- Generates optimal network designs: IP addressing, subnetting, VLANs
- Recommends device configuration, placement, and failover strategies
- Supports iterative refinement through interactive conversation
- Scalability and security recommendations included

---

## 🛠️ Tech Stack

| Layer | Technology | Purpose |
|---|---|---|
| Backend API | FastAPI | High-performance REST API |
| AI Orchestration | LangChain | LLM chaining and workflows |
| Agent State | LangGraph | Stateful multi-agent reasoning |
| Vector Database | Milvus | Log embeddings and similarity search |
| Message Broker | Redis | Async task queue and log pipeline |
| Containerization | Docker | Isolated, reproducible environments |
| Language | Python 3.11 | Core development |

---

## 🧠 System Architecture
User Input (Natural Language)
↓
FastAPI Backend
↓
LangGraph Multi-Agent Orchestrator
↙         ↓          ↘
Log Agent  Server Agent  Network Agent
↓           ↓              ↓
Milvus       SSH            LLM
(Vector DB)  (Remote)     (Reasoning)
↓           ↓              ↓
Anomaly    Task Execution  Design Output
Detection  + Reporting    + Recommendations
↘      ↓       ↙
Unified Response Layer
↓
User / Alert

---

## ⚙️ Installation

### Prerequisites
- Python 3.11+
- Docker & Docker Compose
- Milvus instance (local or cloud)
- Redis instance

### 1. Clone the repository
```bash
git clone https://github.com/Firashamrouni98/LINA.git
cd LINA
```

### 2. Create virtual environment
```bash
python -m venv venv
venv\Scripts\activate  # Windows
source venv/bin/activate  # Mac/Linux
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Configure environment variables
```bash
cp .env.example .env
# Edit .env with your API keys and service URLs
```

### 5. Start services with Docker
```bash
docker-compose up -d
```

### 6. Run the API
```bash
uvicorn main:app --reload
```

---

## 📁 Project Structure
LINA/
│
├── agents/                 # LangGraph agent definitions
│   ├── log_agent.py        # Log analysis agent
│   ├── server_agent.py     # Remote server management agent
│   └── network_agent.py    # Network design agent
│
├── api/                    # FastAPI routes
├── core/                   # LangChain chains and tools
├── db/                     # Milvus vector store integration
├── schemas/                # Pydantic models
├── docker-compose.yml      # Service orchestration
├── requirements.txt        # Dependencies
└── README.md

---

## 🔮 Future Improvements

- [ ] Web-based chat UI for non-technical users
- [ ] Integration with monitoring tools (Grafana, Prometheus)
- [ ] Support for Windows Server management
- [ ] Auto-remediation workflows for common failures
- [ ] Multi-tenant support for enterprise environments
- [ ] Network topology visualization

---

## 👤 Author

**Firas Hamrouni**  
Telecommunications Engineering Graduate | AI & ML Engineer  
Specialized in multi-agent systems, RAG pipelines, and LLM-powered automation

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://www.linkedin.com/in/firas-hamrouni-76177a277)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black)](https://github.com/Firashamrouni98)

---

## 📄 License

MIT License — free to use and modify.