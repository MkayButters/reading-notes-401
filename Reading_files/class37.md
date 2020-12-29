# Machine Learning


- Machine learning is not about algorithms. When you open a textbook or a university syllabus, you'll often be greeted by a grocery list of algorithms. This has fueled the misconception that machine learning is about mastering dozens of algorithms. However, it's much more than that.

- Machine learning is a comprehensive approach to solving problems and individual algorithms are only one piece of the puzzle. The rest of the puzzle is how you apply them the right way.

- Machine learning is the practice of teaching computers how to learn patterns from data, often for making decisions or predictions. For true machine learning, the computer must be able to learn patterns that it's not explicitly programmed to identify.

- Academic machine learning starts with and focuses on individual algorithms. However, in applied machine learning, you should first pick the right machine learning task for the job.

    - A task is a specific objective for your algorithms.
    - Algorithms can be swapped in and out, as long as you pick the right task.
    - In fact, you should always try multiple algorithms because you most likely won't know which one will perform best for your dataset.

- The two most common categories of tasks are supervised learning and unsupervised learning. (There are other tasks as well, but the concepts you'll learn in this course will be widely applicable.)

- Categorical features cannot be visualized through histograms. Instead, you can use bar plots. In particular, you'll want to look out for sparse classes, which are classes that have a very small number of observations.

- By the way, a "class" is simply a unique value for a categorical feature. For example, the following bar plot shows the distribution for a feature called 'exterior_walls'. So Wood Siding, Brick, and Stucco are each classes for that feature.


- Data cleaning is one those things that everyone does but no one really talks about. Sure, it’s not the "sexiest" part of machine learning. And no, there aren’t hidden tricks and secrets to uncover. However, proper data cleaning can make or break your project. Professional data scientists usually spend a very large portion of their time on this step.

- The simple truth in machine learning is better data beats fancier algorithms. In other words... garbage in gets you garbage out. Even if you forget everything else from this course, please remember this point. In fact, if you have a properly cleaned dataset, even simple algorithms can learn impressive insights from the data! Obviously, different types of data will require different types of cleaning. However, the systematic approach laid out in this lesson can always serve as a good starting point.


- Unfortunately, from our experience, the 2 most commonly recommended ways of dealing with missing data actually suck.

    1. Dropping observations that have missing values
    2. Imputing the missing values based on other observations


- In applied machine learning, individual algorithms should be swapped in and out depending on which performs best for the problem and the dataset. Therefore, we will focus on intuition and practical benefits over math and theory.

- Simple linear regression models fit a "straight line" (technically a hyperplane depending on the number of features, but it's the same idea). In practice, they rarely perform well. We actually recommend skipping them for most machine learning problems.

- Their main advantage is that they are easy to interpret and understand. However, our goal is not to study the data and write a research report. Our goal is to build a model that can make accurate predictions.



[<===BACK](../README.md)
