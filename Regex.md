# Title (replace with your title)

Introductory paragraph (replace this with your text)

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors
Anchors are a collection of special characters used to indicate proper positioning within a line of code. Some primary examples are:

Caret '^', which indicates positioning at the start of a string
`const regex = /^Alpha/;`
`console.log(regex.test('Alpha Beta')); //true`
`console.log(regex.test('Beta Alpha')); //false`

Word Boundary '\b', indicates a boundary around the chosen word
`const regex = /\bXylophone\b/; //"Xylophone is a whole word, with nothing before or after`

### Quantifiers
Quantifiers are a collection of special characters used to indicate a number of characters, specifically how many are required for a match. Some primary examples are:

Asterisk '*', which means there must but 0 or more
`const regex = /\d*/;`
`const testStrings = ["1234"}; //true`

Question Mark '?', which means 0 or 1 of the element
`const regex = a?;`
`const testStrings = ["a"]; //true`
`const testStrings = ["aa"];//false`

### Grouping Constructs
Grouping Constructs are a collection of characters to group patterns together, to then quantify or capture, such as:

Parentheses '()', group patterns, usually for quantifiers for multiple elements
`const regex = /(Hey) (Jude!); //groups Hey and Jude separately`
`const string = 'Hey, Jude!';`
`console.log(regex.test(str)); //Output: true`

Named Capturing Groups '(?<name>)', which capture a substring as a name, to be accessed rather than as an index
`const regex = /(?<year>\d{4})-(?<month>\d{2})-(?<day>\d{2})/;`
`const str = '2024-07-31';`
`const match = str.match(regex);`
`if (match) {`
  `const { groups } = match;`
  `console.log(`Year: ${groups.year}`);  // Output: Year: 2024`
  `console.log(`Month: ${groups.month}`); // Output: Month: 07`
 ` console.log(`Day: ${groups.day}`);   // Output: Day: 31`
`} else {`
  `console.log('No match found');`
`}`
'const string = 
### Bracket Expressions
Bracket Expressions are a part of regular expressions which allow the user to match sets of characters, such as:

Negation '[^...]', which matches characters not listed 
`const regex = /[^aeiou]/g; // Matches any character that is not a vowel`
`const str = 'Hello, World!';`
`const matches = str.match(regex);`
`console.log(matches); // Output: [ 'H', 'l', 'l', ',', ' ',` `'W', 'r', 'l', 'd', '!' ]`

### Character Classes
Character Classes, like Bracket Expressions, specifies a set of characters for matching, such as:
Basic Character Class '[...]', which takes any single character for matching
`const regex = /[xyz]/; //Matches any single 'x', 'y', or 'z'`
`Ranges '[a-z]', matches characters between the two`
`const regex = /[c-w]/; //Matches any lowercase letter between c and w`

### The OR Operator
The OR Operator matches one or the other, indicated by the '|' symbol
`const regex = /cat|dog/g; // Matches either "cat" or "dog"`
`const str = 'I have a cat and a dog.';`
`const matches = str.match(regex);`
`console.log(matches); // Output: [ 'cat', 'dog' ]`

### Flags
Flags modify the behavior of pattern matching, changing how the regular expression is processed. They are typically found at the end of the expression, such as:

Global 'g', which indicates a global search for matches
`const regex = /a/g; //Search for 'a', finding all matches`
`const str = 'apple and banana';`
`const matches = str.match(regex);`
`console.log(matches); // Output: ['a', 'a', 'a']`

Case Insensitive 'i', ignores upper and lower case in matching
`const regex = /hello/i; // Case-insensitive search for 'hello'`
`const str = 'Hello, World!';`
`const match = str.match(regex);`
`console.log(match); // Output: ['Hello']`

### Character Escapes
Character Escapes match special characters which might otherwise have their own interpretation, such as:

Backslash '\', creates a sequence ignoring the next character's programming meaning
`const regex = /a\.b/; // Matches 'a.b'`
`const str = 'a.b';`
`console.log(regex.test(str)); // Output: true`

Whitespace '\s', matches whitespace characters
`const regex = /\s+/; // Matches one or more whitespace ``characters`
`const str = 'Hello World';`
`console.log(regex.test(str)); // Output: true`

## Author
My name is Joey Sandoval, my Github link is below:
https://github.com/wol42verine
