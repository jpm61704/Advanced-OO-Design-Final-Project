# Lambda expressions, closures, or functions as types

## Lambda Expressions
### C#
C# supports lambda expressions with the following syntax: ```(input-parameters) => expression```

For example, ```(x) => x + 1``` defines the iterator operator 

Lambdas are expanded further by allowing statements to be in the expression: ```(input-parameters) => { statement }```

### Ruby

Ruby is a bit more complex with regards to how it handles first-order functions. There are initially three types.
-Blocks 
-Procs
-Lambdas

#### Blocks
Blocks are statements that can be grouped together in curley braces or begin/end and then passed into a function invocation. The associated block can be run within a function using the ```yield``` keyword.
Example:
```
def run_twice 
  yield
  yield
end

run_twice {puts "Hello World!"}
```

The example above will print ```"Hello World"``` twice as there are two yields to the block.

#### Procs
Procs(short for procedure) are blocks that are saved into a variable as objects. They can thus be passed around and reused like any other object. They can be executed by calling the method ```call( variables )``` on the proc.

Syntax: ``` proc_name = Proc.new { |arguments| statement }```

#### Lambdas
Lambdas are a type of proc that allow for safe use of the ```return``` keyword. If ```return``` is called inside a proc it will also return for the function that the proc is inside of. Lambdas instead only return out of the lambda and not their enclosing method or function. 

Syntax ```lam_name = lambda { |arguments| statement }```

Lambdas are also a bit more strict with variables. If you pass a proc the wrong number of variables it will try and make things work. But if a lambda is passed the wrong number of variables it will throw an error.

## Closures

Closures in both languages are created whenever a lambda(or in ruby's case, any of the above first-order functions) is left with free variables that reference things outside of the functions main block. This means that the function is tide to the environment(and is also unpure). Closures in both languages don't have any particularly useful features but does help a user understand what is goin on in the code.

