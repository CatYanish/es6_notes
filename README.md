# ES6 / ES 2015

## LET Declarations
Let is a new way to declare variables and have them scoped to the nearest code block (and not to the nearest function, as with the standard `var` declaration). 

Consider this:
```
function regularFunction(){
  if(true){
    var trueBlockVariable = "Hello";
  } else {
    var falseBlockVariable = "Goodbye!";
  }
  
  console.log(falseBlockVariable);
}
```

In the above code, the console log will produce `undefined` rather than the normal 'not defined' error. To test this, you can try console logging any other made up variable, such as 'cats' on the very next line after the 'falseBlockVariable' console log. 

The reason for this is because of the 'var' declaration and hoisting. Hoisting will lift the variable declations to the top of the function and set them to undefined. 

The answer of course, is a `let` declaration.

Consider this:
```
function regularFunction(){
  if(true){
    let trueBlockVariable = "Hello";
  } else {
    let falseBlockVariable = "Goodbye!";
  }
  
  console.log(falseBlockVariable);
}
```

This will produce an error of 'not defined'. This matches our expectation of what we would see in other programming languages. 

### Instructor Notes
* Make sure that students really understand scope,
* Make sure that the students understand the difference between 'undefined' and 'not defined',
* One of the considerations that need to be made is whether or not an error is actually better than undefined for the need of the application.

## CONST Declarations

Const declarations allow us to create variables that cannot change. Which on the surface seems like a bad idea, but it allows us to constrain and address 'magic numbers'. 

Consider this:
```
var 
