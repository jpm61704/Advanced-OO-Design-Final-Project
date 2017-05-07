# Memory Management

## C# 
Memory in C# mainly follows the .Net memory management scheme which is to use garbage collection to handle memory. The basic process is described on [MSDN](https://msdn.microsoft.com/en-us/library/aa691138(v=vs.71).aspx):
1. Object is instantiated
2. If the object cannot be accessed or called anywhere, then it becomes eligible for destruction
3. At some future point the destructor is called
4. The object is unreferencable after destruction and is marker for garbage collection
5. At some future point the garbage collector frees the memory the object occupied
This model of garbage collection is very similiar to java and works well for most regular applications.

  * #### How is it handled?
  * #### How does it work?
  * #### Garbage collection? 
  * #### Automatic reference counting?
