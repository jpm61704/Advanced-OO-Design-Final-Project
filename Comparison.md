# Comparisons of references and values

## Comparisons of Values

### C#

### Ruby

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




How are values compared? (i.e. comparing two strings)
