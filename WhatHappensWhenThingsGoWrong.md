# Errors and exception handling

## C#

Error handling in C# is nearly identical to java, boring and uninspired. It makes use of ```try```, ```catch```, and ```finally``` in the usual way. That said it gets the job done. 

```
// This is an example of the syntax for exceptions in Java... I mean C#... both?

try
{
  // the code to execute
}
catch (Exception e)
{
  // the block to execute if an exception is thrown
}

// upon further inspection this is definitely in C# because no self-respecting java programmer would break style and put opening brackets on their own line.
```

the ```throw``` keyword can be used to throw an exception if code that is being written has some way of failing. 

## Ruby

Ruby error handling is almost as boring and unexceptional as C# _but_ it has different keywords to make the language more exciting.
- ```raise```: raises an exception, this is ruby's equivilent to ```throw```
- ```rescue```: rescues the program in the event of an exception being raised. In most other languages this is called ```catch```
- ```ensure```: the equivilent to ```finally```

The most notable difference about Ruby's error handling is that it doesnt utilize a try keyward and opts to just reuse its ```begin/end``` keywords to define a block to be rescued. 

An example of this:
```
begin
  //code to try
rescue Exception => e
  //what to do if a pesky exception comes around
ensure
  //finally
end
```




