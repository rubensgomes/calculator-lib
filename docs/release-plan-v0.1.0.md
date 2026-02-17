# Release Plan — v0.1.0

**Repository:** rubensgomes/calculator-lib
**Date:** 2026-02-16
**Release type:** Initial release

## Summary

First release of `calculator-lib`, providing the `Calculator` class with 16 stateless mathematical operations: arithmetic, power/root, modulo, rounding, floor/ceil, logarithmic, and exponential functions.

## Changes included

- Core `Calculator` class with `add`, `subtract`, `multiply`, `divide`, `power`, `sqrt`, `nth_root`, `modulo`, `floor_divide`, `absolute`, `round_number`, `floor`, `ceil`, `log10`, `ln`, `exp`
- `ValueError` guards for invalid inputs (division by zero, negative square roots, non-positive logarithms)
- Debug/warning logging on all operations
- Full test suite (62 tests) with 90% coverage threshold
- Package export fix in `__init__.py`
- Project documentation: README.md, CLAUDE.md, llms.txt, CHANGELOG.md

## Release Checklist

- [x] Run `poetry run mypy src/` — fix any issues
- [x] Run `poetry run isort src/ tests/` — fix any issues
- [x] Run `poetry run black src/ tests/` — fix any issues
- [x] Run `poetry run pytest` — fix any issues
- [x] Run `poetry run python -m coverage run -m pytest tests/` — verify coverage >= 90% (result: 100%)
- [x] Update CHANGELOG.md with v0.1.0 release notes
- [ ] Commit all changes to `main`
- [ ] Create git tag `v0.1.0`
- [ ] Push commits and tag to remote
- [ ] Create GitHub release for `v0.1.0`
