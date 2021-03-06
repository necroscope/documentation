---
title: TEXT expression
parent: Expressions
tags: command expressions
comments: true
---


### Description
`TEXT`, as the name suggest, treats its input as text.  All its operations treat their respective input as text as well.


### Operations
- **`after(criteria)`** \- retain the portion of text after the specified `criteria`.
- **`append(text,text,text,...)`** \- add one or more text to the end of `text`.
- **`appendIfMissing(appendWith)`** - add `appendWith` to the end of current text ONLY if `appendWith` is currently 
  not at the end of text
- **`before(criteria)`** \- retain the portion of text before the specified `criteria`.
- **`between(start,end)`** \- retain the portion of text that is between the specified `start` and `end` text.
- **`count(searchFor)`** \- transfer into a [`NUMBER`](NUMBERexpression) data type that contains the number of 
  occurrence for `searchFor`.
- **`csv(position1,position2,...)`** - converts the given text content to csv format, separated by the given position 
  numbers for each line.
- **`distinct`** \- remove any duplicate characters from text.
- **`insert(after,text)`** \- search for `after` in text, and if found, add the specified text to it.  If `after` is 
  not found, no changes will be made to text.
- **`length`** \- transfer into a [`NUMBER`](NUMBERexpression) data type that contains the length of text.
- **`list(delim)`** \- transfer into a [`LIST`](LISTexpression) data type by converting text into a list, using 
  `delim` as the character to split.
- **`lower`** \- turn text into lowercase equivalent.
- **`number`** \- transfer into a [`NUMBER`](NUMBERexpression) data type by converting text into a numeric value.  
  Failure to explicitly convert text into number will result in an ERROR condition.
- **`normalize`** \- remove any leading or trailing whitespaces and also remove duplicate whitespace characters in 
  text. The end result is that text will not contain any occurrences of successive spaces.
- **`pack`** \- remove all whitespace characters (tab, space, line feed, carriage return) from text.
- **`prepend(text,text,text,...)`** \- add one or more text to the beginning of `text`.
- **`prependIfMissing(prependWith)`** - add `prependWith` to the beginning of current text ONLY if `prependWith` if 
  currently not at the beginning of text
- **`remove(criteria)`** \- remove any and all occurrences of `criteria`.
- **`removeEnd(ending)`** / **remove-end(ending)** \- remove ending character sequence (substring) of text that 
  matches `ending`.
- **`removeStart(start)`** / **remove-start(start)** \- remove starting character sequence (substring) of text that 
  matches `start`.
- **`replace(searchFor,replaceWith)`** \- as the name suggest, this operation will search for `searchFor` and replace 
  matches with `replaceWith`.
- **`replaceRegex(searchRegex,replaceWith)`** - perform a regex-search on text using `searchRegex` and replace all 
  matches with `replaceWith`.  Note that grouping character `(` and `)` should be escaped as `\(...\)`.  For example, 
  `[TEXT(...) => replaceRegex(**\(chicken\)**,beef)]`
- **`store(var)`** \- save current TEXT expression to a data variable.  If the specified `var` exists, its value will 
  be overwritten.  Using this operation, one can put an expression on pause and resume it at a later time.
- **`substring(start,end)`** \- retain the portion of text from the `start` position (zero-based) to the `end` 
  position (exclusive).
- **`title`** - turn text into Title Case, while the first letter of every word is capitalized.
- **`trim`** \- remove any non-printable character in the beginning or ending of text.
- **`upper`** \- turn text into UPPERCASE equivalent.


### Example
Example 1 - chain up a "upper" and a "append":<br/>
![](image/TEXTexpression_01.png)

**Output**:<br/>
![](image/TEXTexpression_02.png)

Example 2 - find uniqueness, and change text<br/>
![](image/TEXTexpression_03.png)

**Output**:<br/>
![](image/TEXTexpression_04.png)

Example 2 - Convert the given text content to csv format separated by the given positions. Text input could be a 
text itself or a path to text file.

In this example, after converting to csv format, it saves the csv content to the given output file path.

Date file:<br/>
![](image/TEXTexpression_05.png)

**Script**:<br/>
![](image/TEXTexpression_06.png)

**Output**:<br/>
![](image/TEXTexpression_07.png)
