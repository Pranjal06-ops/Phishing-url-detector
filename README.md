# Phishing URL Detector

ML-based phishing URL detector that extracts URL features and identifies phishing sites. Includes:

- REST API for predictions (Flask)
- Optional web interface 
- Dockerized deployment
- Reproducible data → model → deployment workflow

## Getting Started

### 1. Clone Repo
```
git clone <repo-link>
cd phishing-url-detector-full
```

### 2. Run locally
```
pip install -r deployment/requirements.txt
python src/api/app.py
```

### 3. Web interface
Open `webapp/index.html` in browser or deploy via GitHub Pages.

## Future Enhancements
- Connect live backend API
- Browser extension
- Continuous learning from new URLs
