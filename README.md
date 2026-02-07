# APP-Testing-

I use this app-focused repository to validate what I build, test route behavior, and keep legacy compatibility checks in one place.

## Included

- `aca/` Flask learning app
- `aca/test_all_features.py` test suite
- `aca/legacy_sources/deep_audit_checks.py` deep compatibility checks

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
