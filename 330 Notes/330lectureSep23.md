# **OCaml Higher Order Functions**
Functions as variables and parameters

Ocaml has infinity value if we can't use 0 or Null (can't return null if type is int): \
Review binary search: 

```OCaml
let f x = ( x -. 2.0) ** 3.0

let rec root g left right = 
    let zero y = sqrt(y *. y) < 0.00001 in 
    let middle = (left +. right)/. 2.0 in 
    if zero (g middle) then
        middle
    else if (g middle( < 0.0) then
        root g middle right
    else
        root g left middle
```

## **Anonymous Functions**

- Functions are first class functions and can be passed around.

functions can be anonymous, local (it's like a code block from ruby) \
```OCaml root (fun x -> (x -. 2.0) ** 3.0) 0 3```

- syntax : fun x1 .. xn -> e \
Use fun to make a function with no name : 
fun x -> x + 3

Anonymous function is an expression, a value, no further eval is possible

***Type Checking*** ???

first class and can be used as a variable
```OCaml
let f x = x + 3
let g = f
g 5
```

Fun notation exercises :  
let next = fun x -> x + 1

let plus = fun x y -> x + y

let rec fact = fun n -> (if n = 0 then 1 else n * fact (n-1))

***Pattern Matching with Fun***

Ruby's collect is called map in OCaml
- takes a function and a list, and applies function to each element and returs a list of results

```OCaml
let rec map f l = match l with 
    [] -> []
    | (h::t) -> (f h)::(map f t)
```
## **Accumulator(List Recursion)**
- bypasses some instances of stack overflow that regular recursion deals with

```OCaml
let rec fold f a l = match l with 
    [] -> a
   |(h::t) -> fold f (f a h) t

```