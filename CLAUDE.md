# CLAUDE.md

## Project Overview

**calculator-lib** is a Python calculator library that provides stateless arithmetic, power/root, modulo, rounding, and logarithmic/exponential operations via the `Calculator` class.

- **Distribution name:** `calculator-lib-rubens` (on PyPI)
- **Python package:** `calculator_lib` (imported as `from calculator_lib import Calculator`)
- **Language:** Python >= 3.14
- **Build/Package Manager:** Poetry (poetry-core >= 2.0.0)
- **Source layout:** `src/calculator_lib/`
- **Tests:** `tests/`
- **Repository:** [rubensgomes/calculator-lib](https://github.com/rubensgomes/calculator-lib/)

## Common Commands

### Install dependencies
```bash
poetry install
```

### Run tests
```bash
poetry run pytest
```

### Run tests with coverage
```bash
poetry run pytest --cov
```

### Linting and formatting
```bash
poetry run black src/ tests/
poetry run isort src/ tests/
poetry run mypy src/
poetry run pylint src/
```

## Project Structure

```
src/calculator_lib/
  __init__.py        # Package exports (Calculator)
  calculator.py      # Core Calculator class with all operations
tests/
  test_calculator.py # Tests for all Calculator methods
scripts/
  test_github.sh     # GitHub connectivity test script
docs/
  release-plan-v0.1.0.md  # Release plan for v0.1.0
  release-plan-v0.1.1.md  # Release plan for v0.1.1
```

## Code Conventions

- **Formatter:** Black (default settings)
- **Import sorting:** isort
- **Type checking:** mypy (strict on src/)
- **Linting:** pylint
- **Test framework:** pytest with fixtures
- **Coverage:** >= 90% required (`fail_under = 90` in pyproject.toml)
- All `Calculator` methods are stateless, accept `float` args, return `float`, and raise `ValueError` for invalid inputs
- Logging via `logging.getLogger(__name__)` for debug/warning messages

## Release Process

See [RELEASE.md](RELEASE.md) for the full release process. Releases are managed via Claude Code using the `/release-plan` custom slash command.
