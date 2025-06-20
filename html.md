################### **HTML** ##################

1. **Introduction to HTML**

   - Basic Structure of an HTML Document

2. **HTML Elements and Tags**

   - Headings
   - Paragraphs
   - Bold and Italic Text
   - Lists
     - Unordered List
     - Ordered List
   - Links
   - Images

3. **HTML Forms**

   - Basic Form Structure
   - Input Types (text, email, submit)

4. **HTML Tables**

   - Basic Table Structure
   - Table Rows, Headers, and Data Cells

5. **HTML Semantic Elements**

   - Header
   - Nav
   - Section
   - Main
   - Footer

   - Div

6. **HTML Multimedia Elements**

   - Audio
   - Video

7. **HTML Attributes**
   - Class
   - ID
   - Style
   - Src
   - Href

**Introduction to HTML**

HTML (HyperText Markup Language) is the standard language for creating web
pages. HTML uses a system of tags to define the structure and content of a web
page. It is composed of a series of elements, where each element has an opening
tag and a closing tag, and the content in between them.

Basic Structure of an HTML Document

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>

</body>
</html>

**Explanation**

1. `<!DOCTYPE html>`: Declares the document type and version of HTML.
2. `<html lang="en">`: The root element of the page. The `lang` attribute
   specifies the language (English in this case).
3. `<head>`: Contains metadata like the character set and title.
4. `<meta charset="UTF-8">`: Sets the character encoding to UTF-8.
5. `<meta name="viewport" content="width=device-width, initial-scale=1.0">`:
   Ensures the page is responsive, adjusting to the device's width.
6. `<title>`: Sets the title of the page, shown in the browser's tab.
7. `<body>`: Contains the content of the webpage, such as headings and
   paragraphs.

---

**HTML Elements and Tags**

HTML consists of elements, each defined by a tag.

**Headings** HTML provides six levels of headings, from `<h1>` (most important)
to `<h6>` (least important).

<h1>This is an H1 heading</h1>
<h2>This is an H2 heading</h2>
<h3>This is an H3 heading</h3>

**Paragraphs** To create a block of text, you use the `<p>` element.

<p>This is a paragraph of text that explains more about HTML elements.</p>

**Bold and Italic Text**

- `<b>` or `<strong>` for bold text.
- `<i>` or `<em>` for italic text.

<p>This is <b>bold</b> and this is <i>italic</i> text.</p>
<p>This is <strong>important</strong> and this is <em>emphasized</em> text.</p>

**Lists** HTML supports two types of lists: unordered and ordered.

**Unordered List** (`<ul>`)

<ul>
    <li>itme 1</li> <!--put h1 inside li-->
    <li>Item 2</li> <!--put p inside li-->
    <li>Item 3</li> <!--put strong inside li-->
</ul>

**Ordered List** (`<ol>`)

<ol>
    <li>First item</li>
    <li>Second item</li>
    <li>Third item</li>
</ol>

**Links** To create a hyperlink, you use the `<a>` element with the `href`
attribute.

<a href="https://www.netflix.com/ng/">Click here to visit Netflix</a>

**Images** You can embed images using the `<img>` tag. The `src` attribute
specifies the image source, and `alt` provides alternative text if the image
doesn't load.

<img src="image.jpg" alt="A description of the image">

---

**HTML Forms**

HTML forms are used to collect user input and send it to a server for
processing. A form can include various input types like text fields, checkboxes,
and buttons.

<form>
    <label for="name">Name:</label>
    <input type="text" id="name" name="name">

    <label for="email">Email:</label>
    <input type="email" id="email" name="email">

    <input type="submit" value="Submit">

</form>

Explanation:

1. `<form>`: The form container with `action` (where to send data) and `method`
   (POST or GET).
2. `<label>`: Describes the input fields.
3. `<input>`: Different input types like text, email, and submit.

---

**HTML Tables**

Tables are used to display data in rows and columns.

<table>
    <tr>
        <th>Header 1</th>
        <th>Header 2</th>
    </tr>
    <tr>
        <td>Row 1, Cell 1</td>
        <td>Row 1, Cell 2</td>
    </tr>
    <tr>
        <td>Row 2, Cell 1</td>
        <td>Row 2, Cell 2</td>
    </tr>
</table>

Explanation:

1. `<table>`: Defines the table.
2. `<tr>`: Table row.
3. `<th>`: Table header cell (bold and centered by default).
4. `<td>`: Table data cell.

---

**HTML Semantic Elements**

Semantic HTML elements help give meaning to the structure of the webpage.

<header>
    <h1>Page Header</h1>
</header>

<nav>
    <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
    </ul>
</nav>

<main>
    <section>
        <h2>Section Title</h2>
        <p>Content in this section.</p>
    </section>
</main>

<footer>
    <p>Page Footer</p>
</footer>

Semantic Elements:

- `<header>`: Represents the header section.
- `<nav>`: Defines the navigation links.
- `<main>`: Main content of the document.
- `<section>`: Groups related content.
- `<footer>`: Footer of the page.

---

**HTML Multimedia Elements**

You can embed multimedia content like audio and video.

**Audio**

<audio controls>
<source src="audio.mp3" type="audio/mpeg">
Your browser does not support the audio element.
</audio>

**Video**

<video controls width="400">
<source src="video.mp4" type="video/mp4">
Your browser does not support the video element.
</video>

---

**HTML Attributes**

Attributes provide additional information about HTML elements. Common attributes
include:

- `class`: Assigns CSS class to the element.
- `id`: Unique identifier for an element.
- `style`: Inline CSS for the element.
- `src`: Source for media files (e.g., images, videos).
- `href`: Link target for `<a>` elements.

<p class="highlight">HIGHLIGHT</p>
<p id="intro">INTRO</p>
<p style="color:blue;">COLOR</p>

<!-- This is a comment in HTML -->
