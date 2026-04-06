# Release Plan v0.1.6

## Overview

- **Version:** 0.1.6
- **Date:** 2026-04-05
- **Description:** Update Python version requirement, add tool configurations, update dev dependencies, and refresh documentation

## Changes in this Release

### Changed

- Updated `requires-python` from `>=3.10.0` to `>=3.12.0,<4.0.0`
- Added `[tool.black]`, `[tool.isort]`, `[tool.mypy]`, `[tool.pytest.ini_options]` configurations to `pyproject.toml`
- Added `[tool.poe.tasks]` clean tasks to `pyproject.toml`
- Updated dev dependency versions (`black`, `coverage`, `pytest-cov`) and added `pytest-asyncio`
- Sorted dev dependencies alphabetically in `pyproject.toml`
- Updated `CLAUDE.md` to reflect Python >= 3.12, Black line-length 80, and consolidated docs listing
- Updated `README.md` badges and requirements to Python 3.12+
- Updated `.claude/commands/release-plan.md` to include documentation update step

## Release Steps

- [x] 1. Run `poetry run mypy src/` and fix any issues
- [x] 2. Run `poetry run isort src/ tests/` and fix any issues
- [x] 3. Run `poetry run black src/ tests/` and fix any issues
- [x] 4. Run `poetry run pytest` and fix any issues
- [x] 5. Run `export SOURCE_DATE_EPOCH=$(date +%s); poetry build -v` and fix any issues
- [x] 6. Ensure `CHANGELOG.md` exists and update with current release changes
- [x] 7. Commit all changes, create version tag, push, and create GitHub release
- [x] 8. Run `poetry publish -v` to publish to PyPI
