# Inheritance and Super
## Inheritance
```extends``` keyword
```javascript
class Person{
    constructor(firstName, lastName){
        this.firstName = firstName;
        this.lastName = lastName;
    }
    sayHello(){
        return `Hello ${this.firstName} ${this.lastName}`;
    }
}
class Student extends Person{

}
```
Inheritance similar to Ruby

## Super

When Javascript looks for methods to call, it starts from the last child, then works its way up through all the parents (or each class it extends).

When you call super() inside the constructor() method of a child class, it will call the constructor() method in the parent class.

**Example**
```javascript
class Animal {
    constructor(name) {
        this.name = name;
    }

    tellMeAboutYourself() {
        console.log('My name is ' + this.name);
        console.log(this.whatDoesTheAnimalSay());
    }

}

class Dog extends Animal {
    whatDoesTheAnimalSay() {
        return 'I go woof';
    }

    tellMeAboutYourself() {
        super.tellMeAboutYourself();
        console.log('I am a good boy');
    }
}

class Cat extends Animal {
    whatDoesTheAnimalSay() {
        return 'I go meow';
    }
}

class Kitty extends Cat {
    whatDoesTheAnimalSay() {
        return 'I go meow meow meow';
    }
}


const myAnimal = new Dog('Mooney');
const anotherAnimal = new Cat('Barry');
const lastAnimal = new Kitty('Lindy');

myAnimal.tellMeAboutYourself();
anotherAnimal.tellMeAboutYourself();
lastAnimal.tellMeAboutYourself();
```