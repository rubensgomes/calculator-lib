# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

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
