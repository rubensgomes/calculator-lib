# Release Plan v0.1.5

**Date:** 2026-02-26
**Repository:** rubensgomes/calculator-lib
**Previous Version:** 0.1.4
**New Version:** 0.1.5

## Summary of Changes

- Adopted the Google Python Style Guide as the project coding standard
- Converted all docstrings from RST markup to Google-style plain text
- Added missing module and class docstrings for pylint compliance
- Updated `.pylintrc` to disable `redefined-outer-name` (standard pytest fixture pattern)
- Updated `CLAUDE.md` to document the Google Python Style Guide convention

## Release Checklist

- [x] Run `poetry run mypy src/` and fix any issues
- [x] Run `poetry run isort src/ tests/` and fix any issues
- [x] Run `poetry run black src/ tests/` and fix any issues
- [x] Run `poetry run pytest` and fix any issues
- [x] Run `export SOURCE_DATE_EPOCH=$(date +%s); poetry build -v` and fix any issues
- [x] Ensure `CHANGELOG.md` exists and update with v0.1.5 changes
- [x] Commit all changes to main, create tag v0.1.5, push, and create GitHub release
- [x] Run `poetry publish -v` to publish to PyPI
