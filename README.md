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
Fibonacci and Lucas numbers $`F_{\frac {n}{2}}`$ and $`L_{\frac {n}{2}}`$ exist.
