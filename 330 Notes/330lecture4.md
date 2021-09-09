# **330 lecture 4**

**Operators as messages**
- 1+2 can be written as 1.+(2)
- if x.[](if true then 1 else 2 end), x is an array

***Small Talk*** - 
Ruby not fully consistent in message passing, small talk built fo this

### Object Copy vs. Reference Copy
```Ruby
x = "groundhog" ; y = x
# This is a reference copy

# Ruby can also maken an object copy
x = "groundhog"
y = String.new(x)

x == y # compares structural equality - (shallow, compares contents)
x.equal? y # compares physical equality (deep comparison)

```
---
## **Comparisons**
Ruby Comparison Method
<=> Binary operator, returns __ when a is ___ b
- -1 less than
- 0 = equal to
- +1 greater than

## **Sorting**
Default Sort (puts values in ascending order)
- [2, 5, 1, 3, 4].sort  -  returns [1,2,3,4,5]

Custom Sort 
- [2, 5, 1, 3, 4].sort { |x, y| y <=> x } - returns same thing
---

1..3 is an object of class Range. Includes 1 and 3 \
1...3 is also an object of class Range. Does not include 3.

convert range to array via to_a; e.g., (1..2).to_a

### Auto Ruby Global Variables
$_ stores last read line of input. \
Try not to use this because confusing

### **Mixins**
Inheritence to reuse code, similart to java \ 
- include A "inlines" A's methods at that point

**Ruby Modules**
: a collection of methods and constants
- Module methods acan be called directly
- instance methods are "mixed in" to another class

> Practce mixins
> Also practice mixins: enumerable (on slides 9/9)
> exceptions

## **Ruby Regex**
A way of describing patterns or sets of strings

```Ruby
/Ruby/ # Matches exactly the string "Ruby" 

(/Ruby|OCaml|Java)/ # Mathches any of these

(/Ruby|Regular)/ or /R(uby|egular)/

/(Ru|Tub)by|\(Ruby\)
# Find "Ruby" or "(Ruby)" or "Tubby"?

```

Matching Opearator =~ of String
- if line =~ /Ruby/

**Repetition Opearators**
- /(Ruby)*/ means zero or more
- /(Ruby+)/ means one or more
- /{Ruby}{3}/ - exactly 3 occurences

> REVIEW ALL REGEX SLIDES



