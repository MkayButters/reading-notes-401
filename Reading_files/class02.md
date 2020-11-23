# Tests

- The test file name should follow the same name of module name. For instance, if our module is gender.py, our test name should be test_gender.py. It’s ideal to separate the tests folder from production code (the implementation) and to have something like this:

- AAA: Arrange, Act and Assert.
    1. Arrange: you need to organize the data needed to execute that piece of code (input);
    2. Act: here you will execute the code being tested (exercise the behaviour);
    3. Assert: after executing the code, you will check if the result (output) is the same as you were expecting.

- The cycle is made by three steps:
    1. 🆘 Write a unit test and make it fail (it needs to fail because the feature isn’t there, right? If this test passes, call the Ghostbusters, really)
    2. ✅ Write the feature and make the test pass! (you can dance after that)
    3. 🔵 Refactor the code — the first version doesn’t need to be the beautiful one (don’t be shy)


- The greatest advantage about TDD is to craft the software design first
- Your code will be more reliable: after a change you can run your tests and be in peace
- Beginning may be hard — and that’s fine. You just need to practice!

# Recursion

- The process in which a function calls itself directly or indirectly is called recursion and the corresponding function is called as recursive function. Using recursive algorithm, certain problems can be solved quite easily. 

- Soliving a problem with recursion: 
    - The idea is to represent a problem in terms of one or more smaller problems, and add one or more base conditions that stop the recursion.

- Difference between indirect and direct funcitons;
    - A function fun is called direct recursive if it calls the same function fun. A function fun is called indirect recursive if it calls another function say fun_new and fun_new calls fun directly or indirectly. 

__Recursive vs Iterative Programming;__

    Advantages:
    
        Recursion provides a clean and simple way to write code. Some problems are inherently recursive like tree traversals. We can write such codes also iteratively with the help of a stack data structure. 

    Disadvantages:

        The recursive program has greater space requirements than iterative program as all functions will remain in the stack until the base case is reached. It also has greater time requirements because of function calls and returns overhead.

[<===BACK](../README.md)
