#REACT BASICS

https://www.lynda.com/React-js-tutorials/What-you-should-know-before-watching-course/379264/413763-4.html

* React 0.13.2
* Use `createClass` not `createComponent`
* The `transferPropsTo` method has been deprecated
* Using `/**@jsx React.DOM**/` is not required

##What is React?
React is a JavaScript library that's used for building user interfaces. It's an open source project that started at Facebook and it's maintained by developers at Facebook and Instagram and also a huge community of contributors. React is intended to be the view or the user interface, the V in MVC. One of the benefits and goals of the React project is to make developing a large scale single page application or SPA, much easier.

Probably the most exciting feature of React though is the virtual DOM. Whenever a change happens the virtual DOM efficiently re-renders the DOM. We'll discuss the virtual DOM in more detail in the next video. Finally, JSX is a familiar XML syntax that we can use directly in our JavaScript. React code is easy to understand for developers, designers, and anyone with the knowledge of XML or HTML. All of this is why React is becoming more and more popular and why it's so fun to work with.

##Why is React So Fast?
* JS objects are faster than DOM objects
* The Reac virtual DOM is a JS object
* React never reads from the "real" DOM
* React only writes to the real DOM if needed
* React efficiently handles DOM updates


##React Developer Tools for Chrome

1. add "react-detector"
2. you can press command +  option + i or j then go to the "React" tab

##2. Getting Started

###React.js Syntax
*Under Exercise Files see 02_01 start and finish*

###Introducing JSX and Babel
 * Instead of using React.createElement we use React.createClass
 
 *See 02_02 start and finish*

##3. React Components

###Creating a React component
*see 03_02 start and finish

* Note all React render functions must be wrapped in some sort of container in order to render

```
 var MyComponent = React.createClass({
            render: function() {
                return <div>My React Component</div>;
            }
        });

        React.render( <div>
            <MyComponent />, document.getElementById('react-container'));
```

Within this script tag, I'm going to create a new React component. We're going to set MyComponent equal to React.createClass. We're going to pass in an object. And then we're going to make sure that this has a render method. Now our render function is going to return something. And in this case, it's going to return a div that just reads "My Component." Excellent.

So now that we've created this we want to render this to our page. So I will use React.render. And remember, our render function takes in two things: first, the name of the component, and then it will also take in where I want to mount this or where I want to place this in the DOM.

###Using properties
*see 03_03 start and finish

* We can make our components more dynamic by adding properties. Sending properties to a component is very similar to adding attributes to HTML. Check it out > ``text="Hello World"``

```
React.reder(<MyComponent text="Hello World" />);
```

* How to render the above?

```
var MyComponent = React.createClass({
    render: function() {
        <h1>{this.props.text}</h1>
    }
```

* Props give us a way to reuse components with different data. 

* The next thing that I want to demonstrate here, is this.props.children.