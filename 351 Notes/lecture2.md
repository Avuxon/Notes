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
If growing at the same rate or slower :
θ notation \
If growing faster use Ω

