# **Lecture 2**
Algorithm
: step-by-step finite list of instructions for solving a problem
> Ex: Tournament assignement

Efficiency determined by:
- Time
- Space

Two algorithms :
- **Bubble Sort** (slow algorithm): 4n^2 instructions
- **Merge Sort** (fast algorithm): 80n lg n instructions

*Time is also affected by processing speed of computer.*
> Know how to compare time of different speed computers paired w/ different speed algorithms

```
 n(n+1)(n+2) / 6 = \
n^3 / 6 + n^2 / 2 + n / 3 = \
n^3 / 6 + O(n^2) = \
n^3 / 6 \
= θ(n^3) \
-> Only the highest order term matters, you lose information as you progress
```

### Order notation relationship symbols:
**Big-O** : If *f(x)* = O(*g(x)*), then *f(x)* is eventually smaller than some constant multiple of *g(x)*

**Big-Omega** : If *f(x)* = Ω(*g(x)*), then *f(x)* is eventually greater than some constant multiple of *g(x)*

**Big-Theta** : If *f(x)* = θ(*g(x)*), were B*g(x)* ≤ *f(x)* ≤ C*g(x)*, then *g(x)* is eventually in between B*g(x)* & C*g(x)*




