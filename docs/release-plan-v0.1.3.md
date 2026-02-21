# Release Plan — v0.1.3

**Date:** 2026-02-20
**Repository:** rubensgomes/calculator-lib
**Current version:** 0.1.2 → **Target version:** 0.1.3

## Summary of Changes

- Expanded `.gitignore` with comprehensive ignore rules (Claude Code, Jupyter, AI/ML artifacts, secrets, OS files)
- Fixed minor typos in `LICENSE` (missing period, capitalized "Limitation of Liability")
- Simplified and updated `RELEASE.md` (removed outdated steps, corrected script references)
- Added new `SETUP.md` documentation file
- Updated `poetry.lock` with latest dependency versions
- Cleaned up `pyproject.toml`

## Release Steps

- [x] **Step 1:** Run `poetry run mypy src/` — type checking ✅
- [x] **Step 2:** Run `poetry run isort src/ tests/` — import sorting ✅
- [x] **Step 3:** Run `poetry run black src/ tests/` — code formatting ✅
- [x] **Step 4:** Run `poetry run pytest` — run test suite ✅
- [x] **Step 5:** Run `export SOURCE_DATE_EPOCH=$(date +%s); poetry build -v` — build package ✅
- [x] **Step 6:** Ensure `CHANGELOG.md` exists and update it with v0.1.3 changes ✅
- [x] **Step 7:** Bump version to 0.1.3 in `pyproject.toml` ✅
- [x] **Step 8:** Commit all changes, create `v0.1.3` tag, push to remote, create GitHub release ✅
- [x] **Step 9:** Run `poetry publish -v` — publish to PyPI ✅
