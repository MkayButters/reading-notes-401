## List Comprehensions

- List comprehensions provide a concise way to create lists.

- It consists of brackets containing an expression followed by a for clause, then zero or more for or if clauses. The expressions can be anything, meaning you can put in all kinds of objects in lists. The result will be a new list resulting from evaluating the expression in the context of the for and if clauses which follow it.

- The list comprehension always returns a result list.

 - The list comprehension starts with a __‘[‘__ and __‘]’__, square brackets, to help you remember that the
result is going to be a list.

- Examples of lower and upercasing syntax:

>`` [x.lower() for x in ["A","B","C"]]
['a', 'b', 'c']``

>``[x.upper() for x in ["a","b","c"]]
['A', 'B', 'C']]``

This example show how to extract all the numbers from a string:

>``string = "Hello 12345 World"
numbers = [x for x in string if x.isdigit()]
print numbers``

>``['1', '2', '3', '4', '5']``


[<===BACK](../README.md)
