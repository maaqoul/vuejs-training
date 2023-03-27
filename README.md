
# Vue.js Training Plan

## Day 1: JavaScript Refresher and Vue.js Introduction

### Morning: JavaScript Refresher (3 hours)

1. **History of JavaScript** (30 minutes)
   - Creation and early years
   - Evolution of ECMAScript standards
   - Modern JavaScript (ES6+)

2. **JavaScript Fundamentals** (1 hour)
   - Variables, constants, and data types
   - Operators and control structures
   - Functions and scope

3. **Asynchronous JavaScript** (1 hour)
   - Callbacks
   - Promises
   - Async/await

4. **Working with DOM and Events** (30 minutes)
   - DOM manipulation
   - Event handling and propagation

### Afternoon: Introduction to Vue.js (3 hours)

1. **Introduction to Vue.js** (30 minutes)
   - History of Vue.js
   - Key concepts and benefits

2. **Creating a Vue Instance** (30 minutes)
   - Vue instance properties and methods
   - Reactive data and the virtual DOM

3. **Directives and Components** (1 hour)
   - Built-in directives
   - Creating custom components

4. **Handling Events and Binding Data** (1 hour)
   - Event handling with v-on
   - Two-way data binding with v-model

## Day 2: Intermediate Vue.js Concepts

### Morning: Vuex and Vue Router (3 hours)

1. **Introduction to Vuex** (1.5 hours)
   - What is Vuex?
   - Core concepts: state, getters, mutations, and actions
   - Setting up a Vuex store

2. **Introduction to Vue Router** (1.5 hours)
   - What is Vue Router?
   - Setting up routes and router-view
   - Navigation and route guards

### Afternoon: Advanced Vue.js Features (3 hours)

1. **Custom Directives** (1 hour)
   - Creating custom directives
   - Binding values and arguments

2. **Mixins and Composition API** (2 hours)
   - What are mixins?
   - Introduction to the Composition API
   - Refactoring components with the Composition API

## Day 3: Project Setup and Tailwind CSS

### Morning: Project Setup (2 hours)

1. **Project Setup and Requirements** (1 hour)
   - Project overview
   - Defining the project structure
   - Installing dependencies

2. **Tailwind CSS Introduction** (1 hour)
   - What is Tailwind CSS?
   - Setting up and configuring Tailwind CSS

### Afternoon: Building the Mini E-commerce App (4 hours)

1. **Creating Components and Routes** (2 hours)
   - Designing the components hierarchy
   - Setting up the routes for the app

2. **Styling with Tailwind CSS** (2 hours)
   - Applying utility classes
   - Customizing the design and layout

## Day 4: Developing the Mini E-commerce App

### Morning: Vuex and Backend Integration (3 hours)

1. **Setting Up the Vuex Store** (1.5 hours)
   - Creating the store
   - Defining state, getters, mutations, and actions

2. **Integrating the Backend API** (1.5 hours)
   - Fetching data from the API
   - Handling API errors

### Afternoon: Implementing Features (3 hours)

1. **Product Listing and Filtering** (1.5 hours)
   - Displaying products
   - Implementing filters and sorting

2. **Shopping Cart Functionality** (1.5 hours)
   - Adding products to the cart

   - Updating and removing items from the cart
   - Calculating the cart total

## Day 5: Finalizing the Mini E-commerce App

### Morning: User Authentication and Checkout (3 hours)

1. **User Authentication** (1.5 hours)
   - Implementing sign up and login functionality
   - Securing routes with route guards

2. **Checkout Process** (1.5 hours)
   - Creating a checkout form
   - Validating form input
   - Sending order data to the backend

### Afternoon: Testing and Deployment (3 hours)

1. **Testing the Application** (1.5 hours)
   - Unit testing with Jest
   - End-to-end testing with Cypress

2. **Deployment and Wrap-up** (1.5 hours)
   - Deploying the application
   - Reviewing key concepts and lessons learned
   - Final questions and next steps

# Day 1: JavaScript Refresher and Vue.js Introduction

## Morning: JavaScript Refresher (3 hours)

### 1. History of JavaScript (30 minutes)

JavaScript was created in 1995 by Brendan Eich, who was working at Netscape at the time. Originally named Mocha, it was soon renamed to LiveScript, and finally to JavaScript. The language has evolved over the years with the introduction of new ECMAScript standards. Today, we have modern JavaScript, which includes features from ES6 and later versions.

- **Practice**:
1. Who created JavaScript and in what year?
2. What is ECMAScript and what is its relation to JavaScript?


### 2. JavaScript Fundamentals (1 hour)

In this section, we'll cover the core concepts of JavaScript, including:

- **Variables and Constants**: You can declare variables with the `let` keyword and constants with the `const` keyword. Variables can be reassigned, whereas constants cannot.
	```javascript 
	let variableName = "John";
	const constantName = "Doe";
	 ```

- **Data Types**: JavaScript has several data types, such as strings, numbers, booleans, objects, and arrays.
	```javascript
	let string = "Hello, World!";
	let number = 42;
	let boolean = true;
	let object = { key: "value" };
	let array = [1, 2, 3]
	```

- **Operators and Control Structures**: We'll explore basic operators for arithmetic, comparison, and logical operations. Additionally, we'll discuss control structures like `if`, `else`, `for`, and `while`.
	```javascript 
	// If statement
	if (number > 10) {
	  console.log("Number is greater than 10");
	} else {
	  console.log("Number is not greater than 10");
	}

	// For loop
	for (let i = 0; i < array.length; i++) {
	  console.log(array[i]);
	}
	 ```

- **Functions and Scope**: Functions are used to group code into reusable pieces. They can be declared with the `function` keyword or as arrow functions. Scope refers to the visibility of variables, which can be either global or local.
	```javascript
	// Function declaration
	function greet(name) {
	  console.log("Hello, " + name);
	}

	// Arrow function
	const greet = (name) => {
	  console.log("Hello, " + name);
	};
	 ```
- **Practice**:
1. What is the difference between `let`, `const`, and `var`?
2. List the primitive data types in JavaScript.
3. How do you declare a function in JavaScript? Provide an example of a function declaration and an arrow function.
4. What are the different types of loops available in JavaScript? Provide an example of a `for` loop and a `forEach` loop.

### 3. Asynchronous JavaScript (1 hour)

Asynchronous JavaScript is crucial for handling tasks that take time to complete, like fetching data from an API. We'll go over the following concepts:

- **Callbacks**: Functions that are passed as arguments to other functions and are executed once the parent function has finished.
	```javascript
	function fetchData(callback) {
	  setTimeout(() => {
	    callback("Data fetched");
	  }, 1000);
	}

	fetchData((data) => {
	  console.log(data);
	});
	```

- **Promises**: Objects that represent the eventual completion or failure of an asynchronous operation. They make it easier to handle asynchronous code by allowing you
to chain `.then()` and `.catch()` methods for success and error handling.

	```javascript
	function fetchData() {
	  return new Promise((resolve, reject) => {
	    setTimeout(() => {
	      resolve("Data fetched");
	    }, 1000);
	  });
	}

	fetchData()
	  .then((data) => {
	    console.log(data);
	  })
	  .catch((error) => {
	    console.error(error);
	  });
	  ```


- **Async/await**: A more modern and readable way to work with asynchronous code, async/await allows you to write asynchronous code that looks like synchronous code. The `async` keyword is used before a function declaration, and the `await` keyword is used before calling a function that returns a promise.
	```javascript
	async function fetchData() {
	  return new Promise((resolve, reject) => {
	    setTimeout(() => {
	      resolve("Data fetched");
	    }, 1000);
	  });
	}

	async function getData() {
	  try {
	    const data = await fetchData();
	    console.log(data);
	  } catch (error) {
	    console.error(error);
	  }
	}

	getData();
	 ```
- **Practice**:
1. What is a callback function? Provide an example.
2. What is a promise and how do you create one in JavaScript? Provide an example.
3. Explain the concept of async/await and provide an example.

### 4. Working with DOM and Events (30 minutes)

The Document Object Model (DOM) is a tree-like representation of an HTML document. JavaScript can interact with the DOM to manipulate elements, attributes, and content. We'll discuss:

- **DOM Manipulation**: Techniques to access and modify DOM elements, such as `getElementById`, `querySelector`, and `innerHTML`.
	```javascript
	const element = document.getElementById("example");
	const elements = document.querySelectorAll(".example");
	element.innerHTML = "New content";
	 ```

- **Event Handling and Propagation**: Events are actions that occur in the browser, like a user clicking a button. We can use event listeners to respond to events and event propagation to control the flow of events through the DOM.
	```javascript
	const button = document.querySelector("button");

	button.addEventListener("click", (event) => {
	  console.log("Button clicked");
	  event.stopPropagation();
	});
	 ```
- **Practice**:
1. What is the Document Object Model (DOM)?
2. How do you select an element by its ID and class name in JavaScript?
3. Provide an example of adding an event listener to a button that logs a message when clicked.
4. What is event propagation? Explain event capturing and event bubbling.

## Afternoon: Introduction to Vue.js (3 hours)

### 1. Introduction to Vue.js (30 minutes)

Vue.js is a progressive JavaScript framework for building user interfaces. It was created by Evan You in 2014 and has since become a popular choice for developers. Key concepts and benefits of Vue.js include its reactive data binding, component-based architecture, and excellent performance.

-**Practice**:
1. Who created Vue.js and in what year?
2. What are some key concepts and benefits of using Vue.js?

### 2. Creating a Vue Instance (30 minutes)

A Vue instance is an object that manages the state and behavior of a portion of the DOM. We'll cover:

-**Vue Instance Properties and Methods**: Vue instances have properties like `$data`, `$el`, and `$options`, and methods like `$watch` and `$nextTick`.
	```javascript
	const app = new Vue({
	  el: "#app",
	  data: {
	    message: "Hello Vue!"
	  },
	  methods: {
	    showMessage() {
	      console.log(this.message);
	    }
	  }
	});
	```

- **Reactive data and the virtual DOM**:  When the underlying data changes. The virtual DOM is an in-memory representation of the actual DOM, which Vue.js uses to efficiently update the DOM by minimizing changes.
	```javascript
	<!DOCTYPE html>
	<html>
	<head>
	  <title>Vue Reactive Data Example</title>
	  <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
	</head>
	<body>
	  <div id="app">
	    <p>{{ message }}</p>
	    <button @click="changeMessage">Change Message</button>
	  </div>

	  <script>
	    new Vue({
	      el: '#app',
	      data: {
	        message: 'Hello, Vue!'
	      },
	      methods: {
	        changeMessage() {
	          this.message = 'Message updated!';
	        }
	      }
	    });
	  </script>
	</body>
	</html>
	```
-**Practice**:
1. What is a Vue instance?
2. How do you create a new Vue instance? Provide an example.
3. What are some important Vue instance properties and methods?

### 3. Directives and Components (1 hour)

Directives and components are the building blocks of a Vue.js application.

- **Built-in Directives**: Vue.js comes with several built-in directives, like `v-if`, `v-for`, `v-show`, `v-bind`, and `v-on`. These directives provide declarative ways to bind data to the DOM and handle user interactions.
	```javascript
	<!-- Conditional rendering -->
	<div v-if="isVisible">This element is visible.</div>

	<!-- Loop through an array -->
	<ul>
	  <li v-for="item in items" :key="item.id">{{ item.name }}</li>
	</ul>

	<!-- Bind attribute -->
	<img v-bind:src="imageSrc" alt="example">

	<!-- Listen to an event -->
	<button v-on:click="handleClick">Click me</button>
	 ```

- **Creating Custom Components**: Components are reusable, self-contained pieces of code that represent a part of the user interface. We'll learn how to create custom components and how to pass data and events between components using props and custom events.
```javascript
Vue.component("example-component", {
  props: ["title"],
  template: `<h1>{{ title }}</h1>`
});

<example-component title="Hello, Vue!"></example-component>
```
-**Practice**:
1. What is a Vue directive? Provide examples of built-in directives.
2. What is a Vue component? How do you create a custom Vue component?

### 4. Handling Events and Binding Data (1 hour)

Vue.js provides a simple and efficient way to handle events and bind data.

- **Event Handling with v-on**: The `v-on` directive allows you to attach event listeners to DOM elements. You can define event handlers as methods within your Vue instance or component and use the `v-on` directive to call these methods in response to events.
	```javascript
	new Vue({
	  el: "#app",
	  methods: {
	    handleClick() {
	      console.log("Button clicked");
	    }
	  }
	});

	<button v-on:click="handleClick">Click me</button>
	```

- **Two-way Data Binding with v-model**: The `v-model` directive provides two-way data binding between form input elements and your Vue instance or component data. This means that changes to the input elements automatically update the corresponding data properties, and vice versa.

	```javascript
	new Vue({
	  el: "#app",
	  data: {
	    inputText: ""
	  }
	});
	<input type="text" v-model="inputText">
	 ```
-**Practice**:
1. How do you handle events in Vue.js? Provide an example using the `v-on` directive.
2. What is two-way data binding in Vue.js? Provide an example using the `v-model` directive.

