## Automation

Regular Expressions, often shortened as regex, are a sequence of characters used to check whether a pattern exists in a given text (string) or not. If you've ever used search engines, search and replace tools of word processors and text editors - you've already seen regular expressions in use. They are used at the server side to validate the format of email addresses or passwords during registration, used for parsing text data files to find, replace, or delete certain string, etc. They help in manipulating textual data, which is often a prerequisite for data science projects involving text mining.

- In Python, regular expressions are supported by the re module. That means that if you want to start using them in your Python scripts, you have to import this module with the help of import. The re library in Python provides several functions that make it a skill worth mastering. You will see some of them closely in this tutorial.

- You can easily tackle many basic patterns in Python using ordinary characters. Ordinary characters are the simplest regular expressions. They match themselves exactly and do not have a special meaning in their regular expression syntax.

- The match() function returns a match object if the text matches the pattern. Otherwise, it returns None. The re module also contains several other functions, and you will learn some of them later on in the tutorial.

- With the search function, you scan through the given string/sequence, looking for the first location where the regular expression produces a match.
 
- The group function returns the string matched by the re. You will see both these functions in more detail later.

    - The group feature of regular expression allows you to pick up parts of the matching text. Parts of a regular expression pattern bounded by parenthesis () are called groups. The parenthesis does not change what the expression matches, but rather forms groups within the matched sequence. You have been using the group() function all along in this tutorial's examples. The plain match.group() without any argument is still the whole matched text as usual.


[<===BACK](../README.md)
