# IndentationError
### What is IndentationError?

A Error that raises for space mistakes. A Subclass of SyntaxError. 
> [Base class for syntax errors related to incorrect indentation. This is a subclass of SyntaxError.](https://docs.python.org/3/library/exceptions.html/#IndentationError)

### Some Examples of error makeover the error:
#### Ex1: expected an indent block
```py
if 'Hello':
print('give this indent')
```
**Correct form:**
```py
if 'Hello':
    print('given indent')
```

#### Ex2: unexpected indent
```py
def hello():
    h = input('> ')
   print(h)
```
**Correct Form:**
```py
def hello():
    h = input('> ')
    print(h)
```
_**Similar As:**_
```py
  print('test')
```
*Correct Form:*
```py
print('test')
```

### Some More Info On Raising Indentation Error:
#### Simple raise syntax
```py
raise IndentationError('Give me indent block')
```
**Result:**

```
Traceback (most recent call last):
  File "/home/errors/test.py", line 1, in <module>
    raise IndentationError('hello')
IndentationError: Give me indent block
```

#### Custom error with detailed info
```py
error = IndentationError('hello!')

error.msg = error.msg+' I am indent'

error.lineno = 100

error.filename='errorfile.py'

raise error
```
**Result:**
```
Traceback (most recent call last):
  File "<filename>", line 1, in <module>
  File "errorfile.py", line 100
IndentationError: hello! I am indent
```
----


* **ID of IndentationError:** 2879828888
--------

