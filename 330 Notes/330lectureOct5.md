# **Week 6**

***Alphabet*** : finitie set of symbols
- usually denoted with Σ

***String*** : finite sequence of symbols from Σ
- ε is the empty string
- |s| is length of string s
- Set of strings = {"0", "1", "01"}
- ∅ is empty set

***String concatenation*** : 
Concatanate strings from different alphabets; new alphabet is union of two sets

***Language*** : set of strings over an alphabet
``` 
ex: All strings of length 1 or 2 over alphabet Σ = {a, b, c} that begin with a is 
L = {a, aa, ab, ac} (L here is a language)
```
```
ex: The set of phone numbers over the alphabet 
Σ = {0, 1, 2, 3, 4, 5, 6, 7, 9, (, ), -}
In REGEX : /\(\d{3, 3}/)/d{3,3}-\d{4,4}/
```
## **Operations on Langauges**
- concatanation, union, kleene closure

Let L1 = {a, b}, L2 = {1, 2, 3} \
Σ = ?

L1L2 = {a1, a2, a3, b1, b2, b3}

L1 U L2 = {a, b, 1, 2, 3}

## Regex: Grammar

R::=∅ The empty language

## **Implementing RegEx**
***Finite Automaton*** : 

2 states S : 
- Start state (can only be 1, implied by one circle)
- End state (can be multiple, implied by double circle)

```
ex : 
process string "01"
start in S0, look at first character
<01, S0>  configurations
<1, S0>
< - , S1> Accept

ex 2: 
<010, S0>
<10, S0>
<0, S1>
< - , S0> Reject
```
- String is accepted if automaton is in final state when end of string s is reached 
- Start state can be a final state
- Two symbols can share a transition
- Every RegEx and Finite State Automaton can be converted to one of each other

- If transition is omitted, assume it goes to a dead state that is not shown
---
# **October 7**: DFAs, NFAs, Regexps

What we learned last class were Deterministic Final State Automatons (DFAs)
- have exactly one sequence of stems for each string

## **NFAs - Nondeterministic Final State Automatons**
- NFAs may have more than one transition per symbol
- DFA is a special case of NFAs

### **Formal Definition**
- A DFA is a 
5 tuple (Σ, Q, q0, F, ƍ (delta))
- Σ = {0, 1}
- Q is {S0, S1, S2} (set of all states)
- q0 = S0 (start state)
- F = {S1} (final state)
- ƍ is all transitions states, (can be shown as a table or written as {(S0,0,S0), (S0,1,S1) etc...})

Must reduce NFA to DFA before converting to RegEx
