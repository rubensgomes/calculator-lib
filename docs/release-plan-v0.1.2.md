# Release Plan - calculator-lib-rubens v0.1.2

**Date:** 2026-02-18
**Author:** Rubens Gomes
**Repository:** rubensgomes/calculator-lib

## Release Summary

Patch release with improved documentation: enhanced README with badges, API reference tables, categorized usage examples, and error handling section. Updated CLAUDE.md project structure and release plan command.

### Changes

- Improved `README.md` with PyPI/license badges, API reference tables, categorized usage examples, and error handling section
- Updated `CLAUDE.md` to include v0.1.1 release plan in project structure
- Updated `.claude/commands/release-plan.md` to create NEW release plans
- Updated `llms.txt` with minor formatting fixes
- Updated `pyproject.toml` version bump to 0.1.2

## Release Checklist

- [x] 1. Run GitHub connectivity test (`scripts/test_github.sh rubensgomes/calculator-lib`) - **PASSED** (8/8 tests)
- [x] 2. Run `poetry run mypy src/` and fix any issues - **PASSED** (no issues in 2 files)
- [x] 3. Run `poetry run isort src/ tests/` and fix any issues - **PASSED** (no changes needed)
- [x] 4. Run `poetry run black src/ tests/` and fix any issues - **PASSED** (4 files unchanged)
- [x] 5. Run `poetry run pytest` and fix any issues - **PASSED** (62 tests passed)
- [x] 6. Run `export SOURCE_DATE_EPOCH=$(date +%s); poetry build -v` and fix any issues - **PASSED** (built sdist and wheel for 0.1.2)
- [x] 7. Ensure `CHANGELOG.md` exists and update with v0.1.2 changes - **DONE**
- [x] 8. Commit all changes, create tag v0.1.2, push, and create GitHub release - **DONE**
- [x] 9. Run `poetry publish -v` (LAST step) - **DONE** (published to PyPI)
