# Calculator-LIB

A Python calculator library providing stateless arithmetic, power/root, modulo,
rounding, and logarithmic/exponential operations.

[![Python 3.14+](https://img.shields.io/badge/python-3.14%2B-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## Installation

```bash
pip install calculator-lib-rubens
```

## Quick Start

```python
from calculator_lib import Calculator

calc = Calculator()

calc.add(2, 3)  # 5
calc.subtract(10, 4)  # 6
calc.multiply(3, 4)  # 12
calc.divide(10, 2)  # 5.0
```

## API Reference

### Core Arithmetic

| Method           | Description                        |
|------------------|------------------------------------|
| `add(a, b)`      | Returns the sum of `a` and `b`     |
| `subtract(a, b)` | Returns `a` minus `b`              |
| `multiply(a, b)` | Returns the product of `a` and `b` |
| `divide(a, b)`   | Returns `a` divided by `b`         |

### Power & Roots

| Method           | Description                         |
|------------------|-------------------------------------|
| `power(a, b)`    | Returns `a` raised to the power `b` |
| `sqrt(a)`        | Returns the square root of `a`      |
| `nth_root(a, n)` | Returns the n-th root of `a`        |

### Modulo & Integer Math

| Method               | Description                           |
|----------------------|---------------------------------------|
| `modulo(a, b)`       | Returns the remainder of `a / b`      |
| `floor_divide(a, b)` | Returns the floor division of `a / b` |

### Absolute & Rounding

| Method                        | Description                            |
|-------------------------------|----------------------------------------|
| `absolute(a)`                 | Returns the absolute value of `a`      |
| `round_number(a, decimals=0)` | Rounds `a` to the given decimal places |
| `floor(a)`                    | Returns the largest integer <= `a`     |
| `ceil(a)`                     | Returns the smallest integer >= `a`    |

### Logarithmic & Exponential

| Method     | Description                          |
|------------|--------------------------------------|
| `log10(a)` | Returns the base-10 logarithm of `a` |
| `ln(a)`    | Returns the natural logarithm of `a` |
| `exp(a)`   | Returns *e* raised to the power `a`  |

## Usage Examples

```python
import math
from calculator_lib import Calculator

calc = Calculator()

# Power & Roots
calc.power(2, 3)  # 8
calc.sqrt(16)  # 4.0
calc.nth_root(27, 3)  # 3.0

# Modulo & Rounding
calc.modulo(10, 3)  # 1
calc.floor_divide(7, 2)  # 3
calc.round_number(3.14159, 2)  # 3.14
calc.floor(3.7)  # 3.0
calc.ceil(3.2)  # 4.0

# Logarithmic & Exponential
calc.log10(100)  # 2.0
calc.ln(math.e)  # 1.0
calc.exp(1)  # 2.718281828459045
```

## Error Handling

All methods validate their inputs and raise `ValueError` with descriptive
messages for invalid operations:

```python
calc.divide(10, 0)  # ValueError: Cannot divide by zero
calc.sqrt(-1)  # ValueError: Cannot take square root of a negative number
calc.log10(0)  # ValueError: Cannot take logarithm of a non-positive number
calc.nth_root(-4, 2)  # ValueError: Cannot take even root of a negative number
calc.modulo(10, 0)  # ValueError: Cannot modulo by zero
```

## Requirements

- Python 3.14+

## License

[Modified MIT](LICENSE)
