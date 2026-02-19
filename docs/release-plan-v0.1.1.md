# Release Plan - calculator-lib-rubens v0.1.1

**Date:** 2026-02-18
**Author:** Rubens Gomes
**Repository:** rubensgomes/calculator-lib

## Release Summary

Patch release updating project metadata, documentation, and dependency versions.

### Changes

- Renamed distribution from `calculator-lib` to `calculator-lib-rubens` for PyPI uniqueness
- Updated `pyproject.toml` with keywords, MIT license classifier, and bumped uvicorn dependency
- Updated `README.md` with correct distribution name, fixed license reference, and improved commands section
- Updated `CLAUDE.md` with distribution name, repository link, expanded project structure, and release process section
- Updated `llms.txt` with correct distribution name, installation instructions, categorized API sections, and error handling examples
- Updated `poetry.lock` with latest dependency versions

## Release Checklist

- [x] 1. Run GitHub connectivity test (`scripts/test_github.sh rubensgomes/calculator-lib`) - **PASSED** (8/8 tests)
- [x] 2. Run `poetry run mypy src/` - **PASSED** (no issues in 2 files)
- [x] 3. Run `poetry run isort src/ tests/` - **PASSED** (no changes needed)
- [x] 4. Run `poetry run black src/ tests/` - **PASSED** (4 files unchanged)
- [x] 5. Run `poetry run pytest` - **PASSED** (62 tests passed)
- [x] 6. Run `poetry build -v` - **PASSED** (built sdist and wheel)
- [ ] 7. Run `poetry publish -v` - **PENDING** (awaiting final approval)
- [x] 8. Update `CHANGELOG.md` with v0.1.1 changes - **DONE**
- [x] 9. Save release plan to `docs/` - **DONE**
