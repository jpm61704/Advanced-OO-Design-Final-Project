##  Interfaces/Protocols

#### C# (Sharp)
* C# supports the use of  Interfaces.

```csharp
public class Car : IEquatable<Car>
    {
        public string Make {get; set;}
        public string Model { get; set; }
        public string Year { get; set; }

        // Implementation of IEquatable<T> interface
        public bool Equals(Car car)
        {
            if (this.Make == car.Make &&
                this.Model == car.Model &&
                this.Year == car.Year)
            {
                return true;
            }
            else
                return false;
        }
    }
```
* When a class or struct implements an interface, the class or struct must provide an implementation for all of the members that the interface defines. The interface itself provides no functionality that a class or struct can inherit in the way that it can inherit base class functionality. However, if a base class implements an interface, any class that's derived from the base class inherits that implementation.

#### Ruby
* Ruby supports Interfaces.

```Ruby
require 'interface'

MyInterface = interface{
  required_methods :foo, :bar, :baz
}

# Raises an error until 'baz' is defined
class MyClass
  def foo
    puts "foo"
  end

  def bar
    puts "bar"
  end

  implements MyInterface
end
```
