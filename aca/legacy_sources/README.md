# Legacy Sources Guide

This folder preserves additional source files discovered on this machine.

## What This Folder Is

`legacy_sources/` is a historical bundle of earlier app variants and support utilities.
It is kept for:

- traceability (what was built previously),
- comparison (old vs current implementation),
- reference during debugging and feature recovery.

The active app entry points are still outside this folder:

- `app.py` (main Flask app),
- `UnifiedApp.py` (desktop base),
- `ModernUnifiedApp.py` (desktop modern UI).

## Files and Purpose

- `UnifiedApp_desktop.py`
Desktop all-in-one app (Tkinter) with code execution, templates, and helper tools.

- `UnifiedApp_Modern_desktop.py`
Modernized UI variant of the desktop app. Updated to import `UnifiedApp_desktop.py` in this folder.

- `PyLearn_app.py`
Flask web app variant with learning paths and an `/execute` endpoint.

- `Launch_Python_Learning_desktop.bat`
Windows launcher script. Updated to use local folder paths and run `PyLearn_app.py`.

- `aca-unified-assistant.py`
Assistant/coach utility with ACA-copilot integrations and study helpers.

## File Matrix (What They Are + When To Use)

- `UnifiedApp_desktop.py`
Type: Legacy desktop application.
Use when: You want the original all-in-one Tkinter workflow.
Depends on: local files/templates in this repo.
Status: Imports/compiles successfully.

- `UnifiedApp_Modern_desktop.py`
Type: Legacy desktop UI variant.
Use when: You want a modernized desktop layout from the legacy branch.
Depends on: `UnifiedApp_desktop.py`.
Status: Import path repaired; imports/compiles successfully.

- `PyLearn_app.py`
Type: Legacy Flask web app variant.
Use when: You need the older lesson/path flow for comparison with `app.py`.
Depends on: shared templates under `aca/templates`.
Status: Route compatibility fixed; smoke tests passing.

- `Launch_Python_Learning_desktop.bat`
Type: Windows launcher for legacy Flask app.
Use when: You want one-click local startup on Windows.
Depends on: local Python (and optional `.venv`).
Status: Hardcoded path removed; now script-relative.

- `aca-unified-assistant.py`
Type: Support assistant/coaching utility script.
Use when: You want ACA-copilot integrated helper flows.
Depends on: external/local `aca-copilot` assets.
Status: Imports successfully; advanced features require external files.

- `deep_audit_checks.py`
Type: Automated validation script.
Use when: You want one command to verify main + legacy code health.
Depends on: project Python environment and local app files.
Status: Exit code `0` on success.

- `DEEP_AUDIT_REPORT.md`
Type: Validation report.
Use when: You need a written record of findings/fixes for reviewers.

## How to Run

### 1) Legacy Flask app

```powershell
cd legacy_sources
python PyLearn_app.py
```

Open `http://127.0.0.1:5000`.

### 2) Legacy desktop app

```powershell
cd legacy_sources
python UnifiedApp_desktop.py
```

### 3) Legacy modern desktop UI

```powershell
cd legacy_sources
python UnifiedApp_Modern_desktop.py
```

### 4) Legacy launcher (Windows)

```powershell
cd legacy_sources
.\Launch_Python_Learning_desktop.bat
```

## Notes

- These files are preserved for traceability and portfolio history.
- Main active implementations remain at repo root (`UnifiedApp.py`, `ModernUnifiedApp.py`, `app.py`).
- `aca-unified-assistant.py` may require additional local files (`aca-copilot` folder) to use all features.
- Deep technical validation details are in `legacy_sources/DEEP_AUDIT_REPORT.md`.
- Automated deep checks can be run with `python legacy_sources/deep_audit_checks.py`.
- This folder is intentionally preserved history; avoid treating it as the primary app entrypoint.

## Fixes Applied During Import

- `UnifiedApp_Modern_desktop.py`: fixed import to use `UnifiedApp_desktop.py` in this folder.
- `Launch_Python_Learning_desktop.bat`: removed hardcoded absolute path; now runs from local folder.
- `PyLearn_app.py`: added missing progress metadata expected by templates.
- `PyLearn_app.py`: added compatibility route alias for `lesson_view` endpoint.
