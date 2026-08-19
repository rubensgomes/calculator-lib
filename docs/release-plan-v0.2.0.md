# Release Plan v0.2.0

## Overview

- **Version:** 0.2.0
- **Date:** 2026-08-19
- **Description:** Raise the minimum supported Python to 3.14, update the build
  backend and dev dependency floors, and refresh project documentation

**Why a minor bump:** raising `requires-python` to `>=3.14.0` breaks installation
for existing Python 3.12/3.13 consumers, so this release takes a minor version
bump rather than a patch.

## Changes in this Release

### Changed

- Updated `requires-python` from `>=3.12.0,<4.0.0` to `>=3.14.0,<4.0.0`
- Updated build requirement from `poetry-core>=2.0.0` to `poetry-core>=2.4.1`
- Updated dev dependency minimum versions in `pyproject.toml` (`black`, `coverage`,
  `httpx`, `mypy`, `pylint`, `pytest`, `pytest-asyncio`)
- Relaxed `types-pyyaml` constraint from `>=6.0.12.20250915` to `>=6.0.12`
- Updated `poetry.lock` with latest dependency versions
- Updated `SETUP.md` to run `black` with an explicit `--target-version py314`
  and to list `httpx` among the dev dependencies
- Updated `RELEASE.md` with the `claude` CLI invocation used to start a release
  and corrected the `release-plan.md` link text
- Updated `README.md` Python badge and requirements to 3.14+
- Updated `llms.txt` build system reference to `poetry-core >= 2.4.1`
- Updated `CLAUDE.md` to reflect Python >= 3.14 and `poetry-core >= 2.4.1`, plus
  common commands, project structure, and tooling notes
- Added `target-version = ["py314"]` to `[tool.black]` in `pyproject.toml` so
  `black` no longer warns about an inferred Python 3.15 target

### Removed

- Removed the deprecated `License :: OSI Approved :: MIT License` classifier from
  `pyproject.toml` (superseded by the PEP 639 `license = "MIT"` expression)

## Release Steps

- [x] 1. Run `poetry run mypy src/` and fix any issues
- [x] 2. Run `poetry run isort src/ tests/` and fix any issues
- [x] 3. Run `poetry run black src/ tests/` and fix any issues
- [x] 4. Run `poetry run pytest` and fix any issues
- [x] 5. Run `export SOURCE_DATE_EPOCH=$(date +%s); poetry build -v` and fix any issues
- [x] 6. Ensure `CHANGELOG.md` exists and update with current release changes
- [x] 7. Commit all changes, create version tag, push, and create GitHub release
- [ ] 8. Run `poetry publish -v` to publish to PyPI

## Outstanding

Step 8 (`poetry publish -v`) is **blocked**: PyPI returned
`HTTP 403 - Invalid or non-existent authentication information`.

The environment has `PYPI_API_TOKEN` set, but Poetry does not read that
variable. Retrying with `POETRY_PYPI_TOKEN_PYPI="$PYPI_API_TOKEN"` produced the
same 403, so the token itself appears to be invalid, expired, or scoped to a
different repository (e.g. TestPyPI).

To finish the release, set a valid PyPI token and re-run the publish:

```bash
export POETRY_PYPI_TOKEN_PYPI="pypi-..."   # project-scoped or account token
poetry publish -v
```

The `dist/` artifacts for 0.2.0 are already built and verified, so no rebuild is
needed. Consider adding `POETRY_PYPI_TOKEN_PYPI` to the environment variables
listed in `RELEASE.md`.
