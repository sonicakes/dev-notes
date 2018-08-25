# Class

Use Class instead of function

We create an instance of an object like in Ruby

MDN says:
> An important difference between function declarations and class declarations is that function declarations are hoisted and class declarations are not. You first need to declare your class and then access it, otherwise code like the following will throw a ReferenceError:
```javascript
const p = new Rectangle(); // ReferenceError

class Rectangle {}
```

## Methods

```static``` keyword to create class methods

creating a Person class
```javascript
class Person {
  constructor(firstName, lastName, favoriteColor, favoriteNumber){
    this.firstName = firstName;
    this.lastName = lastName;
    this.favoriteColor = favoriteColor;
    this.favoriteNumber = favoriteNumber;
    this.family = [];
  }
  fullName(){
    return `${this.firstName} ${this.lastName}`
  }
  multiplyFavoriteNumber(num){
    return num * this.favoriteNumber;
  }
  addToFamily(obj){
    if(obj.constructor === Person && this.family.indexOf(obj) === -1){
      this.family.push(obj)
    }
    return this.family
  }
}
```