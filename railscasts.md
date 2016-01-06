02/01/2016 - #1: Caching with Instance Variables
- method called several times per request and each time sends a query to the database
- solve this by caching the result of the database call in an instance Variable

03/01/2016 - #2: Dynamic find_by Methods
  - performing a find of a task model where false
  - find_by method - search by tasks specifically
  - This is a really useful way to do a Find in Rail as there's a Taskmodel that searches for tasks that haven’t been completed (i.e. the complete column is false). find_by_all is a concise way to achieve this
