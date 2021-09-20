# **Lecture Sep 20 - Heap Sort**

### Heap Sort has 2 phases
1. Create Heap
2. Finish Heap

**Heap:**
A rooted tree w/ values in the nodes where every node's values are larger than or equal to the values in its children. 

- HeapSort uses a full binary tree until the bottom level, where all nodes are shifted to the left. 

- HeapSort is a type of selection sort

leaf sifts through nodes of the tree

> ~ means asymptote \
> Number of sifts is N - 1 ~ N

> Number of levels per sift: ~ lg N

> Number of comparisons per level : 2; \
compares the 2 children, then compares the larger child to the number being sifted

> Total sifts ~ 2N*lg(N)

Given that that the size of the tree shrinks every iteration, what's the summation for number of comparisons?

⅀(i = 0, n-1) 2 lg(N - 0)

Stirling's Formula
N! ~ (N/e)^(N) √(2 \* pi \* N)