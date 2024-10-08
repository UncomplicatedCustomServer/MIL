# MIL
Medium Intermediate Language is a simple, easy to use and fast solution to create universal executable scripts.

## Some useful informations
- every input string is encoded with `base64`
- MIL works with an advanced evaluation stack

## Basic syntax
The basic syntax for an action is the following
```
action args
```
every action is a string.\
For example:
```
def myVar
```
```
call MyBeautifulMethod
```

## Function definion
You can define functions in MIL through the `deffunc` action:
```
deffunc MyFunction
print ITALY IS BEAUTIFUL
enddef
```
You can also add arguments:
```
deffunc MyFunction
defarg name
ld name
print {0} IS BEAUTIFUL
enddef
```

## Variables
With MIL you can create, define, load and edit vars.
```
# define a var
def myVar

# assign it a value
str magic
sv myVar
# (Now myVar = "magic")

# load a value to call the function MyFunction(name)
callfunc MyFunction
ld myVar
setarg name

# call the function MyFunction() and save the answer in myVar
vcallfunc MyFunction
sv myVar
```

## Clear the evaluation stack
You can clear the stack with the `cl` command
```
# clear the WHOLE evaluation stack
cl

# clear n elements from the evaluation stack
cl 2
```

