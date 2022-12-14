# Regex Expression Explained

Regex is a shorthand term for "regular expression," which is a line of unique characters that describe a specific search pattern. Regular expressions are powerful tools used to identify specific characters, or even replace them within a string. Popular use of regex is found within input validation. 

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

NOTE: Throughout this lesson we will use the following regex expression to draw examples from:
Matching an email: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
--
The matching an email regex expression looks entirely cryptic at first glance, but after reading this document you will be able to identify the various search parameters and notations described within the expression. 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components
Because regex expressions are considered to be a literal, the pattern must be wrapped in slash characters (/). The subsections below explain various types of regex components and their use.
If we look at our "matching an email" regex expression we can see it is wrapped in slash characters: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

### Anchors
Anchors (^) identify a string that starts with the character(s) that succeeds it. The $ anchor identifies a string that ends with certain characters that precede it. 
Two possible anchor variations exist: 
- Exact string match anchors.
- Range of possible match anchors using bracket expressions. 

In our "matching an email" regex expression the anchor tells us that the string we are looking for must start and end with the following pattern: [a-z0-9_\.-]


### Quantifiers
Quantifiers allow you to limit strings to certain parts of your regex matches, or even specify particular parts of strings to further narrow your search. Quantifiers tend to include min and max numerical values. In our regex expression above, we see the quantifiers {2,6} which means that we are looking for a sequence of characters between 2 and 6 characters long. 

Quantifiers can be classified as "greedy" matches (which is covered in a later subsection). Put simply, a greedy match will find as many occurrences of a specified pattern as possible. The various types of greedy matches are listed within the[Greedy and Lazy Match](#greedy-and-lazy-match) section of this document.  

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing
When dealing with larger stringers it is helpful to break the string up into parts to identify search parameters. This is where **grouping constructs** come into play. 
In order to group a regex section we must use a set of paranetheses (()). Each section inside a set of paranetheses is called a **subexpression**. 
For example, if we look at our email matching regex we can see two grouped sections: ([\da-z\.-]+)\.([a-z\.]{2,6})
The two groupings are both within the paranetheses, so broken up they are ([\da-z\.-]+) and ([a-z\.]{2,6}). These two groupings are separated by "\."

### Bracket Expressions
Bracket expressions, or a positive character group, are anything inside a set of square brackets ([]) -- they express a range of characters that are to be matched. 
Example: [abc] searches for a string that contains "a" or "b" or "c." 

In order to represent a range of possible characters amidst alphanumeric characters, a hyphen (-) is used. 
Example: [a-c] = [abc].

Negative character groups are also accessed through bracket notation. For example: [^abcdABCD] would find any string that does NOT include the lowercase OR uppercase letters "abcd."
This negative character aspect is described by the anchor (^) as previously described. 


### Greedy and Lazy Match
**Greedy matches**
As previously described, greedy matches aim to find the most possibel occurences of a particular specified pattern. 
The various types of greedy matches are listed below:
* - Matches the pattern 0 or more times.
+ - Matches the pattern 1 or more times.
? - Matches the pattern 0 or one time. 
Curly brackets ({}) further define three more ways to set limits:
    - {n} - matches the pattern n number of times.
    - { n, } - matches the pattern at least n number of times.
    - { n, x} - matches the pattern a minimum of n times and a max of x times. 

**Lazy matches**
Lazy matches are created simply by adding a question mark (?) after a greedy expression. This means that the lazy match will match as few occurrences as possible. 


### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
