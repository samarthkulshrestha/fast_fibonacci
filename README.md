# fast fibonacci

A fast fibonacci numbers algorithm using Lucas sequence identities. This algorithm
can calculate upto the 25th millionth fibonacci number in ~1sec.

## introduction

### lucas sequence identities

These identities are the basis for the algorithm:

+ $`\displaystyle F_{2n}=L_{n}F_{n}`$
+ $`\displaystyle L_{2n}=L_{n}^{2}-2(-1)^{n}`$
+ $`\displaystyle 2F_{n+1}=F_{n}+L_{n}`$
+ $`\displaystyle 2L_{n+1}=5F_{n}+L_{n}`$
