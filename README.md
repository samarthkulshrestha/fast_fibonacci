# fast fibonacci

A fast Fibonacci numbers algorithm using Lucas sequence identities. This algorithm
can calculate upto the 25th millionth Fibonacci number in ~1sec.

## introduction

### lucas sequence identities

These identities are the basis for the algorithm:

+ $`F_{2n}=L_{n}F_{n}`$
+ $`L_{2n}=L_{n}^{2}-2(-1)^{n}`$
+ $`2F_{n+1}=F_{n}+L_{n}`$
+ $`2L_{n+1}=5F_{n}+L_{n}`$

### explanation

Any Fibonacci number $`F_{n}`$ can be calculated if the previous Fibonacci
and Lucas numbers $`F_{n-1}`$ and $`L_{n-1}`$ are known or if the middle
Fibonacci and Lucas numbers $`F_{\frac {n}{2}}`$ and $`L_{\frac {n}{2}}`$
exist.

1. If $`n`$ is zero, return the base cases $`F_{0}`$ and $`L_{0}`$.
2. If $`n`$ is odd, make it even by calculating $`F_{n-1}`$ and $`L_{n-1}`$.
3. If $`n`$ is even, halve it by calculating $`F_{\frac {n}{2}}`$ and $`L_{\frac {n}{2}}`$.

Halving $`n`$ every step is what gives the algorithm its $`O(\log n)`$ time
complexity. Even when $`n`$ is in the form $`2^{k}-1`$, the algorithm ensures
that the next $`n`$ will be even if it is currently odd, making it only twice as
slow as the best case scenario when $`n`$ is in the form $`2^{k}`$.

## usage

+ Clone the repository:

```console
git clone https://github.com/samarthkulshrestha/fast_fibonacci.git
```

+ Run the release build:

```console
cargo run --release
```

+ To build a statically-linked binary, run:

```console
RUSTFLAGS='-C linker=ld.lld -C relocation-model=static -C strip=symbols' cargo build --release --target x86_64-unknown-linux-musl
```

## license

Fast Fibonacci is licensed under the MIT License.

Copyright (c) 2023 Samarth Kulshrestha.
