## Pain and suffering

- All growth comes with some degree of pain, as it pulls you out of your comfort zone. The greater the growth, the greater the pain. But pain in the service of growth is a good thing, as long as that pain is what’s necessary to achieve the growth that you’re aiming for. And even better than that, this pain is only temporary. It’s what will launch you forward into the next phase of your life.

## The Big O

- Big O notation is used in Computer Science to describe the performance or complexity of an algorithm. Big O specifically describes the worst-case scenario, and can be used to describe the execution time required or the space used (e.g. in memory or on disk) by an algorithm.


1. __O(1)__ describes an algorithm that will always execute in the same time (or space) regardless of the size of the input data set.

2. __O(N)__ describes an algorithm whose performance will grow linearly and in direct proportion to the size of the input data set. The example below also demonstrates how Big O favours the worst-case performance scenario; a matching string could be found during any iteration of the for loop and the function would return early, but Big O notation will always assume the upper limit where the algorithm will perform the maximum number of iterations.

3. __O(N2)__ represents an algorithm whose performance is directly proportional to the square of the size of the input data set. This is common with algorithms that involve nested iterations over the data set. Deeper nested iterations will result in O(N3), O(N4) etc.

4. __O(2N)__ denotes an algorithm whose growth doubles with each additon to the input data set. The growth curve of an O(2N) function is exponential - starting off very shallow, then rising meteorically. 

5. __Binary search__ is a technique used to search sorted data sets. It works by selecting the middle element of the data set, essentially the median, and compares it against a target value. If the values match it will return success. If the target value is higher than the value of the probe element it will take the upper half of the data set and perform the same operation against it. Likewise, if the target value is lower than the value of the probe element it will perform the operation against the lower half. It will continue to halve the data set with each iteration until the value has been found or until it can no longer split the data set.

[<===BACK](../README.md)
