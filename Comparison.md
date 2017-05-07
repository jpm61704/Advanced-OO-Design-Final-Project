# Comparisons of references and values

## Comparisons of References

### C#

### Ruby

Object references are compared much how one would expect in most languages. It is done by calling the ```equal?``` or ```eql?``` methods on an object or by using the ```==``` infix operator.

for example:

```
class SomeObject
end

object1 = SomeObject.new
object2 = object1
object3 = SomeObject.new

//all of these evaluate to true
object1 == object2
object1.equal? object2
object1.eql? object2

//all of these evaluate to false
object1 == object3
object1.equal? object3
object1.eql? object3

```

however the ```eal?``` method and ```==``` operator can be redefined to provide custom comparison functionality for a class.

for example:

```
class Person
  @name
  def initialize name 
    @name = name
  end

  def ==(other_person)
    self.name == other_person.name
  end
end
```
The above example will say two people are equal if their names are equal. Ruby also allows for <, >, <=, >=, etc by including the Comparable module in the class. Once with is done a comparision method(```<=>```) can be defined to do comparisons.

Also notable is that the difference between ```==``` and ```eql?``` is that typically the latter is used to compare value _and_ type while the former is only used to compare value. This could be useful when comparing things like numbers where the types can vary widely but it is often possible to compare their values. Other times you may need to keep types seperate

## Comparisons of Values

### C#

### Ruby


How are values compared? (i.e. comparing two strings)
