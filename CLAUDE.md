# CLAUDE.md

## Project Overview

**calculator-lib** is a Python calculator library that provides stateless arithmetic, power/root, modulo, rounding, and logarithmic/exponential operations via the `Calculator` class.

- **Distribution name:** `calculator-lib-rubens` (on PyPI)
- **Python package:** `calculator_lib` (imported as `from calculator_lib import Calculator`)
- **Language:** Python >= 3.14
- **Build/Package Manager:** Poetry (poetry-core >= 2.4.1)
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
poetry run black --target-version py314 src/ tests/
poetry run isort src/ tests/
poetry run mypy src/
poetry run pylint src/
```

### Clean build/test artifacts
```bash
# requires poethepoet, which is NOT currently a dev dependency:
#   poetry add --dev poethepoet
poetry run poe clean
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
  release-plan-v*.md # Release plans for each version
.claude/commands/
  release-plan.md    # /release-plan custom slash command
CHANGELOG.md         # Keep a Changelog / SemVer change history
SETUP.md             # Local development environment setup
RELEASE.md           # Release process and prerequisites
llms.txt             # Machine-readable project/API summary
```

All tool configuration (`black`, `isort`, `mypy`, `pytest`, `coverage`, `poe`)
lives in `pyproject.toml`; `pylint` is configured in `.pylintrc`.

## Code Conventions

- **Style guide:** [Google Python Style Guide](https://google.github.io/styleguide/pyguide.html)
- **Formatter:** Black (line-length 80)
- **Import sorting:** isort
- **Type checking:** mypy (strict on src/)
- **Linting:** pylint
- **Test framework:** pytest with fixtures (`asyncio_mode = "auto"`)
- **Coverage:** >= 90% required (`fail_under = 90` in pyproject.toml)
- All `Calculator` methods are stateless, accept `float` args, return `float`, and raise `ValueError` for invalid inputs
- Logging via `logging.getLogger(__name__)` for debug/warning messages

## Release Process

See [RELEASE.md](RELEASE.md) for the full release process and
[SETUP.md](SETUP.md) for local environment setup. Releases are managed via
Claude Code using the `/release-plan` custom slash command, which also records
each release in [CHANGELOG.md](CHANGELOG.md) and saves a plan under `docs/`.
