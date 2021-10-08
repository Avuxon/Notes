# **Lets, Lists, and Recursion in OCaml**

Lists have a recursive structure

Sum the elements of a list :
``` OCaml
let rec sum lst = match lst with 
    [] -> 0
    (h::t) -> h + sum(t)
```
Negate the elements of a list :
``` OCaml
let rec negate lst = match lst with 
    [] -> []
    (h::t) -> (-h) :: negate t
```

Get the last element of a list : 
```OCaml
let rec last lst = match lst with
    (h::[]) -> h
    (h::t) -> last t
```

merge 2 lists
```OCaml
let rec append l m = match l with
    [] -> m
    (h::t) -> h :: append (t m)
```

reverse a list
```OCaml
let rec rev lst = match lst with
    [] - []
    (h::t) -> append(rev(t) [h])
```

sum each pair in a list
```OCaml
let rec sum2 lst = mstch lst with
    [] -> []
    (m::n::t) -> (m+n) :: sum2 t
    (* m and n are the first two elemenbts of the list, t is the rest)
```

## **Let Definition != Let Expression**
let definition: let x = e;; 
let expression let x = e1 in e2;;

### Shadowing, by the Semantics

- Evalueation of let x = e1 in e2:
- evaluate e1, then substitute v1 for x in e2

### Nested Let Expressions

- Uses of let can be nested in OCaml

### **Tuples**
- like a list but must be a fixed length, has unnamed fields, is homogenous

### **Records**
- identify elements by name

type date = { month: string; day: int; year: int }
let today = {day = 16 ; year = 2017; month = "f"^"eb: } ;;