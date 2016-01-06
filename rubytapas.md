02/01/2016 - #7: Constructors
  - in Ruby, the new is a method on the class
  - in other languages, the constructor is a method with the same name as the class, but in ruby we define our constructor by writing an initialize method
  - to construct a new instance, Ruby needs to do three things:
    - Allocate a new, empty object
    - Run specialized initialize
    - Return the initialized instance
  - What are cartesian and polar and singleton?
  - way to avoid the method being instantiated is to make it private
- can keep a cache of instances and return objects from a cache instead of newly allocated instances

02/01/2012 - #11: Method and Message
  - Methods are not a first class object in Ruby - that means that defining a method does not immediately give you a value that you can pass around.
  - But we can ask for an object representing a method
  - can call method just as a proc or lambda
  - This is consistent with ruby as a purely object orientated language
  - Method vs message is hard to pull apart -  OO is so dominated by method orientated terminology like C++ and Java that we often use them interchangeably
  - to sum up: A message is a name for a responsibility which an object may have. A method is a named, concrete piece of code that encodes one way a responsibility may be fulfilled.
  - Allen K envisioned objects as independent cells, passing messages to each other with no assumption about how those messages would be handled - ruby hues to this vision of OOP
