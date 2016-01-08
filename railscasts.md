02/01/2016 - #1: Caching with Instance Variables
- method called several times per request and each time sends a query to the database
- solve this by caching the result of the database call in an instance Variable

03/01/2016 - #2: Dynamic find_by Methods
  - performing a find of a task model where false
  - find_by method - search by tasks specifically
  - This is a really useful way to do a Find in Rail as there's a Taskmodel that searches for tasks that haven’t been completed (i.e. the complete column is false). find_by_all is a concise way to achieve this

04/01/2016 - #3: Find through Association.
  - Theres no need to pass foreign keys in find conditions, just do the find through a has_many association.
  - can perform a 'find' through an association

05/01/2016 - #4: Move Find into Model
  - Moving a find into the model cleans up controllers and removes duplication
  - Can call custom find methods through association
  - Rails allows class methods through associations, which is very powerful

06/01/2016 - #5: Using with_scope
  - In this example there is a Task Model with a custom find method for all incomplete tasks, which is limiting.
  - But can't add conditions onto custom methods
  - with_scope defines the scope of the search/find
  - As he says in the screencast, any find executed in the new with_scope block automatically inherits the specified options (which you would have set)

07/01/2016 - #6: Shortcut Blocks with Symbol to_proc
  - example: (&:name) is a Symbol to_proc
  - This is something that Rails adds to Ruby
  - It allows you to use a shortcut if you just want to call a method on the object that the block set
  - So you can pass a parameter with an & and the name of the method as a symbol
  - can be on any method that accepts a block and passes one object to it
  - example: projects.each(&:save!) saves all(each) of the projects
  - it's useful to combine multiple method calls or when you have string methods together with blocks

08/01/2016 - #7: All about layouts
  - layout is a view file that defines what surrounds a template
  - yield is important as it tells the layout where to place the content for the template that is using the layout
  - layout is global, so it will be added to any action in any controller across the application
  - layout command can also specify the name of the layout used within a controller
  - this overrides any controller specific or application specific layouts
  - layouts can also be used dynamically i.e. may only want the admin layout to be used when a user is logged it - can be done by passing a symbol as an argument to the layout command, creating a method with the same name as the symbol thus determining which layout should be used.
  - can also be used to restrict a layout to a single action in a controller (render command) - which overrides any controller specific layout.
