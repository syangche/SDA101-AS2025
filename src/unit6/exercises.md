
### Exercise 1 - Exploring DOM
You will build a simple interactive web page that demonstrates DOM access, traversal, and manipulation

#### Part 1: Basic Structure

Create an index.html file and add the following structure:

```html
<!DOCTYPE html>
<html>
<head>
  <title>DOM Practice</title>
  <style>
    body { font-family: Arial; margin: 20px; }
    .highlight { color: crimson; font-weight: bold; }
    .box { padding: 10px; border: 1px solid #ccc; margin-top: 10px; }
  </style>
</head>
<body>
  <h1 id="main-title">My DOM Playground</h1>
  <p class="content">This is paragraph one.</p>
  <p class="content">This is paragraph two.</p>

  <div id="container" class="box">
    <h3>Container Section</h3>
    <p>This is inside a container.</p>
  </div>

  <button id="changeTextBtn">Change Text</button>
  <button id="addElementBtn">Add New Element</button>
  <button id="removeElementBtn">Remove Last Element</button>

  <script src="script.js"></script>
</body>
</html>
```

#### Part 2: Write JavaScript (in script.js)

Practice these concepts step by step:

1. Selecting Elements

```js
const title = document.getElementById("main-title");
const paragraphs = document.getElementsByClassName("content");
const container = document.getElementById("container");
```

2. Traversing the DOM

```js
console.log(container.parentElement);      // parent of container
console.log(container.children);           // all children
console.log(container.firstElementChild);  // first child element
```
3. Manipulating the content

```js
title.textContent = "Welcome to the DOM Practice!";
paragraphs[0].style.color = "green";
```

4. Adding Event Listeners

```js
document.getElementById("changeTextBtn").addEventListener("click", () => {
  title.textContent = "Text Changed via Button Click!";
});

document.getElementById("addElementBtn").addEventListener("click", () => {
  const newPara = document.createElement("p");
  newPara.textContent = "New paragraph added!";
  newPara.classList.add("highlight");
  container.appendChild(newPara);
});

document.getElementById("removeElementBtn").addEventListener("click", () => {
  const lastChild = container.lastElementChild;
  if (lastChild && lastChild.tagName === "P") {
    container.removeChild(lastChild);
  }
});
```

### Optional Challenge:

Add a new button:

- When clicked, it toggles a class (highlight) on all `<p>` elements to change their color.


---

---
---
### Exercise 2 - Basic form validation

Implement **client-side form validation** using **Vanilla JavaScript**.  
Your goal is to make sure the form checks for valid user input **in real-time** (as the user types), without reloading the page.

---

#### What You’ll Build

A simple **registration form** with the following fields:
- Username  
- Email  
- Password  
- Confirm Password  

---

##### Step 1: Create the HTML form
Create a basic HTML form containing:
- `<input>` fields for username, email, password, and confirm password.  
- A **Submit** button.  
- Give each input field a unique `id` so you can easily access them in JavaScript.  

Example:
```html
<form id="registerForm">
  <label>Username</label>
  <input type="text" id="username" />

  <label>Email</label>
  <input type="email" id="email" />

  <label>Password</label>
  <input type="password" id="password" />

  <label>Confirm Password</label>
  <input type="password" id="confirmPassword" />

  <button type="submit" disabled>Register</button>
</form>
<div id="errorMessages"></div>
```

##### Step 2: Connect JavaScript to your HTML

Link your JavaScript file at the end of the `<body>` section:

```js
<script src="script.js"></script>
```

#### Step 3: Add real-time validation

Use JavaScript to check each field **as the user types** (`input` event).

#### Validation Rules

| Field | Validation Rule |
|-------|------------------|
| **Username** | Must be at least **3 characters** long |
| **Email** | Must follow correct email format (e.g., `someone@example.com`) |
| **Password** | Must include:<br> - Minimum **8 characters** <br> - At least **one uppercase letter** <br> - At least **one lowercase letter** <br> - At least **one special character** (e.g., @, #, $, %) |
| **Confirm Password** | Must **match the password field** |

---

#### Step 4: Show error messages dynamically

Use **DOM manipulation** to display helpful messages below each input field.

Example:
```js
usernameError.textContent = "Username must be at least 3 characters long";
```
#### Step 5: Disable the Submit button until all fields are valid

- Initially, keep the **Submit** button **disabled**.  
- Only enable it when **all validations pass**.

#### Example Logic

```js
if (allFieldsAreValid) {
  submitButton.disabled = false;
} else {
  submitButton.disabled = true;
}
```
#### Step 6: (Optional) Style your form

Use CSS to make:
- Error messages appear in red.
- Valid inputs have green borders.