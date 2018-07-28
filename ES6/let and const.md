# LET and CONST
## ```const```:
 - can be mutated when creating arrays and objects
 - can not be changed with primitives (float,integer)
 - can not be re-declared, as in no same variable with same name
## ```let```
```let``` allows you to declare variables that are limited in scope to the block, statement, or expression on which it is used. (MDN reference: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let )
### ```let``` vs ```var```
```var``` will do hoisting, so it will jump on top of functional scope regardless where actual declaration occurs. (https://medium.freecodecamp.org/what-is-variable-hoisting-differentiating-between-var-let-and-const-in-es6-f1a70bb43d)
#### e.g.:
```javascript
function helloInstructor(){
    return elie;
    var elie = "ME";
}
helloInstructor(); 
//we get undefined but really should get ReferenceError
```
#### Use Cases for ```let```
Writing a function that prints out 1-5 with 1 second interval like this with ```var```:
```javascript
for(var=0; i<5; i++){
    setTimeout(function(){
        console.log(i);
    }, 1000);
}
```
will print 5, 5 times in console, which is not what you want. The way to get around it is to run another function inside with ```j``` variable.

With ```let``` however, it logs 0-4 as expected, on separate lines. ```let``` creates a new variable each time loop runs.

##### Explanation on StackOverflow: 
(https://stackoverflow.com/questions/31285911/why-let-and-var-bindings-behave-differently-using-settimeout-function)

>With var you have a function scope, and only one shared binding for all of your loop iterations - i.e. the i in every setTimeout callback means the same variable that finally is equal to 6 after the loop iteration ends.

>With let you have a block scope and when used in the for loop you get a new binding for each iteration - i.e. the i in every setTimeout callback means a different variable, each of which has a different value: the first one is 0, the next one is 1 etc.


