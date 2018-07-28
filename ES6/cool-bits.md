# Cool Bits
## Default parameters
Specify what you want returned instead of 'undefined', if you do not pass any arguments in a function.
```javascript
function multiply(a, b = 1) {
  return a * b;
}
multiply(5, 2); // 10
multiply(5, 1); // 5
multiply(5);    // 5
```
## For...of loop
arrays (Symbol.iterator in proto)
```javascript
var arr = [1,2,3,4,5];
for(let val of arr){
    console.log(val);
}
//1
//2
//3
//4
//5
```
## Rest
... is Rest Operator
It lets you turn your parameters into an array, so you can .reduce(), .sort() etc skipping the step of turning arguments into array first.
```javascript
function sortRestArgs(...theArgs) {
  var sortedArgs = theArgs.sort();
  return sortedArgs;
}

console.log(sortRestArgs(5, 3, 7, 1)); // 1, 3, 5, 7

function sortArguments() {
  var sortedArgs = arguments.sort(); 
  return sortedArgs; // this will never happen
}


console.log(sortArguments(5, 3, 7, 1)); // TypeError (arguments.sort is not a function)
```
## Spread
Useful when passing array into new constructor,or using elements of aray as arguments for a function.
### Examples
 Spread instead of apply
```javascript
var arr = [3,4,5,3,1];
//es5
Math.max.apply(this, arr);//5
//es6
Math.max(...arr);//5
```
```javascript
var dateFields = [1970, 0, 1];  // 1 Jan 1970
var d = new Date(...dateFields);
```

