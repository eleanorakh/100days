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

03/01/2016 - #11: Method and Message
  - Methods are not a first class object in Ruby - that means that defining a method does not immediately give you a value that you can pass around.
  - But we can ask for an object representing a method
  - can call method just as a proc or lambda
  - This is consistent with ruby as a purely object orientated language
  - Method vs message is hard to pull apart -  OO is so dominated by method orientated terminology like C++ and Java that we often use them interchangeably
  - to sum up: A message is a name for a responsibility which an object may have. A method is a named, concrete piece of code that encodes one way a responsibility may be fulfilled.
  - Allen K envisioned objects as independent cells, passing messages to each other with no assumption about how those messages would be handled - ruby hues to this vision of OOP

04/01/2016 - #17: Pay it Forward
  - Use execute for ‘executing’ lower level commands (returns command)
  - Command method: causes some change to happen in the world around it
  - Query method: returns some information
  - Command-Query separation - states that keeping command and query methods separated in a program makes that program simpler and more comprehensible.

05/01/2016 - #20: Struct
  - Can use struct to quickly construct classes
  - Typically, when we create structs in ruby we immediately assign the resulting class to a constant.
  - Ruby has a special rule for when an anonymous class or module is assigned to a constant for the first time. When that happens, Ruby sets the name of the class or module to the name of the constant (this only happens once)  - this is the only time that assigning an object to a variable or a constant causes a change to the object itself
  - can get and set values using hash like syntax structures
  - symbols and strings can be used interchangeably as keys
  - equality operator - struct defines it so that instance with equal attributes are considered equal
  - unlike attributes defined with attr_accessor, structs can introspect and iterate over their attributes
  - structs also have enumerable
  - struct is a powerful tool for defining rich data structures

06/01/2016 - #1: Binary Literals
  - Literal syntax is things like strings, floating points e.ct
  - Ruby has a literal index for hexidecimal and octal numbers
  - Octal numbers are useful for things like specifying unix file permissions (hard)
  - But Ruby also supports binary literals, which aren't as common
  - Binary literals are useful for translating octal numbers into permissions (I think?)
  - Permission order: U(ser) G(roup) O(ther)

07/01/2016 - #2: Large Integer Literals
  - Hard to visualise the number of digits in a numeric literal if it gets too big, so it's common to break digits into groups
  - Ruby let's us instert underscores anywhere we want in Integer Literals
