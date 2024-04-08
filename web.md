# Web Module Questions

### Functional patterns

#### What is a callback function?
A callback function is a function that is passed as an argument to another
function that is expected to call back (execute) the argument at a given time.
This execution may be immediate as in a synchronous callback, or it might
happen at a later time as in an asynchronous callback.

#### What is ECMA script ? What is the difference between Javascript & ECMA script ?
Ecma International is an organization that creates standards for technologies.
ECMA-262 is a standard published by Ecma International. It contains the specification for a general purpose scripting language. This specification is called
ECMAScript. (A scripting language is a programming language designed specifically for acting on an existing entity or system.)
JavaScript is a general purpose scripting language that conforms to the ECMAScript specification.
By reading the ECMAScript specification, you learn how to create a scripting language.
By reading the JavaScript documentation, you learn how to use a scripting language.

#### What is the difference between `let` & `var` ?
Var can skip its scope, let can not. Var can be accessed before it is declared, let can not.

#### Write an example where using the `var` declaration instead of the `let` could create a hard to debug code.
```
for (var i = 0; i < 5; i++) {
  setTimeout(function() {
    console.log(i);
  }, 1000);
}
```
This code will output “5” five times, because var variables are function-scoped and are hoisted to the top of the containing function, which means the value of i is 5 when the anonymous function inside the setTimeout is executed, after the for loop is done.
Instead, this problem can be fixed by using let and constraining the scope of i to the loop block. This would produce the desired outcome, outputing 0-4 each after 1 sec. Using let allows to access the i inside each iteration of the loop and output the correct value.

#### Give a practical example where you would use the `reduce` function in javascript.
Calculate the sum of numbers in an array.
```
const sum = [1, 2, 3, 4].reduce((acc, curr) => acc + curr)
```

#### Give a practical example where you would use the `map` function in javascript.
Return the array of the product names.
```
const products = [
  { id: 1, name: 'product 1', price: 10 },
  { id: 2, name: 'product 2', price: 5 },
  { id: 3, name: 'product 3', price: 15 }
];
const productNames = products.map(product => product.name);
console.log(productNames); // Output: ['product 1', 'product 2', 'product 3']
```

#### Give a practical example where you would use the `filter` function in javascript.
Filter the users who are over 18.
```
const users = [
  {name: "Sam", age: 5},
  {name: "Miranda", age: 19},
  {name: "Kim", age: 35}
]
const usersOver18 = users.filter(user => user.age >=18)
```

### Web basics

#### What is a web server?
A web server is a computer program that is responsible for accepting HTTP requests from clients, such as web browsers, and serving back HTTP responses, such as HTML pages and data.
When a user types a URL into their web browser or clicks on a hyperlink, the browser sends an HTTP request to the server specified by the URL. The server then responds with the requested information, typically in the form of an HTML page, which is then rendered by the browser for the user to view.

#### Explain the client-server architecture.
A Client is either a person or an organization using as a service. In the IT context, the client is a computer/device, also called a Host, that actually uses the service or accepts the information. Client devices include laptops, workstations, IoT devices, and similar network-friendly devices.
A Server in the IT world is a remote computer that provides access to data and services. Servers are usually physical devices such as rack servers, though the rise of cloud computing has brought virtual servers into the equation. The server handles processes like e-mail, application hosting, Internet connections,
printing, and more.
In a client-server architecture, one or more client devices connect to a central server over a network. The clients send requests for data or services to the server, which then processes the requests and sends back the necessary data or the results of the requested service. The client and server can be separate devices or different processes running on the same device. The main advantage of this architecture is that it allows for centralized control and management of data and services, while also allowing for scalable and distributed computing.

#### What is the difference between synchronous and asynchronous execution?
Synchronous execution refers to a mode of operation in which a process or function cannot move on to the next task until the current task is completed.
For example, in a synchronous system, a function call will block, or wait, until it receives a response or a result before continuing to execute. This means that a synchronous process will only move forward if the previous task is done.
On the other hand, asynchronous execution refers to a mode of operation in which a process or function can move on to the next task before the current task is completed. In an asynchronous system, a function call will not block, it
will return immediately with a promise and continue to execute. Therefore, an asynchronous process can do multiple task in parallel, and the execution of the next task doesn’t depend on the current task, so tasks can be executed in any order.

#### What is `npm`? Why is it useful?
npm stands for Node Package Manager, it is a package manager for the JavaScript programming language. And npm is also the world’s largest Software Library. npm is free to use.
npm is installed with Node.js. This means that you have to install Node.js to get npm installed on your computer. npm consists of a command line client, also called npm, and an online database of public and paid-for private packages, called the npm registry. The registry is accessed via the client, and the available packages can be browsed and searched via the npm website. Npm has automated dependency and package management.
All npm packages are defined in files called package.json. npm can manage dependencies. npm can (in one command line) install all the dependencies of a project (with npm install).
npm is useful because it allows developers to:
  • easily share and reuse code
  • manage dependencies in their projects
  • easily update and manage version of the packages
  • discover new packages and learn about their functionality through the npm registry
  • automate repetitive tasks with the command-line interface.

#### What is the difference between the `dependencies` & `devDependencies` in a `package.json` file ?
In a package.json file, the dependencies and devDependencies fields are used to specify the packages that your project depends on. The main difference between the two is when the dependencies are needed.

dependencies: are packages that are required for your application to run in production. These are the packages that your application needs to function correctly when it is deployed to an environment outside of a development environment. Examples: frameworks: React, AngularJS, Vue.js and Express.

devDependencies: on the other hand, are packages that are only needed during the development of the application, they are not needed in production. These are packages that are used for development and testing purposes. Examples: Nodemon; testing libraries: e. g. Jest; linters: e.g. ESLint and Prettier; transpilers:
e.g. webpack and Babel (since production-ready code is already transpiled and minified)
When you run npm install, npm will install all of the packages listed in both dependencies and devDependencies. But when you run npm install --production, npm will only install the packages listed in dependencies.
To save a dependency as a devDependency on installation we need to do an npm install --save-dev, instead of just an npm install --save.

#### What would be the impact of javascript `fetch` if it was not asyncronous ?
The fetch() method in JavaScript is used to retrieve resources from a server, and it’s asynchronous by default, this means that it will not block the execution of the rest of the code while it is waiting for the response from the server.
If fetch() was not asynchronous, it would block the execution of the rest of the code until it receives a response from the server. This means that your application would be frozen until the fetch request completes.

#### Why benefits would bring to a developer to use the `Postman` application ?
API or Application Programming Interface is defined as a set of rules or protocols which help various software components to interact with each other. Postman is a simple application used for testing APIs. It provides a user-friendly interface for making various types of HTTP requests (such as GET, POST, PUT, DELETE, etc.) to an API, and it also allows developers to view and inspect the responses from the API. Developers can create workspaces in Postman, which can contain collections, where you can store requests in folders and run them sequentially.
Using Postman can bring many benefits to a developer:
  • Easy to use interface: Postman provides a simple, intuitive interface that makes it easy for developers to create and test API requests.
  • Testing and debugging: Postman allows developers to test and debug their APIs by making various types of requests and inspecting the responses. It makes it easy to identify errors and fix them quickly.
  • Documenting APIs: Postman allows developers to document and share their APIs, by providing a way to create collections of requests and write notes on the documentation.
  • Automating tests: Postman allows developers to automate their tests by creating collections of requests and running them in a specific order, also can be integrated with other tools, like Jenkins.
  • Saving and sharing requests: Postman allows developers to save requests and responses and share them with other team members. This can be very useful for collaboration and working on large projects.
  • Request history: Postman keep the history of requests, which can be useful for debugging, testing and also for keeping track of the changes made on the API.

#### List the parts of the URL.
Scheme specifies the protocol (http, ftp...). Authority, the hostnam(www.example.com) or IP address with an optional port (192.168.1.1:8080). Path specifies the exact location, starting with a /. There is query (? key-value pair) and fragment(#) as well.

#### What is query parameter?
Comes after the question mark ("?"). The query parameters are used to pass data or parameters to a server or a web page.
https://example.com/search?q=JavaScript+query+parameter
A query parameter is a part of a URL that is used to pass additional information or data to the server as part of an HTTP request. The query parameters are added to the end of a URL, following the path, and they are separated by the “?” character. The query parameters are a key-value pair, where the key and value are separated by the “=” character. Multiple query parameters are separated by the “&” character.

#### What kind of HTTP status codes do you know?
100–199: These status codes indicate that the server has received the request and is processing it.
Successful responses 200–299: 200: ok, 204: ok but no-content
Redirection messages 300–399.
Client error responses (400–499): 404 Not Found: The requested resource could not be found on the server. 
Server error responses (500–599): 500 Internal Server Error: An unexpected error occurred on the server while processing the request.

#### How does an HTTP Request look like? What are the most relevant HTTP header fields?
Request line: The first line of an HTTP request, which includes the request method, the requested URL, and the HTTP protocol version.
Headers: Provides additional information about the request, such as the Host(domain), the user agent, the content type, and the length of the content.
Body: If there is any, sent with the request, such as form data or JSON payload.

#### How does an HTTP Response look like? What are the most relevant HTTP header fields?
Status line: The first line of an HTTP response, which includes the HTTP protocol version, the status code, and the reason phrase.
Headers: Optional metadata that provides additional information about the response, such as the server software, the content type, and the length of the content.
Body: Optional data that is sent with the response, such as HTML, JSON, or image data.

#### Why should you ignore the `node_modules` folder in `.gitignore` ?
The node_modules folder should be ignored in .gitignore because it contains all the packages and dependencies that are installed for a Node.js project using the npm package manager. These dependencies are usually listed in the
package.json file, and the exact versions of the dependencies can be installed on another machine using the npm install command. This means that it is not necessary to include the node_modules folder in the repository, as it can be easily regenerated.

### Rest API: Serve and Fetch

#### Why is it recommend for a developer to use the http methods `get`, `put`, `delete` ?
Because those are the HTTP request methods for reading (GET), updating (PUT or PATCH), and deleting (DELETE) data on a server.

#### How does a `POST` request look like when it is made from a web browser (on the front end written) ?
A POST request made from a web browser on the front end is typically done using JavaScript or a JavaScript library such as jQuery. The request is usually made using the XMLHttpRequest or fetch API, or by using a library function
such as $.ajax() in jQuery.
Here is an example of a POST request using the fetch API:
```
fetch('/api/endpoint', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({ key: 'value' })
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error(error));
  ```
This example is making a POST request to the /api/endpoint URL, with a JSON object containing key-value pairs as the request body. The Content-Type header is set to application/json, which indicates that the request body is in
JSON format. The response from the server is parsed as JSON and logged to the console.

#### What is an API?
An API, or Application Programming Interface, is a set of rules and protocols that allows different software systems to communicate with each other. An API defines how software components should interact, and allows for the creation of mutually beneficial relationships between those components.
APIs can be used to allow different software systems to share data or functionality. For example, a web application might use an API to retrieve data from a database, or to send data to another system for further processing. A mobile app might use an API to access services provided by a cloud-based service.

#### What is REST API?
RESTful APIs use HTTP methods (GET, POST, PUT, DELETE, etc.) to perform operations on resources, which are identified by URIs (Uniform Resource Identifiers). A resource can represent any entity, such as a user, a product, or a file.

#### What is JSON and how do we use it?
JSON data is represented as a collection of key-value pairs, where the keys are strings and the values can be any valid JSON data type, including strings, numbers, booleans, arrays, and objects. We use it as an Object.

#### What is API versioning ?
API versioning is the practice of managing changes to an API and ensuring that these changes are made without disrupting clients. A good API versioning strategy clearly communicates the changes made and allows API consumers to
decide when to upgrade to the latest version at their own pace.
At its core, an API is a piece of software. And like all software, APIs need to update every once in a while.
When a third-party application developer uses your API to build an integration, they expect that the API will be stable. If you make changes to your API without considering clients, it forces them to change their own software. Otherwise, their applications could break if updates aren’t accounted for.
This is why API versioning is about more than simply changing the version number of an API. It’s about avoiding major updates whenever possible and, when these updates do occur, clearly communicating them to customers in announcements via the website, email, and documentation.

#### Give 3 examples of HTTP response status codes ? Explain what each number means.
1. 200 OK - The request succeeded. The result meaning of “success” depends
on the HTTP method:
  • GET: The resource has been fetched and transmitted in the message body.
  • PUT or POST: The resource describing the result of the action is transmitted in the message body.
2. 404 Not Found - The server cannot find the requested resource. In the browser, this means the URL is not recognized. In an API, this can also mean that the endpoint is valid but the resource itself does not exist.
3. 500 Internal Server Error - The server has encountered a situation it does not know how to handle.

### Advanced JavaScript

#### How does the `ternary operator` looks like in javascript?
if the condition is true ? do something : otherwise do something else
The ternary operator is a shorthand way of writing an if-else statement in JavaScript. It’s a way to assign a value based on a condition.

#### How to import a function from another module in JavaScript?
In JavaScript, you can import functions and other values from another module using the import statement. The basic syntax for importing a function from another module is:
  import { functionName } from 'moduleName';
It is important to export the function in the file where you created it, because you can only import it if it was exported.

#### What is a shallow copy on an object?
let objshallow = {...object}
In JavaScript, a shallow copy of an object is a new object that contains all of the original object's properties and values, but the values are references to the same objects in memory as the original object.
When we modify a property of the shallowCopy object, that's value is a primitive type, it does not affect the originalObject.
However, when we modify the nested nestedProp property of the shallowCopy object, it modifies the same property of the originalObject because the value is an object reference.

#### What is a callback function? Tell some examples of its usage.
Passed as an argument to another function and is intended to be called later on within the other function's code. Callback functions are commonly used to handle asynchronous operations, such as retrieving data from a server, where the result is not immediately available. In fetch after then, or in addeventlistener.

#### What is object destructuring in javascript?
Object destructuring is a feature of JavaScript that allows you to extract properties from an object and assign them to variables. It’s a convenient way of extracting data from an object and creating variables with the same name as the properties.
The general syntax for object destructuring is:
  let { variable1, variable2, variable3 } = object;
For example, let’s say you have an object like this:
 ```
  let person = {
    name: "John",
    age: 30,
    address: {
      street: "1 Main St",
      city: "Boston",
    state: "MA"
    }
  };
```
You can extract the properties from the object and assign them to variables like this:
```
  let { name, age } = person;
  console.log(name); // "John"
  console.log(age); // 30
```
You can also use destructuring to extract properties from nested objects:
```
  let { address: { city } } = person;
  console.log(city); // "Boston"
```

You can also assign new variable names while destructuring:
```
  let { name: firstName } = person;
  console.log(firstName); // "John"
```

Object destructuring is useful when you have an object with many properties and you only need a few of them, it can make your code more readable and less verbose. It’s also commonly used in React when extracting properties from
component props.
It’s important to note that, if you try to extract a property from an object that doesn’t exist, JavaScript will throw an error. To prevent this, you can use the default value for the property, like this:
  ```
  let { nickname = 'unknown' } = person;
  console.log(nickname); // "unknown"
  ```

You can also use destructuring in function parameter, it makes it more readable and less verbose to extract the properties from the passed object.
  ```
  function printUser({name, age}) {
    console.log(`Name: ${name}, Age: ${age}`);
  }
  printUser(person);
    // Output: Name: John, Age: 30
```

As you can see, by destructuring the object in the function parameter, you don’t have to access the properties of the object using the dot notation or the bracket notation, which makes the code more readable and easier to understand.
In summary, object destructuring is a powerful feature in JavaScript that allows you to extract properties from an object and assign them to variables, making it more convenient and readable to work with objects. It’s commonly used
in React when extracting properties from component props and also useful in function parameter as well.

#### What is array destructuring in javascript?
Array destructuring is similar to object destructuring, but it allows you to extract elements from an array and assign them to variables.
The general syntax for array destructuring is:
  ```
  let [variable1, variable2, variable3] = array;
  ```

For example, let’s say you have an array like this:
  ```
  let numbers = [1, 2, 3, 4, 5];
  ```

You can extract the elements from the array and assign them to variables like this:
  ```
  let [first, second, third] = numbers;
  console.log(first); // 1
  console.log(second); // 2
  console.log(third); // 3
  ```

You can also use the rest operator … to extract the remaining elements of the array:
  ```
  let [first, second, ...rest] = numbers;
  console.log(rest); // [3, 4, 5]
  ```
Array destructuring is useful when you have an array with many elements and you only need a few of them, it can make your code more readable and less verbose. It’s also commonly used when working with returned values from
functions.
It’s important to note that, if you try to extract an element from an array that doesn’t exist, JavaScript will assign the value undefined to the variable. To prevent this, you can use the default value for the element, like this:
```
  let [first = 0, second = 0, third = 0] = numbers;
```
In summary, array destructuring is a powerful feature in JavaScript that allows you to extract elements from an array and assign them to variables, making it more convenient and readable to work with arrays. It’s commonly used when working with returned values from functions and also useful in function parameter as well.

#### What is the spread operator in `js` ?
iterates through, object, array, string, expands them into individual elements. Create a shallow copy.

#### What are the differences between the `arrow` function and the regular `function`?
syntax: function name(a) {return a + 1}, const name = a => a+1

#### What is the `import` keyword used for?
The static import declaration is used to import read-only live bindings which are exported by another module. The imported bindings are called live bindings because they are updated by the module that exported the binding, but cannot be re-assigned by the importing module.
In order to use the import declaration in a source file, the file must be interpreted by the runtime as a module. In HTML, this is done by adding type=“module” to the tag. Modules are automatically interpreted in strict mode.

#### What is the `required` used for?
Import function, component and so forth from the origin
React uses import.

#### What are template literals?
Template literals are literals delimited with backtick (‘) characters, allowing for multi-line strings, string interpolation with embedded expressions, and special constructs called tagged templates.
Template literals are sometimes informally called template strings, because they are used most commonly for string interpolation (to create strings by doing substitution of placeholders). However, a tagged template literal may not result in a string; it can be used with a custom tag function to perform whatever operations you want on the different parts of the template literal. Template Literals use back-ticks (‘) rather than the quotes ("") to define a string:
```
let text =`Welcome ${firstName}, ${lastName}`;
```

### Testing basics

#### What is code coverage? Why is it used?
#### What is a test case? What is an assertion? Give examples!
#### What are the unit testing best practices? (Eg. how many assertion should a test case contain?)
#### What is arrange/act/assert pattern?
#### How do you test asynchronous code with `jest` ?
#### What is `setup` & `teardown` in jest ?
#### Give an example when you would use in `jest` the `toBe` & `toEqual` assertions.

### React basics

#### What benefits does it bring for a developer to use `components` (opposed of writing all the code in a single file) ?
  • Easier to understand them
  • Components are easily reusable and modifiable
  • Multiple people can work on different components at the same time

#### What is the difference between Element and Component?
React elements are the building blocks of React applications. An element describes what you want to see on the screen. React elements are immutable.
  ```
  const element = <h1>Hello, world</h1>;
  ```
React components are functions or classes that return a React element to be rendered to the page.
  ```
  function Welcome(props) {
    return <h1>Hello, {props.name}</h1>;
  }
  ```

#### How do you pass values between components in `react`?
Props are inputs to a React component. They are data passed down from a parent component to a child component. They get collected into a properties object (props) which then is passed to the component function as the first argument.
Props are readonly.

#### What is `key` prop?
A key prop is needed when creating elements from an array. The key prop should be unique for each element (preferably not the index). It helps React keep track of elements in DOM, should the order change, for example.

#### How does a child component pass data to it's parent component ?
1. Define an event handler function in the parent component and pass it to the child component as a property. The event handler function is called in the child component and accept an argument which is data from the child component.
2. Define a state in the parent component and pass it to the child component as a property. When the state gets set in the child component, it also gets set in the parent component. This is called state lifting.

#### Write the code to create in JSX an HTML DIV element that has the innerText the contents of the variable `let name = 'Andrew'`
  ```
  let name = 'Andrew';
  const myDiv = <div>{name}</div>
  ```
This creates a JSX element representing a DIV element and the {} notation is used to indicate that the value inside it should be treated as JSX and not just a string. It will then display Andrew as the inner text of the div.

#### Write the code to create in JSX an unordered list from the array `let names = ["Mathew", "John", "Maverik"]`
  ```
  let names = ["Mathew", "John", "Maverik"];
  const nameList = (
    <ul>
      {names.map((name,index) => (
        <li key={index}>{name}</li>
      ))}
    </ul>
  );
  ```

#### Write the code to set the background color red of a div in JSX.
```
  const myDiv = <div style={{ backgroundColor: "red" }}>My Div</div>
```
In JSX, the style attribute is used to set the CSS styles for an element. The value of the style attribute is an object, and each property of the object corresponds to a CSS property. It’s important to note that in JSX, CSS property names are written in camelCase (e.g. backgroundColor, textDecoration) instead of kebabcase (e.g. background-color, text-decoration) as in regular CSS.
Additionally, you could also use the className attribute to set the background color of the div by defining a class in a stylesheet and then applying it on the div.
  ```
  .red-bg {
    background-color: red;
  }
const myDiv = <div className="red-bg">My Div</div>
  ```

### Testing react

#### What are unit tests, integration tests? What is the major difference between these two?
#### What is unit testing?
#### What does `mocking` mean from a testing perspective ? Give an example when you would use it.
#### How do you test that function was called `at least` 2 times using `jest` ?
#### Name 4 benefits a developer gets from writing tests.

### React patterns

#### What is the difference between Real DOM and Virtual DOM?
Real DOM Whenever a user requests a webpage, the browser receives an HTML document for that page from the server. The browser then constructs a logical, tree-like structure from the HTML to show the user the requested page
in the client.
This tree-like structure is called the Document Object Model, also known as the DOM. It is a structural representation of the web document as nodes and objects.

Virtual DOM In React, for every DOM object, there is a corresponding “virtual DOM object.” A virtual DOM object is a representation of a DOM object, like a lightweight copy.
React first creates a Virtual DOM tree, where it keeps track of all info, for example which components does each element belong to. Then it will use this virtual tree to create the actual, real DOM tree that gets displayed in the
browser, keeping only the info necessary for displaying the tree.
When you render a JSX element, the whole Virtual DOM object gets updated. Then React compares the virtual DOM with a virtual DOM snapshot that was taken right before the update, determines what element was changed, and updates only that element on the real DOM. This is one method the virtual DOM employs to optimize performance

#### When adding an item to an array, why is it necessary to pass a new array to the `useState` hook ?
States in react should be considered immutable. Mutating the state will change it, however if the reference stays the same, it won’t trigger a rerender. You have to completele replace the array with a new one.

#### Describe what techniques or tools you use to debug a react app.
  • console.log()
  • The browsers debugger

#### What is the difference between a react `class` component & a `functional` component ?
Class has a render method, function returns an element.
Class has states. 

#### Name 3 lifecycle states in a react `functional` component.
  • Mounting - element gets added to the DOM
  • Updating - element changes
  • Unmounting - element gets removed from the DOM

#### What is conditional rendering in `react` ? Give an example.
You can use conditional rendering to add an element to the DOM tree only if a certain condition is met.
  ```
  return (
    <div>
      {somethingThatsTrueOrFalse && <p>Rendered!</p>}
    </div>
  )
  ```
The code above will render the paragraph if the left side of the && is true, and won’t if it’s false. However, this method won’t work with truthy/falsey values, in that case it will simply render both the value and the paragraph.

#### Write the code that prints to the console `component destroyed` when the component it is part of is removed from the DOM tree.
```
  import { useEffect } from 'react';

  function MyComponent() {
    useEffect(() => {
      return () => console.log("component destroyed");
    }, []);
  return <div>My Component</div>;
  }
```

#### Why is there an infinite loop in this code
```
function App() {
  const [count, setCount] = useState(0); //initial value of this 
  useEffect(() => {
    setCount((count) => count + 1); //increment this Hook
  }); //no dependency array.
  return (
    <div className="App">
      <p> value of count: {count} </p>
    </div>
  );
}
```
Cause there is no dependency.

In this code, there is an infinite loop caused by the useEffect hook. When the component is first rendered, the count state variable is set to 0. The useEffect hook is then called, and inside it, the setCount function is called to increment the count variable. However, because there is no dependency array provided to the useEffect hook, it will run on every render of the component, including re-renders caused by the setCount function inside the effect.
This creates an infinite loop, where the component is continuously re-rendering, and the count state variable is continuously being incremented. The displayed value of the count on the screen doesn’t change and the component can not finish its lifecycle.
To fix this issue, it is necessary to pass a dependency array to useEffect that includes the value of count, so that it only runs when the count value changes.

#### Why is there an infinite loop in this code
```
  async function App() {
  const [count, setCount] = useState("");
  setCount(count + 1);
  return (
    <div className="App">
      <p> value of count: {count} </p>
    </div>
  );
}
```
Cause setCount is called without any action, which means the component will rerender each and every time when it renders...

The useState hook is called to set the initial value of count state variable to an empty string, and then, right after that, the function setCount(count + 1) is being invoked which causes the component to re-render, updating the value of the count state variable.
However, because count state variable is updated during render phase and component is re-rendered, the component will re-execute setCount(count + 1) and then again component re-renders and so on. This creates an infinite loop, where the component is continuously re-rendering, and the count state variable is continuously being incremented. The component can not finish its lifecycle.
To fix this issue, you should move setCount(count + 1); inside an useEffect hook that only runs once and also you need to pass the dependencies.

### Mongo & mongoose

#### What is a database schema ?
Mongoose is a Node.js-based library for MongoDB. It provides an API for connecting to MongoDB and using its services.
By default, MongoDB does not require the documents in a collection to have the same fields and data types. Mongoose allows us to define schemas our data fit into. This way we can ensure that all saved documents has the same structure and contain required properties.
A schema is an object with key-value pairs. The keys correspond to the indentically named fields in the document. The values contain the data type (e.g. String, Number, Boolean…) and other optional properties, like required, or
a default value. If we define other parameters besides the data type, we use nested objects in the values.
Example for a schema:
```
const BlogSchema = new Schema({
title: {type: String, required: true }, // required means title must be entered
author: String, // String is shorthand for {type: String}
body: String,
comments: [{ body: String, date: Date }],
date: { type: Date, default: Date.now },
});
```
In contrast to schema, a model is a tool for interacting with MongoDB. It is created from the schema. The model provides an interface to the database for this collection - so that we can create, query, update and delete documents.
We use the mongoose.model() function to create a model from a schema.
// Syntax: mongoose.model(<Collectionname>, <CollectionSchema>)
```
mongoose.model("Post", BlogSchema)
```

#### Why is the `id` unique in a database ?
(I suppose they meant the _id.) Because then the documents can be identified by a property which is unique to them. When you create a new document, Mongoose automatically adds a unique _id property to your document.

#### What are the advatanges & disadvatages of using `lean()` function in a mongo query ?
Mongoose documents represent a one-to-one mapping to documents as stored in MongoDB. Each document is an instance of its Model. By default, Mongoose queries return an instance of the Mongoose Document class. Documents are
much heavier than vanilla JavaScript objects, because they have a lot of internal state for change tracking.
The lean() function tells Mongoose to skip instantiating a full Mongoose document and just give you a plain JavaScript object.
```
const docs = await Model.find().lean();
```
Advantages: JS objects are smaller than a Mongoose document and faster to work with.
Disadvantages: JS objects are not connected with the MongoDB anymore, so cannot be used to manipulate the DB.

#### Write the code to store the object `{name: "Andrew", age: 10}` to a mongo database. You can ignore the part of connection parameters.
```
async function main() {
  // method 1
  const dbUser = new User({name: "Andrew", age: 10});
  dbUser.save();
  // method 2
  await User.create({name: "Andrew", age: 10});
};
main();
```

#### Write the code to delete from a mongo database all employees that are over 18 years. The scheme for an employee is `{name: string, age: int}`. You can ignore the part of connection parameters.
```
async function main() {
  await Employee.deleteMany({ age: { $gt: 18 } });
};
main();
```

#### Write the code to display in the console from a mongo database the employees who are over 18 years. The scheme for an employee is `{name: string, age: int}`. You can ignore the part of connection parameters.
```
async function main() {
  console.log( await Employee.find({ age: { $gt: 18 } }));
};
main();
```

#### Write the code to update from a mongo database the employees with name='John' and set the new age to 8. The scheme for an employee is `{name: string, age: int}`. You can ignore the part of connection parameters.
In MongoDB, updateMany() method updates all matched documents within the collection based on the given query. When you update your documents the value of the _id field remains unchanged. This method can also add new fields in the given documents. It takes three parameters, the first one is the selection criteria to update the documents, the second one is the new data to be updated, and the third one is optional.
```
async function main() {
  await Employee.updateMany({name: John}, {age: 8});
};
main();
```

### Authentication (cookies + google)

#### How to properly store passwords?
#### What is encryption and decryption?
#### What is hashing?
#### What is OAuth2?
#### What is the difference between encryption and hashing? When would you use which?
#### How/where would you store sensitive data (like db password, API key, ...) of your application?
#### What would you use a session for?
#### What would you use a cookie for?

### Mern stack

#### What does `MERN` stand for in the context of web development ?
  • MongoDB - document database
  • Express - web server framework
  • React - frontend JS framework
  • Node - JS web server

#### What is routing in the context of a `react` app ?
react routing is a client side routing, meaning it can display different pages based on the URL without sending request to the server

#### What is routing in the context of an `express` app ?
Routing in express means that a server will run different operations based on the request’s URL and method, which result in different responses

#### What is `CORS` policy ?
Cross-Origin Resource Sharing is a policy which decides whether the browser can access resources form a server that’s different form the website origin, or not.

#### What advantages does a developer have for using `bootstrap` or `material ui` ?
Bootstrap is a free and open-source CSS framework directed at responsive, mobile-first front-end web development. It contains HTML, CSS and JavaScript-based design templates.
Material UI is an open-source React component library. It includes a collection of prebuilt components that are ready for use in production.
bootstrap and material ui provide user-friendly, nice looking UI elements which can applied easily, allowing the developer to spend less time on design while they’re working on the rest of the application.
