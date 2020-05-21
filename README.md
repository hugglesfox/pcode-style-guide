# The Non Definitive Guide to the Wonders of NickCode

This is a living document which aims to be the best guide possible to the pseudocode flavour created by Dr Nick Patterson for SIT105 (which will be referred to as nickcode for the rest of the document). This document is not officially endorsed by Dr Patterson therefore **use at own risk** but with the amount of confusion around nickcode and the ambiguity of the Assignment 3 marking rubric, we thought that a formal definition of nickcode was required. Inspiration for the following guide has been taken from Dr Patterson's Cloud practicals and lectures as well as the Python and Rust programming languages.

## Contents

// TODO

## 1. Comments

A comment is a line of text which is marked by a `//` at the start of the line which is used for making notes about your code without affecting the algorithm in any way. Comments should have a space between the `//` and the start of the comment.

Inline comments should be defined 2 spaces after the line of code.

```
// This is a comment

x = 1  // This is an inline comment

//Please don't do this. Put a space between the // and the P

```

## 2. Types

Types are data structures used to hold various different representations of data.

### 2.1. Strings

Strings are a data structure which contain one or more characters. Strings are defined by surround characters in either single or double quotation marks as long as the use of single or double quotation marks is consistent throughout the code.

```
"This is a string"
'This is also a string'

'This is not a string as the quotation marks used to wrap the text are not the same"
```

### 2.2. Integers

### 2.3. Floating point integers

### 2.4. Booleans

Booleans are a binary data type meaning they have 1 of two possible values (true or false). Booleans should be use pascal case.

```
// Good
True
False

// Bad
true
false
TRUE
FALSE
```

### 2.5. Tuples

### 2.6. Arrays

### 2.7. Hashmaps (Dictionaries)

### 2.8. A note on type casting

Automatic.

## 3. Operators

Operators are used to manipulate variables. All operators should be spaced out for readability and compliance.

```
// Good
x = 1 + 1

// Bad
x=1+1
```

### 3.1. Integer operations

Integer operations is a fancy word for maths.

#### 3.1.1. Addition

```
x = 1 + 1  // x returns 2
```

#### 3.1.2. Subtraction

```
x = 2 - 1  // x returns 1
```

#### 3.1.3. Multiplication

```
x = 2 * 2  // x returns 4
```

#### 3.1.4. Division

```
x = 4 / 2  // x returns 2
```

#### 3.1.5. Modulo

Modulo returns the remainder of a division operation.

```
x = 5 % 4  // x returns 1
```

#### 3.1.6. Powers

The syntax of powers does not have a space between operators.

```
x = 2^2  // x returns 4
```

#### 3.1.7. Equivalent

An `==` operator checks if the two values are the same and returns a Boolean.

```
1 == 1  // Returns TRUE

1 == 2  // Returns FALSE
```

An `!=` operator checks if the two values are different and returns a Boolean.

```
1 != 1  // Returns FALSE

1 != 2  // Returns TRUE
```

#### 3.1.8. Greater then and Less then

A `>` operator checks if the value on the left is greater than the value on the right.

```
2 > 1  // Returns TRUE

1 > 2  // Returns FALSE
```

A `<` operator checks if the value on the left is less than the value on the right.

```
1 < 2  // Returns TRUE

2 < 1  // Returns FALSE
```

### 3.2. String operations

Manipulate strings using operators.

#### 3.2.1. Concatenation (Addition)

Uses the `+` operator to combine two strings into one. Remember to include spacing as it just combines the content of the strings.

```
PRINT "Hello " + "World"  // Returns "Hello World"

PRINT "Hello" + "World"  // Returns "HelloWorld"
```

Variables can also be concatenated into strings with this method.

```
x = "World"
PRINT "Hello " + x  // Returns "Hello World"

x = 1 + 1
PRINT "1 + 1 = " + x  // Returns "1 + 1 = 2"
```

#### 3.2.2. Equivalent

An `==` operator checks if the two strings are the same and returns a Boolean.

```
"foo" == "foo"  // Returns TRUE

"foo" == "bar"  // Returns FALSE
```

You can also use a `!=` operator to check if the two strings are different and return a Boolean.

```
"foo" != "bar"  // Returns TRUE

"foo" != "foo"  // Returns FALSE
```

### 3.3. Boolean Logic

Boolean logic has two states, TRUE and FALSE. Boolean states can be combined with logic to output another state.

#### 3.3.1. AND

The AND operator requires both Booleans on each side to return TRUE to return TRUE.

```
TRUE AND TRUE  // Returns TRUE

TRUE AND FALSE  // Returns FALSE

FALSE AND FALSE  // Returns FALSE

1 == 1 AND 2 > 1  // Returns TRUE
```

#### 3.3.2. OR

The OR operator only requires one Boolean to be TRUE to return TRUE.

```
TRUE OR TRUE  // Returns TRUE

TRUE OR FALSE  // Returns TRUE

FALSE OR FALSE  // Returns FALSE

1 == 1 OR 1 > 2  // Returns TRUE
```

#### 3.3.1. NOT

The NOT operator reverses a Boolean value, so a TRUE becomes FALSE and FALSE becomes TRUE.

```
NOT TRUE  // Returns FALSE

NOT FALSE  // Returns TRUE

x = 1 > 2
NOT x  // Returns TRUE
```

## 4. Variables

## 5. Scope

Indentaion

## 6. Modules

> NOTE for writers: Make a note on how cohesion actually works and why having a million modules is a bad idea.

### 6.2. Arguments

### 6.1. RETURN

## 7. Builtins

Built in modules should be capitalised and do not use parenthesis to pass arguments unlike user defined modules for an example

```
// Good
DISPLAY "Hello World"

// Bad
DISPLAY("Hello World")
```

### 7.1. DISPLAY

The `DISPLAY` builtin writes a string to the display or console.

```
DISPLAY "Hello World"
```

The above code will write `Hello World` to the console.

### 7.2. PRINT

The `PRINT` builtin writes a string to a printer. This is primarily used for interfacing with [teleprinters](https://en.wikipedia.org/wiki/Teleprinter).

```
PRINT "Why are you using a printer in 2020?"
```

The above code will print a page with the text `Why are you using a printer in 2020?`.

### 7.3. READ

The `READ` builtin reads a string from either user input or a file.

```
file_content = READ "file_path"
```

Here the contents a readable thing (such as a file) called `file_path` is written to the variable `file_content`.

### 7.4. IF

The `IF` builtin checks whether a condition is true and only then will it run the resulting code in the form

```
IF condition THEN
    // Code here is ran if condition evaluates to true.
ENDIF
```

where `THEN` marks the end of the condition and `END` marks the end of the scope of the `IF` statement.

An example of `IF` which doubles a number if the number is greater then 1 could be

```
x = READ "Enter a number: "  // Read a number from user input

IF x > 1 THEN  // Check to see if the inputted number is greater then 1
    x = x * 2  // Double x
ENDIF
```

### 7.5. ELSEIF

### 7.6. ELSE

### 7.7. CASE

> NOTE for writers: Do you think we could get away with ditching DOWHILE and DO for just WHILE and FOR?

### 7.8. WHILE

### 7.9. DOWHILE

### 7.10. DO

### 7.11. OPEN/CLOSE

### 7.12. Main()

## 8. Objects?

> NOTE for writers: Do we want objects? I'm thinking just to keep it flat like C.

## 9. Citing

It is not required to cite this document if you wish to reference it for your assignment 3 but if you appreciate the work we would kindly ask you to include the following sentence in your assignment:

> The pseudocode provided has been created with reference to [The Non Definitive Guide to the Wonders of NickCode](https://github.com/hugglesfox/pcode-style-guide)

## 10. Contributing

This guide is a living document. If you wish to add to it or modify it at all then please feel free to make a pull request. Your contributions will always be warmly welcome.
