# Era Test (`github.com/era-lang-official/test`)

Built-in testing assertions, test suites, and micro-benchmarking runners for Era.

## Features
- **Assertions**: `assert_true`, `assert_false`, `assert_eq_str`, `assert_eq_int`, `assert_contains`.
- **TestRunner**: Collects passed/failed assertions and produces clean test reports.
- **BenchmarkRunner**: Times iteration loops and reports operations per millisecond.

## Usage
```era
import "github.com/era-lang-official/test";

fn main() {
    let mut runner = TestRunner::new("MathSuite".to_string());
    runner = runner.assert_eq_int(2 + 2, 4, "addition");
    runner.summary();
}
```

