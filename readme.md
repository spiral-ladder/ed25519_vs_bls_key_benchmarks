Compare performance of ed25519_dalek and threshold_crypto bls keys.

# Quickstart

```
$ cargo build --release && ./target/release/ed25519_vs_bls_key_benchmarks > /tmp/test.csv
```

Open `/tmp/test.csv` in your spreadsheet application.


# Results

Results are saved in `results.csv`.

All timings here are in microseconds (µs). 

_Hardware: M2 Pro, 12 cores, 32GB RAM_

|  | BLS12-381 | ED25519 | BLS/ED |
| ------ | ------ | ------ | ------ |
| Sign 32B | 127.7 | 11.9 |  10.7 |
| Sign 1MiB | 523.8 | 3499.8 | 0.15 |
| Verify 32B | 526.6 | 28.4 | 18.5 |
| Verify 1MiB | 939.5 | 1772.7 | 0.53 |
