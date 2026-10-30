# recruit-agent

FastAPI service scaffold for recruitment agent workflows.

## Requirements

- Python 3.11+

## Setup

```bash
python -m venv .venv
source .venv/bin/activate
pip install -e ".[dev]"
cp .env.example .env
# Edit .env with your values
pre-commit install
```

## Run

```bash
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000
```

Health check: `GET http://localhost:8000/health`

## Quality checks

```bash
ruff check .
ruff format .
mypy --strict app tests
pytest
```
