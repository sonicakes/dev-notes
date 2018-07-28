# Arrow Functions
- do not have their own keyword ```this``` and ```arguments```
- not to be used as methods in objects due to the above

### Usage
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