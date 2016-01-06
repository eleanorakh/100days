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
