# timer

A minimal QPM package for the Quantum Language (`.sa`). Adds two functions,
`starttimer()` and `endtimer()`, so you can measure how long any block of
code takes to run — no manual timestamp math required.

## Install

```
qpm install timer
```

## Usage

```
from timer import starttimer, endtimer

starttimer()

// ... your program ...

endtimer()
```

Output:

```
Execution time: 0.842 seconds
```

## How it works

`starttimer()` records the current time via the language's built-in
`time()`. `endtimer()` records the time again and prints the difference.
Just wrap whatever you want to measure between the two calls.

## Example

```
from timer import starttimer, endtimer

starttimer()

function fib(n) {
    if (n < 2) { return n; }
    return fib(n - 1) + fib(n - 2);
}
print(fib(28));

endtimer()
```

---
Published by TeamUranus.
