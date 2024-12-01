## **What is JavaScript?**

JavaScript is a high-level, interpreted programming language primarily used to add interactivity, control multimedia, and dynamically update content on web pages. Unlike HTML and CSS, which structure and style a webpage, JavaScript enables dynamic functionalities such as animations, form validations, and API integration.

### Key Features:

- **Lightweight:** Designed to run in browsers without consuming much memory.
- **Interpreted:** Does not require compilation; executed directly in browsers.
- **Versatile:** Can be used for front-end (browser), back-end (Node.js), and even mobile development.
- **Object-Oriented:** Allows the use of objects for structuring data and behavior.

---

## **Install a JavaScript Source Code Editor**

A source code editor simplifies writing and debugging JavaScript code.

### Recommended Editors:

1. **Visual Studio Code (VS Code):**

   - Lightweight and fast.
   - Features intelligent code completion, debugging, and extensions.
   - Download: [https://code.visualstudio.com/](https://code.visualstudio.com/)

2. **Sublime Text:**

   - Known for speed and simplicity.
   - Offers features like syntax highlighting and multi-selection editing.
   - Download: [https://www.sublimetext.com/](https://www.sublimetext.com/)

3. **Atom:**
   - Open-source and customizable.
   - Perfect for collaborative projects.
   - Download: [https://atom.io/](https://atom.io/)

---

## **Use the Console Tab of Web Development Tools**

### What is the Console?

The **console** is part of a browser's developer tools, allowing developers to:

- Test and debug JavaScript code.
- Log outputs for troubleshooting.
- Interact with the DOM dynamically.

### How to Open the Console:

1. Open any modern browser (e.g., Chrome, Firefox).
2. Press `Ctrl + Shift + I` (Windows/Linux) or `Cmd + Option + I` (Mac) to open Developer Tools.
3. Navigate to the **Console** tab.

### Example:

Type the following in the console and press Enter:

```javascript
console.log("Hello, Console!");
```

The console will display:

```
Hello, Console!
```

---

## **Writing Your First JavaScript Code (External Script)**

### Why Use External Scripts?

- **Separation of Concerns:** Keeps HTML clean and modular.
- **Reusability:** The same script file can be used across multiple pages.
- **Easier Maintenance:** Modifications in the external file automatically apply to all linked pages.

### Example:

1. **HTML File (`index.html`):**

   ```html
   <!DOCTYPE html>
   <html lang="en">
     <head>
       <meta charset="UTF-8" />
       <meta name="viewport" content="width=device-width, initial-scale=1.0" />
       <title>JavaScript Demo</title>
     </head>
     <body>
       <h1>Welcome to JavaScript</h1>
       <p>Check the console for output.</p>
       <!-- Link to External JavaScript -->
       <script src="script.js"></script>
     </body>
   </html>
   ```

2. **JavaScript File (`script.js`):**

   ```javascript
   console.log("Hello, World!");
   ```

3. Open the `index.html` file in a browser and view the console to see:
   ```
   Hello, World!
   ```

---

## **Control Flow Statements**

Control flow statements allow you to manage the execution path of your code.

### **If-Else Statements**

Used to execute code based on conditions.

```javascript
let score = 80;

if (score >= 90) {
  console.log("Grade: A");
} else if (score >= 75) {
  console.log("Grade: B");
} else {
  console.log("Grade: C");
}
```

### **Switch Statements**

Ideal for multiple conditions.

```javascript
let day = "Monday";

switch (day) {
  case "Monday":
    console.log("Start of the week!");
    break;
  case "Friday":
    console.log("Almost weekend!");
    break;
  default:
    console.log("Midweek vibes!");
}
```

### **Ternary Operator**

A concise way to write conditional expressions.

```javascript
let age = 18;
let message = age >= 18 ? "You are an adult." : "You are a minor.";
console.log(message);
```

---

## **Loops**

Loops allow repetitive execution of code.

### **For Loop**

Executes a block of code a fixed number of times.

```javascript
for (let i = 0; i < 5; i++) {
  console.log(i); // Output: 0, 1, 2, 3, 4
}
```

### **While Loop**

Executes while the condition is true.

```javascript
let i = 0;
while (i < 5) {
  console.log(i);
  i++;
}
```

### **Do-While Loop**

Executes at least once before checking the condition.

```javascript
let i = 0;
do {
  console.log(i);
  i++;
} while (i < 5);
```

### **forEach Loop**

Iterates over each element in an array.

```javascript
const fruits = ["Apple", "Banana", "Cherry"];
fruits.forEach((fruit, index) => {
  console.log(`${index}: ${fruit}`);
});
// Output:
// 0: Apple
// 1: Banana
// 2: Cherry
```

### **for...in Loop**

Iterates over the keys of an object.

```javascript
const person = {
  name: "Alice",
  age: 25,
  job: "Engineer",
};
for (let key in person) {
  console.log(`${key}: ${person[key]}`);
}
// Output:
// name: Alice
// age: 25
// job: Engineer
```

### **Break and Continue**

- **Break:** Terminates the loop.
- **Continue:** Skips the current iteration.

```javascript
for (let i = 0; i < 10; i++) {
  if (i === 5) break;
  if (i % 2 === 0) continue;
  console.log(i); // Output: 1, 3
}
```

---

## **Functions**

Functions are reusable blocks of code.

### Function Declaration

```javascript
function greet(name) {
  return `Hello, ${name}!`;
}
console.log(greet("Alice")); // Output: Hello, Alice!
```

### Arrow Functions

A shorter syntax for functions.

```javascript
const add = (a, b) => a + b;
console.log(add(5, 3)); // Output: 8
```

### Default Parameters

Set default values for parameters.

```javascript
function greet(name = "Guest") {
  return `Hello, ${name}!`;
}
console.log(greet()); // Output: Hello, Guest!
```

### Recursive Function

A function that calls itself.

```javascript
function factorial(n) {
  return n === 1 ? 1 : n * factorial(n - 1);
}
console.log(factorial(5)); // Output: 120
```

---

## **Objects and Prototypes**

Objects are collections of key-value pairs.

### Example Object:

```javascript
const person = {
  name: "Alice",
  age: 25,
  greet() {
    console.log(`Hi, I'm ${this.name}`);
  },
};
person.greet(); // Output: Hi, I'm Alice
```

### Prototypes

Allow inheritance of methods.

```javascript
function Person(name, age) {
  this.name = name;
  this.age = age;
}
Person.prototype.sayHello = function () {
  console.log(`Hello, I'm ${this.name}`);
};
const john = new Person("John", 30);
john.sayHello(); // Output: Hello, I'm John
```

---

## **What is the DOM (Document Object Model)?**

The DOM is a programming interface for web documents. It represents the structure of an HTML or XML document as a tree-like structure where each node is an object representing a part of the document (e.g., elements, attributes, text).

### Why is the DOM Important?

- **Dynamic Interaction:** JavaScript uses the DOM to dynamically update, add, or remove elements and content.
- **Event Handling:** It enables interaction between users and web applications through event listeners.
- **Traversal and Manipulation:** Allows navigation through parent, child, and sibling nodes and manipulation of their content or attributes.

### Core DOM Concepts

1. **Text Node:** Represents the text content of an element or attribute.

   ```html
   <p>Hello, World!</p>
   ```

   The text "Hello, World!" is a text node.

2. **Element Node:** Represents an HTML or XML element.

   ```html
   <p>Hello, World!</p>
   ```

   The `<p>` tag is an element node.

3. **Child Node:** Any node that is a direct descendant of another node.

   ```html
   <div>
     <p>This is a child node.</p>
   </div>
   ```

4. **Parent Node:** The node that contains a child node.

   ```html
   <div>
     <!-- Parent node -->
     <p>Child node</p>
   </div>
   ```

5. **Descendant Node:** Any node nested within another node (not limited to direct children).
6. **Sibling Node:** Nodes that share the same parent.

---

## **DOM Manipulation and Examples**

### **Query/Get Elements**

Retrieve elements from the DOM using different methods.

- By **ID**:
  ```javascript
  let element = document.getElementById("title");
  console.log(element.textContent);
  ```
- By **Class Name**:
  ```javascript
  let elements = document.getElementsByClassName("items");
  console.log(elements[0]);
  ```
- By **Tag Name**:
  ```javascript
  let paragraphs = document.getElementsByTagName("p");
  console.log(paragraphs);
  ```
- By **CSS Selector**:
  ```javascript
  let button = document.querySelector(".btn");
  console.log(button);
  ```

---

### **Create and Clone Elements**

- **Create an Element**:

  ```javascript
  let newElement = document.createElement("div");
  newElement.textContent = "This is a new div!";
  document.body.appendChild(newElement);
  ```

- **Clone an Element**:
  ```javascript
  let clonedElement = newElement.cloneNode(true);
  document.body.appendChild(clonedElement);
  ```

---

### **Add Nodes to the Document**

- **Append Child**:

  ```javascript
  let parent = document.getElementById("container");
  let child = document.createElement("span");
  child.textContent = "I'm a child!";
  parent.appendChild(child);
  ```

- **Insert Before**:
  ```javascript
  let reference = document.getElementById("reference");
  parent.insertBefore(child, reference);
  ```

---

### **Modify Element Content and Attributes**

- **Text Content**:

  ```javascript
  let title = document.getElementById("title");
  title.textContent = "New Title";
  ```

- **HTML Content**:

  ```javascript
  let container = document.getElementById("container");
  container.innerHTML = "<p>New Content</p>";
  ```

- **Attributes**:
  ```javascript
  let link = document.querySelector("a");
  link.setAttribute("href", "https://example.com");
  console.log(link.getAttribute("href"));
  ```

---

### **Get and Modify Element Class**

- **Add Class**:

  ```javascript
  let element = document.getElementById("box");
  element.classList.add("highlight");
  ```

- **Remove Class**:

  ```javascript
  element.classList.remove("highlight");
  ```

- **Toggle Class**:
  ```javascript
  element.classList.toggle("highlight");
  ```

---

### **Remove Node**

```javascript
let element = document.getElementById("box");
element.remove();
```

---

### **Event Listeners**

Event listeners let you run JavaScript when a specific event occurs.

- **Add an Event Listener**:

  ```javascript
  let button = document.querySelector("button");
  button.addEventListener("click", () => {
    console.log("Button was clicked!");
  });
  ```

- **Remove an Event Listener**:
  ```javascript
  const handleClick = () => console.log("Button was clicked!");
  button.addEventListener("click", handleClick);
  button.removeEventListener("click", handleClick);
  ```

---

## **JavaScript Event Flow**

Events in JavaScript follow a specific flow:

1. **Capturing Phase:** Event moves from the root to the target element.
2. **Target Phase:** Event reaches the target element.
3. **Bubbling Phase:** Event propagates back to the root.

### Example of Event Bubbling:

```javascript
document.querySelector("div").addEventListener("click", () => {
  console.log("Div clicked!");
});

document.querySelector("button").addEventListener("click", () => {
  console.log("Button clicked!");
});
```

Clicking the button will log:

```
Button clicked!
Div clicked!
```

---

## **Summary of the DOM**

The DOM enables dynamic, interactive web applications by providing methods to query, traverse, and manipulate the document structure. Mastering the DOM unlocks the full potential of JavaScript in web development. Use the methods and concepts outlined here to build user-driven, responsive web applications.
