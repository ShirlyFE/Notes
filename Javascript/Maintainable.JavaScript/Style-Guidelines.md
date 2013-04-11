**Style Guidelines**
====================

##1.Basic Formatting

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

>* Between methods* Between the local variables in a method and its first statement* Before a multiline or single-line comment* Between logical sections inside a method to improve readability

####6.Naming

>JavaScript’s core, ECMAScript, is written using a conven- tion called camel case. Camel-case names begin with a lowercase letter and each sub- sequent word begins with an uppercase letter.

#####6.1 Variables and Functions

>Variable names are always camel case and should begin with a noun. Beginning with a noun helps to differentiate variables from functions, which should begin with a verb.

For function and method names, the first word should always be a verb, and there are some common conventions used for that verb:
>* can: Function returns a boolean 
* has: Function returns a boolean* is: Function returns a boolean
* get: Function returns a nonboolean 
* set: Function is used to save a value

#####6.2 Constants

The convention comes from C and uses all uppercase letters with underscores sepa- rating words.

Consider the following example:
	if (count < MAX_COUNT) { 		doSomething();	}
	In this code, it’s easy to tell that count is a variable that may change and MAX_COUNT is a variable that is intended to never change. 
#####6.3 Constructors
Constructors are formatted using Pascal case.
Pascal case is the same as camel case except that the initial letter is uppercase. 
>JSLint will warn if a constructor is found without an initial uppercase letter or if a constructor function is used without the new operator. JSHint will warn if a constructor is found without an initial uppercase letter only if you add the special newcap option.####7.Literal Values
>JavaScript has several types of primitive literal values: strings, numbers, booleans, null, and undefined. There are also object literals and array literals.

#####7.1 Strings

>in the string using double quotes, we had to escape the double quote characters, and in the string using single quotes, we did not. What matters is that you pick a single style and stick with it throughout the code base.
>I prefer using double quotes, because I tend to switch back and forth between writing Java and JavaScript frequently. Because Java uses only dou- ble quotes for strings, I find it easier to switch between contexts by maintaining that convention in JavaScript. 

multiline strings, split the string into multiple strings and concatenate them together:
	// Good	var longString = "Here's the story, of a man " +					  "named Brady.";
#####7.2 Numbers
>1. It’s a good idea to always include digits before and after the decimal point to avoid any confusion.
>2. the best approach is to disallow octal literals in code. Although not called out in any of the popular style guides, both JSLint and JSHint will warn when they come across an octal literal. 
#####7.3 Null
The special value null is often misunderstood and confused with undefined. This value should be used in just a few cases:>* To initialize a variable that may later be assigned an object value* To compare against an initialized variable that may or may not have an object value* To pass into a function where an object is expected* To return from a function where an object is expected
There are also some cases in which null should not be used:>* Do not use null to test whether an argument was supplied.* Do not test an uninitialized variable for the value null.
#####7.4 Undefined
>By avoiding the use of the special value undefined, you effectively keep the meaning of typeof returning “ __undefined__ ” to a single case: when a variable hasn’t been declared. If you’re using a variable that may or may not be assigned an object value later on, initialize it to __null__.
>__The typeof operator returns “object” for a null value, so it can be differentiated from undefined.__
#####7.5 Object Literals
	// Good	var book = {		title: "Maintainable JavaScript",		author: "Nicholas C. Zakas" 
	};#####7.6 Array Literals
	// Good	var colors = [ "red", "green", "blue" ]; 	var numbers = [ 1, 2, 3, 4 ];					  