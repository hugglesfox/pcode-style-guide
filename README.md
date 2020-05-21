# The Non Definitive Guide to the Wonders of NickCode

This is a living document which aims to be the best guide possible to the pseudocode flavour created by Dr Nick Patterson for SIT105 (which will be referred to as nickcode for the rest of the document). This document is not officially endorsed by Dr Patterson therefore **use at own risk** but with the amount of confusion around nickcode and the ambiguity of the Assignment 3 marking rubric, we thought that a formal definition of nickcode was required. Inspiration for the following guide has been taken from Dr Patterson's Cloud practicals and lectures as well as the Python and Rust programming languages.

## Contents

1. [Comments](#1-Comments)

2. [Types](#2-Types)

	2.1. [Strings](#21-Strings)

	2.2. [Integers](#22-Integers)

	2.3. [Floating point integers](#23-Floating-point-integers)

	2.4. [Booleans](#24-Booleans)

	2.5. [Tuples](#25-Tuples)

	2.6. [Arrays](#26-Arrays)

	2.7. [Hashmaps (Dictionaries)](#27-Hashmaps-Dictionaries)

	2.8. [A note on type casting](#28-A-note-on-type-casting)

3. [Operator](#3-Operators)

	3.1. [Integer operations](#31-Integer-operations)

		3.1.1. [Addition](#311-Addition)

		3.1.2. [Subtraction](#312-Subtraction)

		3.1.3. [Multiplication](#313-Multiplication)

		3.1.4. [Division](#314-Division)

		3.1.5. [Modulo](#315-Modulo)

		3.1.6. [Powers](#316-Powers)

		3.1.7. [Equivalent](#317-Equivalent)

		3.1.8. [Greater then and Less then](#318-Greater-then-and-Less-then)

	3.2. [String operations](#32-String-operations)

		3.2.1. [Concatenation (Addition)](#321-Concatenation-Addition)

		3.2.2. [Equivalent](#322-Equivalent)

	3.3. [Boolean Logic](#33-Boolean-Logic)

		3.3.1. [AND](#331-AND)

		3.3.2. [OR](#332-OR)

		3.3.1. [NOT](#331-NOT)

4. [Variables](#4-Variables)

5. [Scope](#5-Scope)

6. [Modules](#6-Modules)

	6.2. [Arguments](#62-Arguments)

	6.1. [RETURN](#61-RETURN)

7. [Builtins](#7-Builtins)

	7.1. [DISPLAY](#71-DISPLAY)

	7.2. [PRINT](#72-PRINT)

	7.3. [READ](#73-READ)

	7.4. [IF](#74-IF)

	7.5. [ELSEIF](#75-ELSEIF)

	7.6. [ELSE](#76-ELSE)

	7.7. [CASE](#77-CASE)

	7.8. [WHILE](#78-WHILE)

	7.9. [DOWHILE](#79-DOWHILE)

	7.10. [DO](#710-DO)

	7.11. [OPEN/CLOSE](#711-OPENCLOSE)

	7.12. [Main()](#712-Main())

8. [Objects?](#8-Objects)

9. [Citing](#9-Citing)

10. [Contributing](#10-Contributing)

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

Booleans are a binary data type meaning they have 1 of two possible values (true or false). Booleans should be use upper case.

```
// Good
TRUE
FALSE

// Bad
true
false
True
False
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

An example of an `IF` statement which displays the text `FIZZBUZZ` when a number is a multiple of 3 and a multiple of 5 would be

```
x = READ "Enter a number: "  // Read a number from user input

IF x % 3 == 0 AND x % 5 == 0 THEN
    DISPLAY "FIZZBUZZ"
ENDIF
```

Here if `x` equalled 15 then `FIZZBUZZ` will be displayed but if 3 or 5 were inputted then nothing will be displayed.

### 7.5. ELSEIF

The `ELSEIF` builtin is appended to an `IF` in order to preform further operations if the condition of the above if fails (is false). `ELSEIF` has a similar syntax to the `IF` statement. `ELSEIF` statements can be used as many times as required.

```
IF condition THEN
    // Code here is ran if condition evaluates to true.
ELSEIF another_condition THEN
    // Code here is ran if the condition evaluates to false but
    // another_condition evaluates to true
ENDIF
```

An example of a `ELSEIF` which displays the text `BUZZ` if a number is a multiple of 5 or `FIZZ` if the number is a multiple of 3 would be

```
x = READ "Enter a number: "  // Read a number from user input

IF x % 3 == 0 AND x % 5 == 0 THEN
    DISPLAY "FIZZBUZZ"
ELSEIF x % 3 == 0 THEN
    DISPLAY "FIZZ"
ELSEIF x % 5 == 0 THEN
    DISPLAY "BUZZ"
ENDIF
```

Here if 3 is inputted, `FIZZ` will be displayed, if 5 is inputted then `BUZZ` will be displayed and if 15 is inputted then `FIZZBUZZ` is displayed.

### 7.6. ELSE

The `ELSE` builtin is used to run code when ever the above `IF` or `ELSEIF` statements fail.

```
IF condition THEN
    // Code here is ran if condition evaluates to true.
ELSEIF another_condition THEN
    // Code here is ran if the condition evaluates to false but
    // another_condition evaluates to true
ELSE
    // Code there is ran both condition and another_condition evaluate
    // to false above
ENDIF
```

Continuing on the previous examples, if the inputted number is not a multiple of 5 or a multiple of 3 then display the number

```
x = READ "Enter a number: "  // Read a number from user input

IF x % 3 == 0 AND x % 5 == 0 THEN
    DISPLAY "FIZZBUZZ"
ELSEIF x % 3 == 0 THEN
    DISPLAY "FIZZ"
ELSEIF x % 5 == 0 THEN
    DISPLAY "BUZZ"
ELSE
    DISPLAY x
ENDIF
```

So if 3 is inputted, `FIZZ` will be displayed, if 5 is inputted then `BUZZ` will be displayed and if 15 is inputted then `FIZZBUZZ` is displayed but if 7 is inputted then `7` is outputted.

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
