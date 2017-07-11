# Javascript Code Style Guide

 * [Spacing](#spacing)
  * [Objects and Array Expressions](#objects-and-array-expressions)
  * [Multi-line Statements](#multi-line-statements)
  * [Chained Method Calls](#chained-method-calls)
  * [Full File Closures](#full-file-closures)
  * [Constructors](#constructors)
 * [Equality](#equality)
 * [Type Checks](#type-checks)
 * [Comments](#comments)
 * [Quotes](#quotes)
 * [Semicolons](#semicolons)
 * [Naming Conventions](#naming-conventions)
 * [Global Variables](#global-variables)
 * [Switch Statements](#switch-statements)

## Spacing

- Indent using tabs.
- No whitespace at the end of line or on blank lines.
- Lines should be no longer than 80 characters, and must not exceed 100 (counting tabs as 4 spaces). There are 2 exceptions, both allowing the line to exceed 100 characters:
	- If the line contains a comment with a long URL.
	- If the line contains a regex literal. This prevents having to use the regex constructor which requires otherwise unnecessary string escaping.
- `if`/`else`/`for`/`while` do not need to have braces if it's scope content is on one line.
- `try` always have braces and go on multiple lines.
- The `?` and `:` in a ternary conditional must have space on both sides.
- New line at the end of each file.
- If the entire file is wrapped in a closure, the function body is not indented.

### Objects and Array Expressions

Object and array expressions can be on one line if they are short (remember the line length limits). When an expression is too long to fit on one line, there must be one property or element per line. Property names only need to be quoted if they are reserved words or contain special characters.

### Multi-line Statements

When a statement is too long to fit on one line, line breaks must occur after an operator.
When a conditional is too long to fit on one line, successive lines must be indented one extra level to distinguish them from the body.

### Chained Method Calls

When a chain of method calls is too long to fit on one line, there must be one call per line, with the first call on a separate line from the object the methods are called on. If the method changes the context, an extra level of indentation must be used.

### Full File Closures

When a entire file is wrapped in a closure / AMD wrapper, the body of the closure is not indented.

### Constructors

Constructor functions should always be invoked with argument lists, even when such lists are empty.

## Equality

Strict equality checks (`===`) must be used in favor of abstract equality checks (`==`).
The only exception is when checking for `undefined` and `null` by way of `null`.

## Type Checks

- String ```typeof object === 'string'```
- Number ```typeof object === 'number'```
- Boolean ```typeof object === 'boolean'```
- Object ```typeof object === 'object'```
- Plain Object ```$.isPlainObject(object)```
- Function ```typeof object === 'function'```
- Array ```$.isArray(object)```
- null ```object === null```
- null or undefined ```object == null```
- undefined
	- Global variables ```typeof object === 'undefined'```
	- Local variables ```object === undefined```
	- Properties ```object.prop === undefined```

## Comments

Comments start with a capital first letter and don't require a period at the end.
There must be a single space between the comment token and the comment text.

Single line comments go over the line they refer to.

## Quotes

- The Plug-It team uses single quotes.
- Strings that require inner quoting must use single outside and double inside.

## Semicolons

- Always use semicolons.

## Naming Conventions

Variable and function names should be full words, using camel case with a lowercase first letter.
Names should be descriptive but not excessively so.
Exceptions are allowed for iterators, such as the use of `i` to represent the index in a loop.

## Global Variables

Each project may expose at most one global variable.

## Switch Statements

Only use `switch` statements if there are a large number of cases or when fall-through would give an advantage.

When using `switch` statements:
 - Use a `break` or `return` for each case other than `default`.
 - Indent `case` statements from the `switch` statement.

