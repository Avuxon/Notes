# **330 Lecture 3 - Writing Ruby as Ruby**

Ruby - basic unit is the expression, not a statement
```Ruby 
> x = 4;
==> 4

x = 3
y = 10 + (if x then 3 else 4 end)

```

semi-colon is discard / new-line operator
```Ruby
> x = 1; 2; 3; 4
==> 4
> x
==> 1
```

```Ruby
4.0./ (3.0).*(PI.*(radius.**(3)))
```

### **Code Blocks**
```
[1,2,3,4].each { |val| puts val }
> alternative to for loops
{1..4}.each { |i| print i; puts i*i }
```

Enumerators
- Integers : 5.upto(10)
- Ranges : (5..10).each
- Array : [1,2,3,4,5].each 
- Strings : "this".each_char
- Hashes : 

find : 
```Ruby
[1,2,3,4,5].find { |y| y % 2 == 0 }
> returns first value that is true or satisfies value
```

x.map! modifies array in place

**Code blocks w/ yield**
```Ruby
countx(4) { puts "foo" }
```


