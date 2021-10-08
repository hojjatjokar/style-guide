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
