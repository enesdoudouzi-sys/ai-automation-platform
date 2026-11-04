# Backend API

## Requirements

- Python 3.11+
- pip

## Local setup

Run from the repository root:

    python -m venv .venv
    source .venv/bin/activate
    # Windows PowerShell: .venv\\Scripts\\Activate.ps1
    pip install -r backend/requirements.txt

## Start the API

    uvicorn app.main:app --app-dir backend --reload

- API root: http://127.0.0.1:8000/
- Health check: http://127.0.0.1:8000/api/v1/health
- Interactive API docs: http://127.0.0.1:8000/docs

## Run tests

    PYTHONPATH=backend pytest backend/tests -q
