# SIT105 Pseudocode Style Guide

> **Please note that this document is only a guide and there is zero guarantee that Nick will actually accept this style guide (but it's better then nothing). This not a conclusive guide. USE AT OWN RISK.**

This document defines a set of styling guidelines which should be used in order to make pseudocode more consistent and readable. Inspiration for the following rules has been taken from the SIT105 lectures, Nick's Cloud practical, the Python Enhancement Proposal 8 and the Rust Style Guide.

This is not designed to teach pseudocode but rather define some best practices in terms of presentation of pseudocode for SIT105 assessment 3.

## Comments

Comments are marked by a `//` at the start of the line. Inline comments should be defined 2 spaces after the line of code.

### Example

```
// This is a comment

x = 1  // This is an inline comment.
```

## Operators

Spaces should be present around all operators.

### Example

```
// Good
a == a
a != b

// Bad
a==a
a!=b
```

## Comma separated values

Spaces should be after the comma in all comma separated values.

### Example

```
// Good
[a, b, c]
Module(a, b, c)

// Bad
[a,b,c]
Module(a,b,c)
```

## Strings

String should be defined with either single or double quotations as long as the use of either single or double quotations is consistent throughout the code.

### Example

```
"This is a string"
'This is also a string'
```

## Booleans

Booleans should be capitalised.

### Example

```
True
False
```

## Variables

Variables are defined using the `=` operator and should use snake case.

### Example

```
x = 1
method_output = ModuleName()
```

## Builtins

Built in modules should be capitalised and do not use parenthesis to pass argument unlike user defined modules although parenthesis may be used in some situations where it evaluates to a boolean in order to improve visual grepping.

Builtins can also magically create variables (don't ask questions, it's somehow common).

Possible builtins include:

  - `DISPLAY`
  - `PRINT`
  - `WRITE`
  - `READ`
  - `IF`
  - `WHILE`
  - `RETURN`

### Example

```
DOWHILE (READ line IN file SUCCEEDS)
    DISPLAY line
ENDDO
```

## Modules

Modules should use capitalised word casing and be defined before use. A module definition ends when an `END` statement is reached.

Arguments can be passed to a in the parenthesis when defined and called, where empty parenthesis signals no arguments. A user defined module should always be followed by parenthesis when called and defined.

If module output is to be used it must be defined to a variable (see the variable examples for an example). User defined modules cannot magically create variables such as Builtins.

### Example

```
// Define the module Hello()
Hello(name, age)
    DISPLAY "Hello my name is " + name + "and I am aged" + age
END

Main()
  Hello("Hayden", 18)  // call the module Hello() with the parameters Hayden and 18
END
```

## Scope

Scope is defined using an `END` statements. `END` statements vary depending on what scope they define.

Scope is also signified through an indentation of multiples of 4 spaces to improve visual grepping.

Possible `END` statements include:

  - `END`
  - `ENDIF`
  - `ENDDO`
  - `ENDWHILE`
  - `ENDFOR`

### Example

```
WHILE True DO  // WHILE scope starts here
    // This code is in the scope of the WHILE loop
    PRINT "Hello World"
ENDWHILE  // WHILE scope ends here

x = 1  // This code is out of the scope of the WHILE loop
```

## Contributing

This style guide is a living document. If you wish to add or modify it at all then please feel free to make a pull request.
