# Debugging

### Order of Execution
- To find the source of an error, it helps to know how scripts are processed.
    - The order in which statements are executed can be complex 
        - some tasks cannot complete until another statement or function has been run

- The JavaScript interpreter uses the concept of execution contexts.
    - There is one global execution context
        - plus, each function creates a new new execution context.   
            - they correspond to variable scope

#### EXECUTION CONTEXT
Every statement in a script lives in one of three
execution contexts:
- GLOBAL CONTEXT
    - Code that is in the script, but not in a function.
        - There is only one global context in any page.
- FUNCTION CONTEXT
    - Code that is being run within a function.
        - Each function has its own function context.
- EVAL CONTEXT (NOT SHOWN)
    - Text is executed like code in an internal function called ```eva l ()``` (which is not covered in this book). 

### VARIABLE SCOPE
The first two execution contexts correspond with the
notion of scope:
- GLOBAL SCOPE
    - If a variable is declared outside a function, it can be used anywhere because it has global scope.
        - If you do not use the var keyword when creating a variable, it is placed in global scope.
- FUNCTION-LEVEL SCOPE
    - When a variable is declared within a function, it can only be used within that function. 
        - This is because it has function-level scope. 

The JS Interpreter processes one line of code at a time.
- When a statement needs data from another function, it stacks/piles the new function on top of the current task

### Execution context + hoisting 
Each tie a script enters a new contect, there are two phases of activity
1. Prepare
- The new scope is created
- Variables, functions, and arguments are created
- The value of the this keyword is determined 

2. Execute
- Now it can assign values to variables
- Reference functions and run their code
- Execute statements 

### Understanding Scope
In the interpreter, each execution context has its own ```variables``` object.
- It holds the variables, functions, and parameters available within it.
    - Each execution context can also access its parent's ```variables``` object.
- _lexical scope_ - linked to the object they were defined within.

## Understanding Errors
If a JavaScript statement generates an error, then it throws an _exception_.
- At that point, the interpreter stops and looks for exception-handl ing code. 

### Error Objects
- Error objects can help you find where your mistakes are and browsers have tools to help you read them. 

When an Er ror object is created, it will contain the
following properties:

|PROPERTY | DESCRIPTION|
|---------|------------|
|name | Type of execution|
|message | Description|
|```file``` Number | Name of the JavaScript file|
|```line``` Number | Line number of error |

- Syntax error - caused by incorrect use of the rules of the language
    - often the result of a simple typo
- Reference error - caused by a variable that it not declared or out of scope
- Eval error - incorrect use of ```eval()``` function
    - evaluates text through the interpretor and runs it as code. Rare to see thus type of error as other browsers often throw other errors when they are supposed to throw and eval error
- URI error - incorrect use of uri functions
    - If these characters are not escaped in URls, they will
cause an error: 
        - / ? & I : ; 
- Type error - value is an unexpected data type
    - often caused by trying to use an object or method that does not exist
- Range error - number outside of range
    - calling a functions using numbers outside of its range
- Error - generic error object
    - the generic error object is the template/prototype from which all other errors are created
- NaN - Not an Error
    - __If you perform a mathematical operation using a value that is not a number, you end up with the value of NaN, not a type error.__ 

## Debugging Errors
There are two things you can do with errors:

1. DEBUG THE SCRIPT TO FIX ERRORS
    - If you come across an error while writing a script (or when someone reports a bug), you will need to debug the code, track down the source of the error, and fix it. 

2. HANDLE ERRORS GRACEFULLY
    - You can handle errors gracefully using ```try```, ```catch```, ```throw```, and ```finally``` statements.
        - sometimes, an error may occur in the script for a
reason beyond your control. 
        - In such cases, it is particularly important to write error-handling code. 

### Debugging Workflow
Debugging is about deduction: eliminating potential causes of an error. 

- Where is the problem?
- What exactly is the problem?

__stepping over a function__ - if the debugger comes across a function, it will move onto the next line after the function. 

__step into a function__ - see what is happening inside the function. 

#### Throwing errors
If you know something might cause a problem for your script, you can generate your own errors before the interpreter creates them. 

## DEBUGGING TIPS

#### ANOTHER BROWSER
Some problems are browser specific. Try the code in another browser to see which ones are causing a problem.
#### ADD NUMBERS
Write numbers to the console so you can see which the items
get logged. 
- It shows how far your code runs before errors stop it.
#### STRIP IT BACK
Remove parts of code, and strip it down to the minimum you need
- You can do this either by 
    - removing the code altogether
    - by just commenting it out using multi-line comments: /* Anything between these characters is a cofllllent */
#### EXPLAINING THE CODE
Programmers often report finding a solution to a problem while explaining the code to someone else. 
#### SEARCH 
- Stack Overflow is a Q+A site for programmers.
- Or use a traditional search engine such as Google, Bing, or
DuckDuckGo.
#### CODE PLAYGROUNDS
If you want to ask about problematic code on a forum, in
addition to pasting the code into a post, you could add it to a code playground site (such as JSBin.com, JSFiddle. com, or
Dabbl et. corn) and then post a link to it from the forum. 
#### VALIDATION TOOLS 
- Javascript
- Json
- JQuery
#### Common Errors:
Common errors in scripts:
- go back to basics
- missed/extera characters
- data type issues

[<==back](README.md)