# Lecture 2 - Ruby Fundamentals
Why Ruby?
- Large directory of data files
- Find all w/ "AST" in name and more than 1000 words
- Need this quickly

**Scripting Languages** : 
Rapid prototyping langages for common tasks (like python)

**Piagetian Learning Theory** \
Assimilation : 
- Add facts to what we know
- Assimilate to existing patterns
- Ifs in Ruby are like ifs in Java

Accommodation
- Learn new patterns, concepts
- Harder, takes more work
- Ruby code blocks are a new concept
---
## **New Ruby concepts**
- Fully OOP, no primitive objects
- lightwieght syntax
- dynamic, implicit declarations
- new data types
- Regular expressions
- Code blocks

Ruby variables are **implicitly declared**, first use of a var declares it

---
**Static Type Checking (static typing)** : 
Before program is run, types of all expressions are determined. Disallowed operaitions cause compile-time error and cannot run the program. \
Ex: Java, C

Static types are often explicit, (aka manifest)

**Dynamic type Checking** : 
During program execution, can determine type from run-time value. Type is checked before use. \
Ex: Ruby, Python

**Control Statements** in Ruby : 
while loops, conditionals. Terminate any of these with **'end'**.

True branch is taken unless guard is false or nil. 0 is true. 

---
To get type of var do 
```Ruby
x = 5
x.class # outputs 'Integer'

y.ancestors # outputs all superclasses of y
```

Get array of all class methods w/
```Ruby
(1..3).methods # gives all methods for range type
```
## **Array Essentials**
- Heterogeneous, ex: a = [1, "foo", 2.15]
- Return nil if out of range, so ex: puts[a]
- Empty array, ex: a = []
- Delete by value, ex: a.delete("foo")
---
- a.sort does not modify objects (returns a copy)
- a.sort! modifies original object
- a.uniq or uniq! removes all duplicates