# Components
 React component is a small, reusable chunk of code that is responsible for one job, which often involves rendering HTML.

Here's another fact about components: every component must come from a component class.

A component class is like a factory that creates components. If you have a component class, then you can use that class to produce as many components as you want.

To make a component class, you use a base class from the React library: React.Component.

What is React.Component, and how do you use it to make a component class?

React.Component is a JavaScript class. To create your own component class, you must subclass React.Component. You can do this by using the syntax class YourComponentNameGoesHere extends React.Component {}.

import React from 'react'
import ReactDOM from 'react-dom'

They both import JS objects

React library is getting imported

import React from 'react' creates a JavaScript object. This object contains properties that are needed to make React work, such as React.createElement() and React.Component.

import ReactDOM from 'react-dom' creates another JavaScript object. This object contains methods that help React interact with the DOM, such as ReactDOM.render().

## Render method
A render method must contain a return statement. Usually, this return statement returns a JSX expression:
```
class ComponentFactory extends React.Component {
  render() {
    return <h1>Hello world</h1>;
  }
}
```

Of course, none of this explains the point of a render method. All you know so far is that its name is render, it needs a return statement for some reason, and you have to include it in the body of your component class declaration.

## Component instance

MyComponentClass is now a working component class! It's ready to follow its instructions and make some React components.

So, let's make a React component! It only takes one more line:

<MyComponentClass />
To make a React component, you write a JSX element. Instead of naming your JSX element something like h1 or div like you've done before, give it the same name as a component class. Voilà, there's your component instance!
