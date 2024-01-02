---
dg-publish: 
aliases:
  - Python programming
  - Python code
  - Python coding
  - programming in Python
tags:
  - computer-science/programming
note-type:
  - general
  - moc
description: 
file-created: 2023-10-19
file-modified: 2023-12-09
linter-yaml-title-alias: Python programming
review: 
---

# Python programming

#status/postponed

---

See also [[REF How to get started building a programming skill set|REF How to get started building a programming skill set]]

## Resources for learning Python

See [[Resources for learning Python]]

## The rules of being a good programmer

1. Document your code
2. Write test for your code
3. Make it a usable package (for the future you) %% Talk more to [[Tim Vieregge]] about it %%

## Functions in python programming

### Principles for writing effective functions

From [The Ultimate Guide to Writing Functions - YouTube](https://www.youtube.com/watch?v=yatgY4NpZXE)

1. **Single Responsibility**: Functions should perform a single, well-defined task, and their actions should be at the same level of abstraction.
2. **Separation of Commands and Queries**: Functions should either perform actions (commands) or retrieve information (queries) but not both. This helps clarify the function's purpose.
3. **Avoid Flag Arguments**: Flag arguments, which make a function behave differently based on a Boolean flag, should be avoided. Split the function into two if needed.
4. **Use Meaningful Names**: Choose descriptive and clear function and argument names to improve code readability and understanding.
5. **Introduce Abstraction**: Organize data structures and classes to improve the overall structure and readability of functions.
6. **Dependency Injection**: Rather than creating dependencies within a function, pass them as arguments to make the function more flexible and easier to test.
7. **Partial Function Application**: Use techniques like partial function application to simplify function calls and reduce redundancy in arguments.
8. **Action-Oriented Function Naming**: Function names should be action-oriented and use verbs to describe what they do.

### When use classes vs functions

> [!ai]+ AI
>
> Classes and functions serve different purposes in programming and are used in different contexts. Here are some guidelines on when to use classes versus functions:
> - Use functions when you have a specific task or operation that needs to be performed. Functions are typically used for encapsulating a block of code that can be called multiple times, possibly with different inputs, to perform a specific action or computation.
> - Use classes when you need to define objects that have their own properties (attributes) and behaviors (methods). Classes provide a way to create reusable objects that can be instantiated and manipulated in various ways. They are useful for modeling real-world entities, organizing code into logical units, and implementing concepts like inheritance and polymorphism.
> - Use functions for simple tasks that don't require complex state management or object-oriented features. Functions are often used for procedural programming or for writing smaller, more focused pieces of code.
> - Use classes for more complex tasks that involve managing state, data structures, and interactions between multiple objects. Classes provide a way to encapsulate related data and functionality into a single entity, making it easier to understand and maintain the code.
> - In general, if you find yourself needing to manage multiple instances of something with shared behaviors and attributes, classes are likely the better choice. If you have a single task or computation that doesn't require object-oriented features, functions may be sufficient.
> Ultimately, the decision of whether to use classes or functions depends on the specific requirements and design of your program. It's important to choose the most appropriate tool based on the problem you're trying to solve and the programming paradigm you're working with.

### Python dataclasses

- [How to use Python dataclasses](https://www.dataquest.io/blog/how-to-use-python-data-classes/)
- [If You’re Not Using Python DATA CLASSES Yet, You Should 🚀 - YouTube](https://youtu.be/vRVVyl9uaZc?si=9fnN4VDpfdQRkV8z)

## Managing outputs

### A better way of debugging than print statements

`pip install icecream`

```
from icecream import ic


ic(var_1) ic(var_2)
```

- When debugging, there's a library called Icecream which can be useful^[[Debugging 101: Replace print() with icecream ic() - YouTube](https://www.youtube.com/watch?v=JJ9zZ8cyaEk&t=586s&pp=ygUQaWNlIGNyZWFtIHB5dGhvbg%3D%3D)]
- [15 Python Libraries You Should Know About in 2023 - YouTube](https://www.youtube.com/watch?v=o06MyVhYte4)

Installing a specific package version with pip
- [python - Installing specific package version with pip - Stack Overflow](https://stackoverflow.com/questions/5226311/installing-specific-package-version-with-pip)

### Python logging

[Logging in Python – Real Python](https://realpython.com/python-logging/)

Many logging levels are available in [[Python programming|Python programming]] and allows you to fine-tune granularity of output messages as opposed to `print()`:

```
import logging

logging.debug('This is a debug message')
logging.info('This is an info message')
logging.warning('This is a warning message')
logging.error('This is an error message')
logging.critical('This is a critical message')
```

## Development environment

### Virtual environments in python

- Encapsulates dependencies such as packages from project to project allowing them to become more portable
- Creating a portable dev environment and syncing it to the git repo
	- `pip freeze > requirements.txt` creates a requirements file in the environments
	- `git add requirements.txt` adds it into the repo itself

### Maintaining a consistent dev environment

[[2023-11-23]] I was running into the problem of trying to sync my environment between my desktop computer and my laptop. And right now, the way you do it is that you create a virtual environment, create a freeze requirement, and then ship that over. Somewhat laborious

The `pipenv` package may make my life easier. TBD for future coding projects.
```python
$ pip install --user pipenv
```
[Pipenv: Python Dev Workflow for Humans — pipenv 2023.11.16.dev0 documentation](https://pipenv.pypa.io/en/latest/)

## Best practices for comments and legible code

- Use descriptive names for variables and functions - we should be able to infer behaviour from it
- Writing too many comments means people might skip it. *Why use many words when good name do trick?*
- Comments should be used when needed - when something may not be obvious.

More elegant code:

```python
def warn_if_book_is_overdue():
  for borrow_record in get_borrow_data():
    for book in borrow_record:
      return_due_string = f'{book['date_returned']} {book['time_returned']}'
      return_due_date = datetime.strptime(return_due_string, "%Y/%m/%d %I:%M:%p")
      overdue_hours = (datetime.now() - return_due_date).total_seconds() / 3600
      if overdue_hours > 0 and !book['return_status']:
        print("Please return the book")
```

Written by [someone less experienced](https://www.reddit.com/r/learnprogramming/comments/18bfesf/how_do_software_engineers_with_years_in_the/):

```python
def date_warning(): #warn students that there book is not yet returned
#for a day or two or more
borrow_records = []
borrow_records.append(get_borrow_data()) #Appending the loaded json to be incremented
for x in borrow_records: #First increment 
    for b in x: #Second increment Note: Should have use the json dumps or json loads
        current_datetime = datetime.now() #Get the current time and date
        ret_date = b['date_returned'] #return date
        ret_time = b['time_returned'] #return time

        return_stat = b['return_status'] #return status boolean true or false
        #return_stat is only true if a book is returned and false if not

        date_time_ret = f'{ret_date} {ret_time}' #Combine both into a string

        #turn date_time_ret into a strptime formats
        initial_ret = datetime.strptime(date_time_ret, "%Y/%m/%d %I:%M:%p")
        current_datetime = datetime.now() #Get current time and date 

        #Calculate the total amount of hours to be calculated and turned into fines
        current_data = (current_datetime - initial_ret).total_seconds() / 3600
        if current_data != 0 and return_stat == False: #Sending a message if the return_stat = false
            #And the current_data !=0 means that if its 0 hence it still has time left to be returned
            print("Please return the book")
```


## Decorators

- They modify the behavior of a function without modifying the thing itself - it's like an intercept?
- In flask, the decorator of `@app.route("/home")` is used to specific a web page such as in this case the page `home`