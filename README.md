# ACA Learning Platform

[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Flask-3.0-black?logo=flask)](https://flask.palletsprojects.com/)
[![Status](https://img.shields.io/badge/Portfolio-Interview%20Ready-1f883d)](#)

Portfolio project that combines deep-learning coursework with a production-style learning app.

## Demo

![Project banner](assets/banner.png)

## What this shows

- End-to-end engineering ownership: backend, frontend, tests, and docs
- Applied Python and automation skills in a real runnable product
- Practical architecture decisions around safety, usability, and maintainability

## Core Projects

1. `aca/` - Flask learning platform with in-browser Python execution and progress tracking
2. `DeepLearning_Roadmap.ipynb` - study and implementation roadmap
3. `ACA_v4.2_CapabilityPolicy.json` - policy artifact from ACA work
4. `ACA_v4.2_SchemaRegistry.yaml` - schema contract artifact from ACA work

## Tech Stack

- Python, Flask, Flask-WTF
- HTML, CSS, JavaScript
- Jupyter notebooks
- Automated app checks with Flask test client

## Quick Start

```powershell
cd aca
pip install -r requirements.txt
python app.py
```

Open `http://localhost:5000`.

## Run Tests

```powershell
cd aca
$env:PYTHONIOENCODING='utf-8'
python test_all_features.py
```

## Recruiter Notes

- Built modular route and template architecture for maintainable lesson delivery
- Implemented server-side execution flow for user code with robust error handling
- Added progress persistence and feature-level integration checks
- Documented setup, test flow, and project map for fast reviewer onboarding

## Repository Map

- `aca/app.py` - app routes and execution endpoints
- `aca/progress.py` - learning progress logic
- `aca/templates/` - UI templates
- `aca/static/` - frontend assets
- `aca/test_all_features.py` - integration-style checks
- `PORTFOLIO_ASSETS.md` - resume and interview copy
- `PROJECT_SHOWCASE.md` - curated list of best projects from this machine

## Next Improvements

- Add auth and user accounts
- Add secure execution sandbox hardening
- Add CI badges for test and lint status
- Add live hosted demo URL
