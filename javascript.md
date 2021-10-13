# Style guid for javascript

## Variable declaration

1. ### Don't use var for variable declaration
this has some disadvantages:
- if it used in global scope it will create a global object property
- A repeated var declaration of the same identifier name in a scope is effectively a do-nothing operation for non-strict mode code.
- But a repeated var decalation of the same identifier name in a non-strict mode code can override the value if it contains an assignment.
- In strict mode, a repeated var declaration of the same identifier name in a scope is a SyntaxError.
- If it appears with a repeated name with function declaration any where of the code, it's do-nothing operation. (function hoisting has more )
- in loops var variables won't create a block scope and tends to bug.

2. ### Alway initialize const variables, and don't reassign them. this will throw error
- const variables can't be reassigned.
- const variables can't be redeclared.
- const variables can't be deleted.
- const variables need to be initialized.

3. ### Always declare variables and functions before usage.
- Variables and functions declared at the top of the scope are accessible throughout the scope.
- hoisting can be lead to confusion.
- hoisting for let and const variables is not supported. it will throw error because of TDZ.

4. ### Don't use eval
eval is a powerful function that can be used to execute arbitrary code.
It can cost you performance and security. since it can modify the scope of the code.

5. ### Don't use implied eval
Beside the eval itself there are a few other ways to pass string and have interpreted as it is code. 

Using setTimeout and setInterval can accept a string as a parameter and run it as it is code.

6. ### Don't change the object shape 
- Changing the object shape of an object can lead to poor performance and memory usage.
- Always initialize object with the shape of it will eventually will end up with the same shape.
