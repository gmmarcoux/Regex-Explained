# Title (replace with your title)
RegEx, or regular expressions, are useful for identifying patterns and arrays among symbols, characters, and/or phrases. This tutorial exists to help developers looking to understand the RegEx "Matching an Email."

## Summary
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

This snippet of code, albeit almost nonsensical to the untrained eye, aims to search for patterns that make up the requirements that must be passed in order for one to have a ratified email account. Essentially, at the end of this tutorial, this code should show you how it matches to the requirements set forth within the string to validate an email account with a name + @provider + .com.

## Table of Contents
- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components
    Because ReGex's are wrapped in "/..../," they are considers literal. There are several main components of Regex's that we will cover, inluding Anchors, Quantifiers, OR operators, Character classes, Grouping and capturing, Bracket expressions, Greedy and lazy matches, Boundaries, Back-references, and Look-ahead Look-behind. 

### Anchors
    Anchors: ^ symbolizes the beginning of the string, and $ indicates the end of a string. 

This can bee seen in the above example of matching emails at the start and ending of the string with "/^([...)$/".

### Quantifiers
    Quantifiers: denote the requirments that need to be met to match emails, matching as many patterns as they can. There are several quanitifiers, not limited to, but including *, {}, ?, +, { n }..., all denoting the amount of times a pattern is matched. 

In the "Matching an Email" ReGex, there is a quantifier of "{2, 6}." This matches the quantifier "{ n. x }," which matches a pattern to a minimum (n) of 2, and maximum (x) of 6. 
Prior to this quantifier, the use of "+" is used two times in the ReGex. The + sign signifies the matching of a pattern at least once. In laymen's terms, the + sign helps connect the limits for the user's name + email provider + .com.
 
### Character Classes
    Character Classes: denotes the variety sets of characters that can be used to be a successful match; "{}" exist as a character class. 

Now let's look back at our Regex. There are several character classes we can point to within the string. 
There are 3 "." in the Regex, and a "/d." Periods, in ReGexes, indicate the end of one line and beginning of another, and the "/d" stands for any number between 0-9. 

### Grouping and Capturing
    Grouping constructs in Regex's is done with "()." There are two kinds of grouping, which include capturing, and noncapturing. Capturing groups focus on saving the constrcuts for reuse, and grouping can be made non-capturing with the addition og "?:" preceeding the contruct within the parathensis. 

In this email ReGex, there are three captured groups. 
1. ([a-z0-9_\.-]+) -> email name
2. ([\da-z\.-]+) -> email provider (mac, yahoo, gmail)
3. ([a-z\.]{2,6}) -> .com

### Bracket Expressions
    Bracket expressions, "[]," indicate a range of character possibilities that are the target of the matchings. 

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
The Regex above has several bracket expressions. 
    [a-z0-9_\.-] - This bracket implies that the string can be created from 1.) any lowercase letter between a-z; 2.) any number 0-9; and 3.) the special characters, "-" and "_" can be used in the string. 
    [\da-z\.-] - Similarly to the first bracket expression, "/d" is a shorted version of "0-9," as it indicates any Arabic numeral, and indluces the letters a-z.
    [a-z\.] - The letters a-z.

### Greedy and Lazy Match
    Greedy matching is predominantly done to find the maximum patterns in an array of characters, whereas lazy matching matches the pattern either once, or no times at all, to acheive the fewest matches as possible.

An example of a greedy match in this ReGex is the use of "+," as it means the snippet will keep matching to the previous one to unlimitied times.


## Author
Gracie Marcoux recently graduated from Texas A&M with a degree in Psychology, with an additional certification in The Psychology of Diversity and minor in Anthropology. They are now veering into the big world of technology and coding, hoping to do their best and make a difference in a virtual world that a majority of people nowadays live in. 
### Github 
    https://github.com/gmmarcoux
