# **330 Lecture September 28th - Data Types & Closures**
- Functions are a data type in OCaml

### **User Defined Types**
- *type* can be used to create new names for types
    - example: type mmylist = int * (int list)
    - let empty : mylist = (0, [])
    - val add : int -> mylist -> mylist = <fun>

```OCaml
let first x : mylist = [ ] 
    match x with
    (n, list) -> hd list
    (* pre-condition : list has 1 or more elements *)
```

## **User Defined Variants**
- like a C enum

```OCaml
type coin = Heads | Tails
```
**Constructing and Destructing VAriants**

type t = C1 | .. | Cn 
- Ci is a constructor, must begin with capital letter

Can make types that carry data : 
```Ocaml
type shape = 
  Rect of float * float
  Circle of float

  Circle(2.0)
  Rect(7.3, 119.6)

```
- Use pattern matching to deconstruct values
    - bind pattern values to data parts

- Data types are aka algebraic data types & tagged unions. 

> Option Types (missed a few slides of notes)

**Polymorphic Option Types**
- A polymorphic version of option type can work with any type of data

### **Recursive Data Types**

making a tree
```OCaml

Node(Leaf(1), Node(Leaf(2) Leaf(3)))

let rec height t : tree =  
    match t with 
    Leaf(n) -> 1
    Node(left, right) -> max(height(left), height(right)) # +1?
```

# **Closures**

```OCaml
let x = 3;;
let f y = x + y

f 2 (*will be 5*)
x = 4;;
f 2 (*will still be 5*)

```
> Curried Functions
