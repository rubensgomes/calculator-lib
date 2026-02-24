# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.1.4] - 2026-02-23

### Changed

- Lowered minimum Python version requirement from `>=3.14` to `>=3.10.0` for broader compatibility
- Updated `poetry.lock` with latest dependency versions

## [0.1.3] - 2026-02-20

### Changed

- Expanded `.gitignore` with comprehensive ignore rules (Claude Code, Jupyter, AI/ML artifacts, secrets, OS files)
- Fixed minor typos in `LICENSE` (missing period, capitalized "Limitation of Liability")
- Simplified and updated `RELEASE.md` (removed outdated steps, corrected script references)
- Updated `poetry.lock` with latest dependency versions
- Cleaned up `pyproject.toml`

### Added

- New `SETUP.md` documentation file with project setup instructions

## [0.1.2] - 2026-02-18

### Changed

- Improved `README.md` with PyPI/license badges, API reference tables, categorized usage examples, and error handling section
- Updated `CLAUDE.md` to include v0.1.1 release plan in project structure
- Updated `.claude/commands/release-plan.md` to create NEW release plans per release
- Updated `llms.txt` with minor formatting fixes

## [0.1.1] - 2026-02-18

### Changed

- Renamed distribution from `calculator-lib` to `calculator-lib-rubens` for PyPI uniqueness
- Updated `pyproject.toml` with keywords, MIT license classifier, and bumped uvicorn dependency
- Updated `README.md` with correct distribution name, fixed license reference, and improved commands section
- Updated `CLAUDE.md` with distribution name, repository link, expanded project structure, and release process section
- Updated `llms.txt` with correct distribution name, installation instructions, categorized API sections, and error handling examples
- Updated `poetry.lock` with latest dependency versions

## [0.1.0] - 2026-02-16

### Added

- Core `Calculator` class with 16 stateless mathematical operations:
  - Arithmetic: `add`, `subtract`, `multiply`, `divide`
  - Power & roots: `power`, `sqrt`, `nth_root`
  - Modulo & integer math: `modulo`, `floor_divide`
  - Absolute & rounding: `absolute`, `round_number`, `floor`, `ceil`
  - Logarithmic & exponential: `log10`, `ln`, `exp`
- `ValueError` guards for invalid inputs (division by zero, negative square roots, non-positive logarithms, even roots of negatives, zeroth root)
- Debug and warning logging on all operations
- Full test suite with 62 tests and 100% code coverage
- Project documentation: README.md, CLAUDE.md, llms.txt, CHANGELOG.md
