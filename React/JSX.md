# JSX
JSX is a syntax extension for JS
it's not valid JS and browsers can't read it - it has to be compiled first

JSX elements are treated like JS expressions

You can net JSX elements just like HTML

If a JSX expression takes up more than one line, then you must wrap the multi-line JSX expression in parentheses.

Only one outermost element: this will work:
```
const paragraphs = (
  <div id="i-am-the-outermost-element">
    <p>I am a paragraph.</p>
    <p>I, too, am a paragraph.</p>
  </div>
);
```

ReactDOM is the name of a JavaScript library. This library contains several React-specific methods, all of which deal with the DOM in some way or another.

ReactDOM() takes two arguments: first one is the JSX expression, or variable, to be evaluated. The second argument is the DOM element it should be appended to.

## The Virtual DOM
In React, for every DOM object, there is a corresponding "virtual DOM object." A virtual DOM object is a representation of a DOM object, like a lightweight copy.

A virtual DOM object has the same properties as a real DOM object, but it lacks the real thing's power to directly change what's on the screen.

When you render a JSX element, every single virtual DOM object gets updated.

This sounds incredibly inefficient, but the cost is insignificant because the virtual DOM can update so quickly.

Once the virtual DOM has updated, then React compares the virtual DOM with a virtual DOM snapshot that was taken right before the update.

By comparing the new virtual DOM with a pre-update version, React figures out exactly which virtual DOM objects have changed. This process is called "diffing."

Once React knows which virtual DOM objects have changed, then React updates those objects, and only those objects, on the real DOM. In our example from earlier, React would be smart enough to rebuild your one checked-off list-item, and leave the rest of your list alone.

## className instead of class
class is a reserved word in JS so can't be used in the same situation as class attribute in HTML

In JSX, you have to include the slash. If you write a self-closing tag in JSX and forget the slash, you will raise an error.

## curlies
```
<h1>{2 + 3}</h1>
```
Everything inside of the curly braces will be treated as regular JavaScript.

## Event Listeners
onClick for example onClick ={function}

## Conditions
You can't write if statements inside JSX, but ternary operator is used.

Recall how it works: you write x ? y : z, where x, y, and z are all JavaScript expressions. When your code is executed, x is evaluated as either "truthy" or "falsy." If x is truthy, then the entire ternary operator returns y. If x is falsy, then the entire ternary operator returns z.

example:
```
const headline = (
  <h1>
    { age >= drinkingAge ? 'Buy Drink' : 'Do Teen Stuff' }
  </h1>
);
```
## JSX Conditionals: &&
Some code will run or no code will run

## Keys
When you make a list in JSX, sometimes your list will need to include something called keys:
```
<ul>
  <li key="li-01">Example1</li>
  <li key="li-02">Example2</li>
  <li key="li-03">Example3</li>
</ul>
```

A key is a JSX attribute. The attribute's name is key. The attribute's value should be something unique, similar to an id attribute.

keys don't do anything that you can see! React uses them internally to keep track of lists. If you don't use keys when you're supposed to, React might accidentally scramble your list-items into the wrong order.

Not all lists need to have keys. A list needs keys if either of the following are true:

- The list-items have memory from one render to the next. For instance, when a to-do list renders, each item must "remember" whether it was checked off. The items shouldn't get amnesia when they render.

- A list's order might be shuffled. For instance, a list of search results might be shuffled from one render to the next.

If neither of these conditions are true, then you don't have to worry about keys. If you aren't sure then it never hurts to use them!

## No JSX - React Create element
When a JSX element is compiled, the compiler transforms the JSX element into the method that you see above: React.createElement(). Every JSX element is secretly a call to React.createElement().
