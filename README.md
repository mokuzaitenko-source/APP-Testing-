# APP-Testing-

I use this app-focused repository to validate what I build, test route behavior, and keep legacy compatibility checks in one place.

## Included

- `aca/` Flask learning app
- `aca/test_all_features.py` test suite
- `aca/legacy_sources/deep_audit_checks.py` deep compatibility checks

## Validation Scope

- Main app route checks
- Lesson rendering checks
- Code execution endpoint checks
- Legacy source compatibility checks
- Compile/import validation across active and legacy modules

## Run

```powershell
cd aca
pip install -r requirements.txt
python app.py
```

## Test

```powershell
cd aca
$env:PYTHONIOENCODING='utf-8'
python test_all_features.py
python legacy_sources/deep_audit_checks.py
```

## What This Proves

- The app is runnable and testable in a repeatable way.
- Legacy sources are preserved without breaking current behavior.
- QA workflow is documented for review and handoff.
