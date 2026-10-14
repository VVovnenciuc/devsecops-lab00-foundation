# DevSecOps Lab 00 — Secure Foundation

Repo de bază pentru portofoliul DevSecOps: un CLI Python (`headercheck`) care verifică
header-ele HTTP de securitate, construit cu controale de securitate „shift-left”.

## Controale de securitate implementate
- Commit-uri semnate (SSH) + regulă de branch care le impune
- Pre-commit: gitleaks (secrete), ruff (lint/format), detect-private-key
- CI GitHub Actions cu `permissions: contents: read`, acțiuni fixate pe SHA
- Audit de dependențe (pip-audit) pe lock file cu hash-uri
- Lint de securitate pentru workflow-uri (zizmor)
- Dependabot (Python + GitHub Actions), secret scanning + push protection

## Utilizare

uv sync
uv run headercheck https://example.com

Exit codes: `0` = toate header-ele prezente, `1` = lipsesc header-e, `2` = eroare.

## Ce aș face diferit în producție
_(se completează la finalul lab-ului)_
