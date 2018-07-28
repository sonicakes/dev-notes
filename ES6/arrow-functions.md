# Arrow Functions
- do not have their own keyword ```this``` and ```arguments```
- not to be used as methods in objects due to the above

## Usage
You can rewrite 'normal' code with hipster style like this:
```javascript
//normal way
function tripleAndFilter(arr){
    return arr.map(function(value){
      return value * 3;
    }).filter(function(value){
      return value % 5 === 0;
    })
  }
//hipster, ES6 way
const tripleAndFilter = (arr) => arr.map(value => value * 3).filter(result => result % 5 === 0);
console.log(tripleAndFilter([5,10,15,20]));

```
## Refactoring Old-Style JS with Arrow Functions Syntax
Just like the example above, I practiced with rewriting "grandma's JavaScript" with new shiny ES6. It wasn't easy! This is my "HOW_TO"

The instructions (from Udemy course - Advanced Web Dev Bootcamp) went like this: 
 >Refactor the following code to use ES2015 arrow functions. 
```javascript
  function doubleOddNumbers(arr){
      return arr.filter(function(val){
          return val % 2 !== 0;
      }).map(function(val){
          return val *2;
      })
  }
```

*advice*: Refactor the code using small steps, like a Russian Doll
1. Start with a teeny one, that is nested the deepest
```javascript
 (function(val){
   return val *2;
 })
```
refactors in
```javascript
val => val * 2
```
now the code looks like this
```javascript
 function doubleOddNumbers(arr){
   return arr.filter(function(val){
       return val % 2 !== 0;
   }).map(val => val * 2)
 }
```
2. Then move to a level higher and refactor this bit
```javascript
 (function(val){
   return val % 2 !== 0;
 })
```
refactores in
```javacript
//num => num % 2 !==0
```
now the code looks like this
```javascript
 function doubleOddNumbers(arr){
   return arr.filter(num => num % 2 !==0)
   .map(val => val * 2)
 }
```
3. Finally, the top level function, which is basically all your nested code. You could try and start refactoring from the top level, but I tried and got confused in the process. It is better to start small!
```javascript
function doubleOddNumbers(arr){
    return arr.filter(num => num % 2 !==0)
    .map(val => val * 2)
  }
  ```
refactors in
```javascript
const doubleOddNumbers = (arr) => arr.filter(num => num % 2 !==0).map(val => val * 2);
//testing
console.log(doubleOddNumbers([1,2,3,4,5,6]));
```
Voila!