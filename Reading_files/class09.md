## Dunder Methods

- In Python, special methods are a set of predefined methods you can use to enrich your classes. They are easy to recognize because they start and end with double underscores, for example __init__ or __str__.

- Various dunder methods to unlock the following language features:

1. Initialization of new objects
2. Object representation
3. Enable iteration
4. Operator overloading (comparison)
5. Operator overloading (addition)
6. Method invocation
7. Context manager support (with statement)

- It’s common practice in Python to provide a string representation of your object for the consumer of your class (a bit like API documentation.) There are two ways to do this using dunder methods:

    - __repr__: The “official” string representation of an object. This is how you would make an object of the class. The goal of - __repr__ is to be unambiguous.

    - __str__: The “informal” or nicely printable string representation of an object. This is for the enduser.

- As with any feature, please don’t overuse it. Operator overloading, for example, can get pretty obscure. Adding “karma” to a person object with +bob or tim << 3 is definitely possible using dunders—but might not be the most obvious or appropriate way to use these special methods. However, for common operations like comparison and additions they can be an elegant approach.

## Probability

- At the most basic level, probability seeks to answer the question, “What is the chance of an event happening?” An event is some outcome of interest. To calculate the chance of an event happening, we also need to consider all the other events that can occur.

- The normal distribution is significant to probability and statistics thanks to two factors: the Central Limit Theorem and the Three Sigma Rule.

    - The Central Limit Theorem dictates that the distribution of these estimates will look like a normal distribution. The zenith of this distribution will line up with the true value that the estimates should take on. In statistics, the peak of the normal distribution lines up with the mean, and that’s exactly what we observed. Thus, given multiple “trials” as our data, the Central Limit Theorem suggests that we can hone in on the theoretical ideal given by probability, even when we don’t know the true probability. Central Limit Theorem lets us know that the average of many trials means will approach the true mean, the Three Sigma Rule will tell us how much the data will be spread out around this mean.

- From probability, we developed a way to quantatively show if two groups come from the same distribution. In this case, we compared two wine recommendations and found that they most likely do not come from the same score distribution. In other words, one wine type is most likely better than the other one. Statistics doesn’t have to be a field relegated to just statisticians. As a data scientist, having an intuitive understanding on common statistical measures represent will give you an edge on developing your own theories and the ability to subsequently test these theories. We barely scratched the surface of inferential statistics here, but the same general ideas here will help guide your intuition in your statistical journey. Our article discussed the advantages of the normal distribution, but statisticians have also developed techniques to adjust for distributions that aren’t normal.


[<===BACK](../README.md)
