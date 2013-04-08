**Style Guidelines**
====================

###1.Basic Formatting

####1.Indentation Levels

**two schools of thought:**

_Use tabs for indentation_

_Use spaces for indentation_

>I recommend using four spaces per indentation level. 

####2.Statement Termination

>1. the rules of ASI are complex and difficult to remember, which is why I recommend using semicolons. 

>2. Both JSLint and JSHint will warn by default when semicolons are missing.

####3.Line Length

>Code convention documents for many languages prescribe that lines of code should be no longer than 80 characters. 

####4.Line Breaking

**Break after operator, following line indented two levels**

>1. comma is an operator and so should come last on the preceding line.
2. the control condition of the if statement is split onto a second line after the && operator. 
3. When assigning a value to a variable, the wrapped line should appear immediately under the first part of the assignment. 

####5.Blank Lines

>1. Between methods 2. Between the local variables in a method and its first statement 3. Before a multiline or single-line comment 4. Between logical sections inside a method to improve readability

####6.Naming

>JavaScript’s core, ECMAScript, is written using a conven- tion called camel case. Camel-case names begin with a lowercase letter and each sub- sequent word begins with an uppercase letter.

####7.Variables and Functions

>Variable names are always camel case and should begin with a noun. Beginning with a noun helps to differentiate variables from functions, which should begin with a verb.

For function and method names, the first word should always be a verb, and there are some common conventions used for that verb:
>1. can: Function returns a boolean 
 2. has: Function returns a boolean 3. is: Function returns a boolean
 4. get: Function returns a nonboolean 
 5. set: Function is used to save a value

