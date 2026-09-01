# AegisAI Guardrails — Enterprise LLM Safety & Red-Teaming Gateway

AegisAI Guardrails is a production-grade security and observability gateway for Large Language Models (LLMs). It provides sub-millisecond prompt injection defenses, PII/PHI automated entity redaction, RAG hallucination and context relevance evaluation, and compliance arbitration conforming to the NIST AI Risk Management Framework and EU AI Act.

---

## Dependencies

* **Runtime**: Python 3.10+
* **Core Framework**: FastAPI, Uvicorn, Pydantic v2
* **Quality & Test**: Pytest, Pytest-cov
* **Frontend Dashboard**: HTML5 / ES6 Vanilla Client, Web Audio Alerts

---

## Installation

### 1. Set Up Python Virtual Environment
```bash
git clone git@github.com:gandhikomarala/aeges.git
cd aeges
python -m venv venv
# Windows:
.\venv\Scripts\activate
# Linux/macOS:
source venv/bin/activate
```

### 2. Install Project Dependencies
```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

---

## Build

Build containerized production image locally:
```bash
docker build -t aegisai-guardrails:latest .
```

---

## Run

### Microservice Execution
```bash
python -m uvicorn Backend.main:app --host 0.0.0.0 --port 8000 --reload
```

### Containerized Deployment
```bash
docker-compose up -d --build
```

### Static Dashboard UI
```bash
python -m http.server 8000
```

---

## Usage

1. Open `http://localhost:8000` or the live GitHub Pages portal.
2. Configure active safety threshold levels (Low, Medium, High, Strict).
3. Test adversarial prompts (Jailbreaks, PII exfiltration, hallucination traps) in real-time.

---

## Testing

Execute the automated test suite with coverage report:
```bash
pytest tests/ -v
```
