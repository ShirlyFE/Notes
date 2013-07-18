Statements and Expressions
==========================

>Statements such as __if__ and __for__ can be used in two ways in JavaScript, with curly braces for multiple contained lines or without curly braces for one contained line. 

	// Good	if (condition) {		doSomething(); 	}

>An overwhelming majority of JavaScript developers are in agreement that block state- ments should always use braces and always occupy multiple lines instead of one. This is because of the confusion created when braces aren’t included. 

Braces should be used for all block statements, including:
>* **if*** **for*** **while*** **do...while*** **try...catch...finally**
##1.Brace Alignment
There are two main styles of brace alignment. 
The first is to have the opening brace on the same line as the beginning of the block statement, as in this example:
	if (condition) { 		doSomething();	} else {		doSomethingElse();	}

The second style of brace alignment places the opening brace on the line following the beginning of the block statement, as in this example:
	if (condition) 	{		doSomething(); 	}	else 	{		doSomethingElse(); 	}	
__Google JavaScript Style Guide explicitly forbids it due to fears of automatic semicolon insertion errors.__
##2.Block Statement Spacing
>There are three primary styles for block statement spacing. 
	
	//1	if(condition){ 		doSomething();	}
	//2
	if (condition) { 
		doSomething();	}		//3
	if ( condition ) { 
		doSomething();	}	
>I prefer the second style as a nice compromise between the first and third styles.
>__This is the style recommended by Crockford’s Code Conventions and the Google JavaScript Style Guide.__	
##3.The switch Statement####3.1 Indentation

	//1	switch(condition) { 		case "first":			// code 			break;
		case "second": 			// code 			break;		case "third": 			// code			break;		default:			// code	}


>* Each case statement is indented one level from the switch keyword.* There is an extra line before and after each case statement from the second one on.__it is the format that many editors use automatically.__
	switch(condition) { 	case "first":		// code		break; 	case "second": 		// code 		break;	case "third": 		// code		break; 	default:		// code 	}

**As with other aspects of coding style, this choice is completely a matter of preference.**####3.2 Falling Through>Accidentally omitting a break at the end of a case is a very common source of bugs, so Douglas Crockford argues that every case should end with **break**, **return**, or **throw**, without exception. __JSLint warns when one case falls through into another__.
>My recommen- dation is to allow fall-throughs as long as a comment is used to indicate that the fall- through is intentional.
PS.code example in page 33.

####3.3 default

My preference is to omit default when there is no default action and annotate it using a comment, as in this example:	switch(condition) { 		case "first":			// code 			break;
		case "second": 			// code 			break;				// no default 	}
	

##3.The with Statement

>__The with statement is actually disallowed in strict mode__, causing a syntax error and indicating the ECMAScript committee’s belief that with should no longer be used.


##4.The for Loop


	