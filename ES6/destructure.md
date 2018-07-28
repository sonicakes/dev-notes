# Destructuring

So...what the heck is destructuring and why do I need it? I don't know. Hopefully soon I'll get to use it and then pains of understanding it will pay off. :persevere:

Start with exercise I did to se an example of this monster.

 
>Write a function called displayStudentInfo which accepts an object and returns the string "Your full name is"
 concatenated with the value of the first key and a space and then the value of the last key. 
 See if you can destructure this object inside of the function.

```javascript
function displayStudentInfo(obj){
    // var firstName = obj.first;
    // var lastName = obj.last;
var {first, last} = obj;
    return `Your full name is ${first} ${last}`;
}
console.log(displayStudentInfo({first: 'Elie', last:'Schoppik'}));
```
ok so..I can surely just do it with obj.first/last? -No. React uses ES6, React is Hot, I need to learn ES6!!!

*NB*: make sure to use same name for variables you create in curlies, so that they match whatver arguments are passed into your function (I tried firstName and lastName, as you can see in comments, and that will give you ```undefined```).

So, what the :fish: is destructuring itself? Looks like structuring to me. As if you were making your code shorter, more succinct..But I suppose that's language problem, I interpret the word destructuring differently.

MDN says:
> The destructuring assignment syntax is a JavaScript expression that makes it possible to unpack values from arrays, or properties from objects, into distinct variables.

Completely understandable.

Another exercise then!
