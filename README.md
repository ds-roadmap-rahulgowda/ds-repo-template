This template gives you:
- Poetry with `src/` layout
- pre-commit (ruff + black + hygiene hooks)
- GitHub Actions CI (lint + tests)
- A minimal package (`project_slug`) and a passing sanity test

## How to use
1. Click **Use this template** → create your repo.
2. Clone it locally and rename things:
   - In `pyproject.toml`: change `name = "project-template"` to your project name.
   - In `pyproject.toml`: update `packages = [{ include = "project_slug", from = "src" }]` to your package folder.
   - Rename folder `src/project_slug` → `src/<your_package>`.
   - Update tests/imports from `project_slug` → `<your_package>`.
3. Install & run:
```bash
poetry install
pre-commit install
pre-commit run --all-files
poetry run pytest -q
Push and check the Actions tab (should be green).
