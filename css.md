################ **PROBLEM 2** ######################

1. **Introduction to CSS**

   - Basic Structure of a CSS File

2. **Ways to Add CSS to HTML**

   - Inline CSS
   - Internal CSS
   - External CSS

3. **CSS Selectors**

   - Element Selector
   - Class Selector
   - ID Selector
   - Group Selector
   - Descendant Selector

4. **CSS Properties**

- Width and Height
- Text Styling
  - Color
  - Font-size
  - Text-align
  - Font-family
- Background
  - Background-color
  - Background-image
- Box Model

  - Padding
  - Border
  - Margin

- Display Property
- Positioning

  - Static
  - Relative
  - Absolute
  - Fixed

- Sticky

- Flexbox Layout
- Grid

5. **CSS Units**

   - px, %, em, rem

6. **CSS Pseudo-Classes and Pseudo-Elements**

   - Pseudo-Classes
     - :hover
   - Pseudo-Elements
     - ::before and ::after

7. **CSS Media Queries**

   - Responsive Design

8. **CSS Best Practices**
   - DRY Principle
   <!-- - Use External Stylesheets -->
   - Descriptive Class Names
   - Use Shorthand Properties

**Introduction to CSS**
CSS (Cascading Style Sheets) is used to control the presentation and layout of web pages. While HTML structures the content, CSS styles it, such as adding colors, spacing, and fonts.

Basic Structure of a CSS File

```css
/* This is a comment in CSS */
selector {
  property: value;
}
```

Example:

```css
p {
  color: blue;
  font-size: 16px;
}
```

In this example:

- `p` is the **selector** (targeting the `<p>` tag).
- `color` and `font-size` are **properties**.
- `blue` and `16px` are **values** assigned to the respective properties.

---

**Ways to Add CSS to HTML**

There are three ways to include CSS in an HTML document.

1.  **Inline CSS**
    You can apply CSS directly within an HTML element using the `style` attribute.

```html
<p style="color: red;">This is a red paragraph.</p>
```

2.  **Internal CSS**
    Defined within the `<style>` tag inside the `<head>` section of an HTML document.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <style>
      p {
        color: green;
        font-size: 20px;
      }
    </style>
  </head>
  <body>
    <p>This is a green paragraph with internal CSS.</p>
  </body>
</html>
```

3.  **External CSS**
    Link an external `.css` file using the `<link>` tag inside the `<head>` section.

```html
<!-- HTML File -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <p>This paragraph is styled with external CSS.</p>
  </body>
</html>
```

```css
/* External CSS (styles.css) */
p {
  color: purple;
  font-size: 18px;
}
```

---

**CSS Selectors**

Selectors are used to target the HTML elements you want to style. Below are the most common selectors:

1.  **Element Selector**
    Selects all instances of a specific HTML element.

```css
h1 {
  color: red;
}
```

2.  **Class Selector**
    Selects all elements with a specific class. Classes are defined with a period `.` before the class name.

```html
<p class="intro">This is a paragraph with class selector.</p>
```

```css
.intro {
  color: blue;
}
```

3.  **ID Selector**
    Selects an element with a specific ID. IDs are defined with a hash `` before the ID name.

```html
<p id="main-text">This is a paragraph with ID selector.</p>
```

```css
#main-text {
  color: green;
}
```

4.  **Group Selector**
    You can group multiple selectors by separating them with a comma.

```css
h1,
p {
  color: darkblue;
}
```

5.  **Descendant Selector**
    Selects elements that are nested within another element.

```html
<div class="container">
  <p>This paragraph is inside a div.</p>
</div>
```

```css
.container p {
  color: orange;
}
```

---

**CSS Properties**

1.  **Text Styling**

- **Color**: Sets the text color.

```css
p {
  color: red;
}
```

- **Font-size**: Defines the size of the text.

```css
p {
  font-size: 18px;
}
```

- **Text-align**: Aligns the text (left, right, center, or justify).

```css
p {
  text-align: center;
}
```

- **Font-family**: Defines the font to be used.

```css
p {
  font-family: Arial, sans-serif;
}
```

2.  **Background**

- **Background-color**: Sets the background color of an element.

```css
body {
  background-color: lightgray;
}
```

- **Background-image**: Sets an image as the background.

```css
body {
  background-image: url("background.jpg");
  background-size: cover;
}
```

3.  **Box Model**
    CSS treats each element as a box, consisting of four parts: content, padding, border, and margin.

Border
Creates a border around the element.

```css
p {
  border: 2px solid black;
}
```

Padding
The space between the content and the border.

```css
p {
  padding: 10px;
}
```

Margin
The space outside the border, separating the element from other elements.

```css
p {
  margin: 20px;
}
```

Example of Box Model:

```css
div {
  padding: 20px;
  border: 5px solid blue;
  margin: 15px;
}
```

4.  **Width and Height**
    You can define the width and height of elements.

```css
div {
  width: 300px;
  height: 200px;
}
```

5.  **Display Property**
    The `display` property controls how an element is displayed on the page.

- `block`: The element takes up the full width available.
- `inline`: The element takes up only as much width as needed.
- `inline-block`: Allows elements to sit next to each other while maintaining the block-like properties.

```css
div {
  display: block;
}
span {
  display: inline;
}
```

6.  **Positioning**
    CSS provides different positioning techniques.

- **Static (default)**: Elements appear in the normal document flow.
- **Relative**: Positioned relative to its normal position.
- **Absolute**: Positioned relative to its nearest positioned ancestor.
- **Fixed**: Positioned relative to the viewport, stays in the same place even when scrolling.

```css
div {
  position: absolute;
  top: 50px;
  left: 100px;
}
```

7.  **Flexbox Layout**
    Flexbox makes it easy to align and distribute space among items in a container.

```css
.container {
  display: flex;
  justify-content: space-around; /* Aligns items with space between them */
  align-items: center; /* Centers items vertically */
}
```

```html
<div class="container">
  <div>Box 1</div>
  <div>Box 2</div>
  <div>Box 3</div>
</div>
```

---

**CSS Units**
CSS uses several units to define sizes and lengths. The most common units are:

- **px**: Pixels (fixed size).
- **%**: Percentage (relative to the parent element).
- **em**: Relative to the font-size of the element.
- **rem**: Relative to the root element's font-size.

Example:

```css
p {
  font-size: 1.5em; /* 1.5 times the font size of the parent */
  margin: 10%; /* 10% of the parent element */
}
```

---

**CSS Pseudo-Classes and Pseudo-Elements**

**Pseudo-Classes**
Pseudo-classes are used to define the special state of an element. Examples include `:hover`, and `:focus`.

- **:hover**: Style changes when the user hovers over an element.

```css
a:hover {
  color: red;
}
```

---

**CSS Media Queries**

Media queries are used to apply different styles depending on the device or screen size. This is essential for responsive design.

```css
@media (max-width: 600px) {
  body {
    background-color: lightblue;
  }
}
```

In this example, the background color will change to light blue when the screen width is 600px or smaller.

---

**CSS Best Practices**

1. **Keep CSS DRY (Don’t Repeat Yourself)**: Reuse styles where possible using classes and grouping selectors.
2. **Use External Stylesheets**: Keep CSS separate from HTML to ensure clean and maintainable code.
3. **Use Descriptive Class Names**: Make class names meaningful and easy to understand.
4. **Use Shorthand Properties**: Combine multiple properties where possible. For example:
   ```css
   margin: 10px 5px 15px 0;
   ```

---
