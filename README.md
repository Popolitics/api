# api

REST API, business logic, agrégation des services internes.

Django + Django REST Framework, géré avec [uv](https://docs.astral.sh/uv/).

## Setup

```bash
uv sync
cp .env.example .env    # ajuster DJANGO_SECRET_KEY et le reste au besoin
git config core.hooksPath .githooks   # active les hooks locaux (une fois)
uv run python manage.py migrate
uv run python manage.py runserver
```

`GET /api/health/` → `{"status": "ok"}`
