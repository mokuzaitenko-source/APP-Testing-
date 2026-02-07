# ACA Web App

Interactive Python learning platform built with Flask.

## Features

- Structured learning paths and lesson pages
- In-browser Python code execution with formatted output
- Progress tracking across lessons
- Responsive interface for desktop and mobile

## Run Locally

```powershell
cd aca
pip install -r requirements.txt
python app.py
```

Open `http://localhost:5000`.

## Test

```powershell
cd aca
$env:PYTHONIOENCODING='utf-8'
python test_all_features.py
```

## Project Structure

```text
aca/
  app.py
  progress.py
  requirements.txt
  templates/
  static/
  test_all_features.py
```

## Notes

This app is intentionally local-first and optimized as a portfolio project for interview walkthroughs.
