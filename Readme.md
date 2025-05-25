# Rabin's Probabilistic Primality Test

This project implements and evaluates Rabin's primality test — a fast, randomized algorithm for determining whether an integer is prime with high probability.

## Features

- Python implementation of Rabin's test (`isProbablePrime(n, k)`)
- Early elimination using small-prime divisibility checks
- Empirical performance evaluation on inputs from 8 to 128 bits
- Zero false positives observed in 100,000 tests per bit size (k=5)

## How It Works

1. Decompose `n - 1` as `2^s * d`
2. For `k` random bases `a`:
    - Compute `x = a^d mod n`
    - Check if `x` reveals compositeness via modular squaring
3. Declare `n` probably prime if all tests pass

## Usage

```bash
python3 rabin_test.py

Adjust k or input range in the script to customize performance and reliability.

Environment
	•	Python 3.9+
	•	Tested on macOS (M3, 16GB RAM)

References
	•	Rabin, M. O. (1980). Probabilistic algorithm for testing primality. Journal of Number Theory.