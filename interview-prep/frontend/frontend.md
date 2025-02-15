# 🏠 Frontend Interview Questions

<br><br>

## 🔐 JavaScript Closures

### What is a closure in JavaScript? Provide an example.

- A closure is a feature where an inner function has access to the outer (enclosing) function's variables.

- Retains access to its lexical scope, even when the function is executed outside that scope

- Commonly used to create private variables or to maintain state in asynchronous operations

```javascript
function outerFunction(outerVariable) {
    return function innerFunction(innerVariable) {
        console.log("Outer Variable: " + outerVariable);
        console.log("Inner Variable: " + innerVariable);
    }
}
const newFunction = outerFunction("outside");
newFunction("inside");
```

```javascript
function createCounter() {
    let count = 0;
    return function() {
        count++;
        return count;
    };
}
const counter = createCouter();
console.log(counter());     // outputs 1
console.log(counter());     // outputs 2
```

<br><br>

## 💬 Responsive Design

### How would you implement a design that needs to be responsive across various devices?

- Utilize CSS media queries to apply different styles based on device characteristics like width, height, or orientation

- Employ a fluid grid and use relative units (em, rem, %) instead of pixels to ensure elements scale proportionally


<br><br>

## 🗝️ JavaScript Promises

### Explain the difference between ```.then()``` and ```async/await``` in handling asynchronous operations in JavaScript

- ```.then()``` is used with promises for asynchronous operations, chaining multiple calls for sequential execution

- ```async/await``` makes asynchronous code look synchronous and is syntactic sugar over Promises, improving readability and error handling


<br><br>

## 🔁 React Component Lifecycle

### Describe the lifecycle of a React component and how you would use it to fetch data

- React components have several lifecycle methods:
    - constructor()
    - render()
    - componentDidMount()
    - shouldComponentUpdate()
    - componentDidUpdate()
    - componentWillUnmount()

- To fetch data, use ```componentDidMount()``` for class components or ```useEffect()``` hook in functional components to perform side effects, including data fetching after the initial render


<br><br>

## 🌐 Cross-Origin Resource Sharing (CORS)

### What is CORS and how do you handle it in web applications?

- CORS is a security feature that restricts web applications from making requests to a domain different from the once which served the web page

- To handle it, configure the server to include CORS headers like ```Access-Control-Allow-Origin``` in the response, specifying which domains are allowed to access the resources


<br><br>

## 🤸🏼‍♀️ Frontend Performance Optimization

### What strategies would you employ to optimize the performance of the web application?

- Optimization strategies include:
    - Minimizing and compressing assets (CSS, JavaScript, images)
    - Implementing lazy loading for images and components 
    - Using CDN for static assets
    - Optimizing CSS selectors
    - Leveraging browser caching


<br><br>

## 📄 Singe Page Application (SPA) SEO Challenges

### What are the SEO challenges with SPAs and how can they be addressed?

- SPAs often struggle with SEO as content is dynamically loaded, making it hard for search engine crawlers to index

- Solutions include:
    - Server-side rendering (SSR), using the History API to update URLs for different view
    - Leveraging pre-rendering services or static site generators


<br><br>

## 👂🏼 Event Delegation in JavaScript

### Explain event delegation and its advantages

- Event delegation is a technique where instead of adding an event listener to each similar child element, you add a single event listener to a parent element

- It leverages the event bubbling phase to catch events from child elements

- Advantages include:
    - Reduced memory usage (fewer event listeners)
    - Dynamically handling events from elements added after the initial page load


<br><br>

## 📦 CSS Box Model

### Describe the CSS box model and how CSS properties related to it affect layout

- The CSS box model consists of four areas: content, padding, border, and margin

- These layers affect the total size and spacing of an element on the page

- Understanding this model is crucial for precise layout control, as it determines how elements are sized and how they interact with each other in the document flow


<br><br>

## 💻 Web Accessibility (a11y)

### How do you ensure your web application is accessible?

- To ensure web accessibility:
    - Follow WCAG (Web Content Accessibility Guidelines) and use semantic HTML elements for structure
    - Use ARIA roles for enhanced semantics
    - Ensure keyboard navigability
    - Provide alt text for images
    - Ensure contrast ratios are sufficient for readability

- Testing with screen readers and using accessibility audit tools can help identify and address issues


<br><br>

## 🪝 React Hooks

### What are the various types of React hooks?

- ```useState``` → allows functional components to have state

- ```useEffect``` → enables performing side effects in functional components (data fetching, subscriptions)

- ```useContext``` → provides a way to pass data through the component tree without manually passing props

- ```useReducer``` → an alternative to **useState** for managing complex state logic

- ```useRef``` → creates a mutable object that persists for the lifetime of the component

- **Custom hooks** → allow you to create your own hooks to reuse stateful logic

<br>

### Compare the useState and useReducer hooks in React

- ```useState``` → suitable for simple state logic, providing a variable and function to update it

- ```useReducer``` → better for complex state logic that involves multiple sub-values or when the next state depends on the previous one, as it lets you manage local state of complex components with a reducer function

<br>

### Explain the difference between state and props

#### **STATE**
- **Definition** → State is a built-in React object that is used to store data or information about the component. It is mutable and can be updated over time, usually in response to user events or other changes.

- **Ownership** → State is managed **within the component** itself. It is local to the component and cannot be accessed or modified by other components directly.

- **Usage** → State is used for data that changes over time, such as form inputs, toggles, or dynamic content.

```javascript
import React, { useState } from 'react';

function Counter() {
    const [count, setCount] = useState(0);      // state initialization

    return (
        <div>
            <p>Count: {count}</p>
            <button onClick={() => setCount(count + 1)}>Increment</button>
        </div>
    );
}

// count is a piece of state that changes when the button is clicked
```

#### **PROPS**
- **Definition** → Props (short for "properties") are read-only data passed from a parent component to a child component. They are immutable and cannot be modified by the child component.

- **Ownership** → Props are owned by the **parent component** and passed down to child components. The child component can only use the props it receives.

- **Usage** → Props are used to pass data or configuration from a parent to a child component, such as text, styles, or event handlers.

```javascript
function Greeting(props) {
    return <h1>Hello, {props.name}!</h1>;
}

function App() {
    return <Greeting name="Cosmo" />;   // passing 'name' as a prop
}

// name is a prop passed from the App component to the Greeting component
```

#### **KEY DIFFERENCES**

| **Aspect** | **State** | **Props** |
| --- | --- | --- |
| **Mutability** | Mutable (can be changed within the component) | Immutable (cannot be changed by the child) |
| **Ownership** | Managed within the component | Passed from a parent component |
| **Purpose** | Used for dynamic, changing data | 	Used for passing data or configuration |
| **Example Use Case** | Form inputs, counters, toggles | Displaying static data, configuring behavior |
<hr>

#### When to use State vs Props
- Use **state** when the data needs to change over time or is specific to a single component.

- Use **props** when you need to pass data or behavior from a parent to a child component.

```javascript
function ParentComponent() {
    const [message, setMessage] = useState("Hello from Parent!");   // State

    return (
        <ChildComponent message={message} />    // Passing state as props
    );
}

function ChildComponent(props) {
    return <p>{props.message}</p>;    // Using props
}
```

In this example:
- ```message``` is **state** in the ```ParentComponent```

- ```message``` is passed as **props** to the ```ChildComponent```


<br><br>

## 🌴 Tree Shaking in Webpack

### What is tree shaking and how does it help front-end development?

- Tree shaking is a process used in modern build tools like Webpack to eliminate unused code from the final bundle

- It improves performance by reducing the size of the JavaScript files that browsers need to load, parse, and execute, leading to faster page load times


<br><br>

## ⏹️ CSS Flexbox vs Grid

### Compare CSS Flexbox and Grid. When would you use one over the other?

- **Flexbox** is a one-dimensional layout method ideal for arranging items in a single row or column, offering control over alignment and spacing

- **Grid** is a two-dimensional layout system, perfect for creating complex layouts and aligning content within rows and columns

- Use **Flexbox** for simpler, linear layouts and **Grid** for more complex, multi-dimensional layouts


<br><br>

## 🔃 Progressive Web Apps (PWAs)

### What makes a web application a PWA?

- PWAs are web applications that use modern web technologies to provide a fast, reliable, and engaging user experience

- Key features include the ability to work offline, receive push notifications, and access hardware features, which can improve engagement and performance on mobile devices


<br><br>

## 📈 Web Performance Metrics

### What key performance metrics would you consider critical for a web application?

- Critical web performance metrics include:
    - First Contentful Paint (FCP)
    - Largest Contentful Paint (LCP)
    - Time to Interactive (TTI)
    - Speed Index
    - Cumulative Layout Shift (CLS)
    - First Input Delay (FID)

- These metrics help understand the loading experience, interactivity, and visual stability of a page


<br><br>

## 🪪 Security in Front-End Applications

### How do you protect a front-end application from common security threats?

- To protect a front-end application:
    - Implement Content Security Policy (CSP)
    - Sanitize user input to prevent XSS attacks
    - Use HTTPS for secure communication
    - Store sensitive data securely
    - Keep dependencies up to date to avoid vulnerabilities


<br><br>

## 🖥️ Server-Side Rendering vs Client-Side Rendering

### Compare server-side rendering (SSR) and client-side rendering (CSR)

- **CSR** → renders pages directly in the browser using JavaScript, leading to faster subsequent page loads and a smoother user experience

- **SSR** → generates HTML on the server and sends it to the client, improving initial load times and SEO

- Use **CSR** for dynamic, app-like experiences and **SSR** for static sites or when SEO is a priority


<br><br>

## 🛠️ State Management in SPA

### How do you manage state in a single-page application (SPA)?

- In SPAs, state management can be handled with global state management libraries like Redux or Context API in React applications

- These tools help maintain consistency across the application, making it easier to share state across components and manage changes reactively


<br><br>

## 🧪 Front-End Testing Strategies

### What strategies and tools do you use for front-end testing?

- Effective front-end testing strategies include:
    - Unit testing with Jest
    - Integration testing with React Testing Library
    - End-to-end testing with Cypress or Selenium

- Each testing type targets different aspects of the application, from individual functions and components to integrated workflows and the full user experience


<br><br>

## 🦇 Implementing Dark Mode

### How would you implement a dark mode feature in a web application?

