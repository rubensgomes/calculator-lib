# Calculator-LIB

A Python calculator library providing stateless arithmetic, power/root, modulo, rounding, and logarithmic/exponential operations.

- **Distribution name**: `calculator-lib-rubens`
- **Python package**: `calculator_lib` (imported as `from calculator_lib import Calculator`)
- **Repository**: [rubensgomes/calculator-lib](https://github.com/rubensgomes/calculator-lib/)

## Requirements

- Python 3.14+
- [Poetry](https://python-poetry.org/)

## Getting Started

```bash
# Install dependencies
poetry install

# Activate environment
poetry env activate
```

## Usage

```python
from calculator_lib import Calculator

calc = Calculator()

calc.add(2, 3)          # 5
calc.subtract(10, 4)    # 6
calc.multiply(3, 4)     # 12
calc.divide(10, 2)      # 5.0
calc.power(2, 3)        # 8
calc.sqrt(16)           # 4.0
calc.nth_root(27, 3)    # 3.0
calc.modulo(10, 3)      # 1
calc.floor_divide(7, 2) # 3
calc.absolute(-5)       # 5
calc.round_number(3.14159, 2)  # 3.14
calc.floor(3.7)         # 3.0
calc.ceil(3.2)          # 4.0
calc.log10(100)         # 2.0
calc.ln(math.e)         # 1.0
calc.exp(1)             # 2.718281828459045
```

Invalid inputs raise `ValueError`:

```python
calc.divide(10, 0)      # ValueError: Cannot divide by zero
calc.sqrt(-1)           # ValueError: Cannot take square root of a negative number
calc.log10(0)           # ValueError: Cannot take logarithm of a non-positive number
```

## Common Poetry Commands

```bash
# Update the dependencies found in `pyproject.toml`
poetry update --verbose

# Install the project dependencies
poetry install --verbose

# Activate Poetry-managed virtual environment in your current shell
eval "$(poetry env activate)"

# Sort and group import statements
poetry run isort src/ tests/

# Format your Python code
poetry run black src/ tests/

# Run static type checker on Python `src/` folder
poetry run mypy src/

# Lint
poetry run pylint src/

# Run tests
poetry run pytest

# Run tests with coverage
poetry run pytest --cov
```

## License

[Modified MIT](LICENSE)
