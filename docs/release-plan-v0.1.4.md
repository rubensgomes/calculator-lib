# Release Plan v0.1.4

**Date:** 2026-02-23
**Repository:** rubensgomes/calculator-lib
**Previous Version:** 0.1.3
**New Version:** 0.1.4

## Summary of Changes

- Lowered minimum Python version requirement from `>=3.14` to `>=3.10.0` for broader compatibility
- Updated `poetry.lock` with latest dependency versions

## Release Checklist

- [x] Run `poetry run mypy src/` and fix any issues
- [x] Run `poetry run isort src/ tests/` and fix any issues
- [x] Run `poetry run black src/ tests/` and fix any issues
- [x] Run `poetry run pytest` and fix any issues
- [x] Run `export SOURCE_DATE_EPOCH=$(date +%s); poetry build -v` and fix any issues
- [x] Ensure `CHANGELOG.md` exists and update with v0.1.4 changes
- [x] Commit all changes to main, create tag v0.1.4, push, and create GitHub release
- [x] Run `poetry publish -v` to publish to PyPI
