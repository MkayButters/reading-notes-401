# Pythonism

In Python, special methods are a set of predefined methods you can use to enrich your classes. They are easy to recognize because they start and end with double underscores, for example __init__ or __str__.

As it quickly became tiresome to say under-under-method-under-under Pythonistas adopted the term “dunder methods”, a short form of “double under.”

These “dunders” or “special methods” in Python are also sometimes called “magic methods.” But using this terminology can make them seem more complicated than they really are—at the end of the day there’s nothing “magical” about them. You should treat these methods like a normal language feature.

Dunder methods let you emulate the behavior of built-in types. For example, to get the length of a string you can call len('string'). 


We’ll begin by writing a class that demonstrates the bare-bones iterator protocol in Python. The example I’m using here might look different from the examples you’ve seen in other iterator tutorials, but bear with me. I think doing it this way gives you a more applicable understanding of how iterators work in Python.

Again, RepeaterIterator looks like a straightforward Python class, but you might want to take note of the following two things:

In the __init__ method we link each RepeaterIterator instance to the Repeater object that created it. That way we can hold on to the “source” object that’s being iterated over.

In RepeaterIterator.__next__, we reach back into the “source” Repeater instance and return the value associated with it.

In this code example, Repeater and RepeaterIterator are working together to support Python’s iterator protocol. The two dunder methods we defined, __iter__ and __next__, are the key to making a Python object iterable.

We’ll take a closer look at these two methods and how they work together after some hands-on experimentation with the code we’ve got so far.

Let’s confirm that this two-class setup really made Repeater objects compatible with for-in loop iteration. To do that we’ll first create an instance of Repeater.

You’ll rightfully expect this code to print the numbers 1, 2, and 3 and then stop. And you probably don’t expect it to go on spamming your terminal window by printing threes forever until you mash Ctrl+C a few times in a wild panic…

And so, it’s time to find out how to write an iterator that eventually stops generating new values instead of iterating forever. Because that’s what Python objects typically do when we use them in a for-in loop.

We’ll now write another iterator class that we’ll call BoundedRepeater. It’ll be similar to our previous Repeater example, but this time we’ll want it to stop after a predefined number of repetitions.

Let’s think about this for a bit. How do we do this? How does an iterator signal that it’s exhausted and out of elements to iterate over? Maybe you’re thinking, “Hmm, we could just return None from the __next__ method.”

And that’s not a bad idea—but the trouble is, what are we going to do if we want some iterators to be able to return None as an acceptable value?

Let’s see what other Python iterators do to solve this problem. I’m going to construct a simple container, a list with a few elements, and then I’ll iterate over it until it runs out of elements to see what happens:

To make this iterator class compatible with Python 2 I’ve made two small changes to it:

First, I added a next method that simply calls the original __next__ and forwards its return value. This essentially creates an alias for the existing __next__ implementation so that Python 2 finds it. That way we can support both versions of Python while still keeping all of the actual implementation details in one place.

And second, I modified the class definition to inherit from object in order to ensure we’re creating a new-style class on Python 2. This has nothing to do with iterators specifically, but it’s a good practice nonetheless.








[<===BACK](../README.md)
