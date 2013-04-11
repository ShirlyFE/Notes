Comments
========

JavaScript supports two different types of comments: single-line and multiline.

##1.Single-Line Comments

There are three ways in which a single-line comment is used:

>* On its own line, explaining the line following the comment. The line should always be preceded by an empty line. The comment should be at the same indentation level as the following line.>* As a trailing comment at the end of a line of code. There should be at least one indent level between the code and the comment. The comment should not go beyond the maximum line length. If it does, then move the comment above the line of code.>* To comment out large portions of code (many editors automatically comment out multiple lines).
##2.Multiline Comments
__Don't use multiline comments for trailing comments__
##3.Using Comments
>the general rule is to add comments where they clarify the code.
####3.1 Difficult-to-Understand Code
>The key is to bring some understanding of the code’s purpose to someone else. 
####3.2 Potential Author Errors
>Another good time to comment code is when the code appears to have an error.
####3.3 Browser-Specific Hacks
>JavaScript developers are often forced to use code that is inefficient, inelegant, or downright dirty to get older browsers to work correctly. 
##4.Documentation Comments
>a multiline comment with an extra asterisk at the beginning (/**) followed by a description, followed by one or more attributes indicated by the @ sign. 
>__All methods__  	Be sure to include a description of the method, expected arguments, and possible return values.
>__All constructors__  
	Comments should include the purpose of the custom type and expected argu- ments.>__All objects with documented methods__  
If an object has one or more methods with documentation comments, then it also must be documented for proper documentation generation.