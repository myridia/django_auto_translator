# AGENTS.md — django_auto_translator

## What this is
Django package to auto-translate `.po` translation files using deep-translator (Google Translate).

## Stack
- Python (>=3.8)
- Django
- deep-translator
- polib
- Hatchling (build)

## Build
```bash
pip install -e .
```

## Run
Add to `INSTALLED_APPS`, then:
```bash
python manage.py translate_messages
```

## Structure
- `src/django_auto_translator/` — Django management command
- `tests/` — test suite
- `pyproject.toml` — build config
- `requirements.txt` — dependencies

## Conventions
- No comments in code unless asked.
- Verify: `python -m py_compile src/django_auto_translator/*.py`
