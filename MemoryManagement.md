# Memory Management

## C# 
Memory in C# mainly follows the .Net memory management scheme which is to use garbage collection to handle memory. The basic process is described on [MSDN](https://msdn.microsoft.com/en-us/library/aa691138(v=vs.71).aspx):
1. Object is instantiated
2. If the object cannot be accessed or called anywhere, then it becomes eligible for destruction
3. At some future point the destructor is called
4. The object is unreferencable after destruction and is marker for garbage collection
5. At some future point the garbage collector frees the memory the object occupied
This model of garbage collection is very similiar to java and works well for most regular applications.

## Ruby
Maz, the creator of Ruby, sought to create a language for people and not machines when he was designing ruby. This led him to the obvious decision to include a garbage collector with the language. The garbage collector runs only when the memory for the program has completely runs out and sweeps through the entire area allocated for it.

## Automatic Reference Counting

### C#
The designers of the .Net framework opted for garbage collection over reference counting. There many reasons can be found in the extensive email chain in the link below. In summary they felt that it would add too much complexity to the language for the user to have to navigate.

https://blogs.msdn.microsoft.com/brada/2005/02/11/resource-management/

### Ruby
Ruby also does not use ARC for memory management but specific reasons as to why are not easily available outside of speculation. 
