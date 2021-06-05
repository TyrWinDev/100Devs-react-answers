# 100Devs-react-answers

1.What is React.js?

React is a javascript library used in web development to create a more interactive UI. It helps you create
components for items to be reused, and it also helps you render different states of elements and their changes
in real time without having to reload the page.

2.Why would you use React.js?

One would use React.js if they were working with a website that has A LOT going on. An example of this is 
Facebook. They have a ton of information on the feed page, with a lot being update constantly. They also have a 
lot of pages that use the same exact same elements. Because of this, React helps one create components to be able
to reuse them in another page. These components are only a few lines long, so it saves a one from rewriting the same
code in different pages. 
Also, a page that has constant updates would be a pain in the neck if the page had to reload with each update. React
makes it so the page could target in on specific areas that need to rerendered, and it avoids having to refresh
the page.

3.What are components?

Components are like sections that you create in React to be reused. Say for example you plan on using a header 
in multiple pages, creating a component of that header saves you a ton of coding in the future. Also, it lets you
add props to the component, so if you do want to make slight changes to the header from page to page, all that 
is need is a few lines to be tweaked.

4.What is JSX?

JSX(Javascript extension) is a React extension used to modify the DOM by using HTML style code.

5.What are props?

Props are arguments passed into React compononents; they are passed via HTML attributes. It allows the programmer
to make little changes to a component to not have to write out the entire code again for the small changes.

6.What is state?

State is used for components that can change which will cause it to rerender. For example, let's say we have a
user online. When he/she is online, we can add a dot on the side of their username. The dot can be green when online,
but itll turn red when they are offline. This is something that would require state. It can only be used within a 
class component.

7.What are the differences btw/ functional and class based components?

A functional component is just a regular Javascript function that accepts props as an argument and returns
a Reach element. A class component requires you to extend from React


8. Give an example of a functional and class based component:

An example of a functional component is:

import React from 'react';
import ReactDOM from 'react-dom';
import Demo from './App';
  
ReactDOM.render(
  <React.StrictMode>
    <Demo />
  </React.StrictMode>,
  document.getElementById('root')
);

An example of a class-based component is:

class Example extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      count: 0
    };
  }

  render() {
    return (
      <div>
        <p>You clicked {this.state.count} times</p>
        <button onClick={() => this.setState({ count: this.state.count + 1 })}>
          Click me
        </button>
      </div>
    );
  }
}


9.What are React Hooks?

React hooks were introduced to help make it easier to reuse state logic in your app. It allows you to use state without using a class component.


10.How does useState work?

useState is a hook function imported from react. useState is set up with array destructuring, with first value setting the current state and the second value returning a function that lets you update the state. It differs from this.setState in that it updates the state instead of merging it.



11.Give an example of useState:

import React, { useState } from 'react';

function Example() {
  // Declare a new state variable, which we'll call "count"
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}
