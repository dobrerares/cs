# Tuple packing and unpacking
```python
def function()->tuple:
	return "abcd", 1234

x=function()
# x = ("abcd", 1234)
```

Here x gets the whole tuple

```python
def function()->tuple:
	return "abcd", 1234

x,y=function()
# x = "abcd"
# y = 1234
```

The tuple returned by the function will be unpacked automatically

>[!Important]
>If there we are trying to unpack a tuple with less elements than the number of variables python will throw an error

# User Interface
Don't use `print()` and `input()` functions outside of the user interface functions (outside of some special cases i.e. assignment 2 with the sort functions)