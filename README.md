# Phishing URL Detector
# 🛡️ Phishing URL Detector (ML-Based)

An intelligent, machine learning–powered system that detects phishing URLs by extracting and analyzing key lexical and structural features. Designed for security research, browser safety tools, and automated threat detection workflows.

<div align="center">

| API | Web UI | Docker | ML Pipeline |
|----|----|----|----|
| ✅ | ✅ | ✅ | ✅ |

</div>

---

## 🌍 Overview

Phishing attacks are one of the most common cybersecurity threats, often delivered through malicious links that appear legitimate.  
This project provides an **ML-based phishing URL detection system** that predicts whether a URL is safe or harmful — in real time.

The system is:
- **Accurate** — trained on real-world phishing & benign datasets  
- **Fast** — lightweight inference suitable for real-time use  
- **Deployable** — run locally, via REST API, web UI, or Docker  

---

## ✨ Features

- 🔍 **URL Feature Extraction** — lexical & structural analysis
- 🤖 **Machine Learning Model** — phishing vs. legitimate classification
- 🌐 **REST API (Flask)** — integrates easily with apps and browser extensions
- 💻 **Optional Web Interface** — simple UI for manual checks
- 🐳 **Dockerized Deployment** — production-friendly
- 🔁 **Reproducible Workflow** — data → features → training → deployment

---

## 🗂️ Project Structure

phishing-url-detector-full/
│
├── src/
│ ├── data/ # Data loading & preprocessing
│ ├── features/ # URL feature extraction scripts
│ ├── models/ # Model training & evaluation
│ └── api/ # Flask REST API
│
├── models/ # Saved trained models
├── webapp/ # (Optional) front-end interface
├── tests/ # Unit tests
└── deployment/
└── requirements.txt # Python dependencies

---

## 🚀 Getting Started

### Prerequisites
- Python 3.9+
- pip
- (Optional) Docker & docker-compose

### Local Setup

```bash
git clone <repo-link>
cd phishing-url-detector-full
pip install -r deployment/requirements.txt
python src/api/app.py

API will start at: http://localhost:5000

Test a prediction: curl -X POST "http://localhost:5000/predict" \
  -H "Content-Type: application/json" \
  -d '{"url": "http://example-verify-login-security.com"}'

🌐 Optional Web UI: python -m http.server 8000 --directory webapp
Then open: http://localhost:8000
🐳 Docker Deployment: docker build -t phishing-detector .
docker run -p 5000:5000 phishing-detector
🧪 Testing & Code Quality:
 pytest -q
black .
flake8 src tests


