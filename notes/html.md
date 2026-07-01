
# HTML Notes
**Date:** 29-June-2026

---

## What is HTML?
- HyperText Markup Language
- Gives structure to the webpage
- Like a skeleton
- Not a programming language - it is a markup language, it has no logic or conditions

---

## Headings - `<h1>` to `<h6>`
- These are the heading elements
- Higher the number, lower the importance
- Only one `<h1>` per page is preferred - search engines treat it as the main topic of the page, multiple `<h1>` tags hurt SEO

---

## Paragraph - `<p>`
- Specifies text as a paragraph

---

## Comments
```html
<!-- this is a comment -->
```
- Hides code from the webpage
- Gives classification about the code which is helpful for screen readers
- Sometimes used to stop code from executing

---

## `<main>`
```html
<main></main>
```
- Specifies the code part inside it as the main part of the document
- Helpful for screen readers - they skip navigation and jump directly to main content
- Only one `<main>` per page

---

## `<img>`
```html
<img src="image-path.jpg" alt="description">
```
- Void element - no closing tag
- Specifies an image in a document
- `src` - specifies the URL or path of the image, where it is located
- `alt` - gives a description about the image which helps screen readers; also shows when image fails to load

---

## Anchor Element - `<a>`
```html
<a href="https://example.com">Click here</a>
<a href="https://example.com" target="_blank" rel="noopener noreferrer">Open in new tab</a>
```
- Specifies links
- Makes text as a clickable link
- `href` attribute specifies which page that link should open
- `target="_blank"` - opens the link in a new page
- Always add `rel="noopener noreferrer"` with `target="_blank"` - without it the new tab can access and manipulate the original page, which is a security risk

---

## Nesting
- Having HTML elements inside another HTML element
- Must be closed in the reverse order they were opened

```html
<!-- Correct -->
<div><p>Hello</p></div>

<!-- Wrong -->
<div><p>Hello</div></p>
```

---

## `<section>`
```html
<section>
  <h2>Title</h2>
  <p>Content...</p>
</section>
```
- Groups the elements as a section
- Like headings, footers etc.

---

## Lists
- To list items using `<li>`

**Unordered list** - when order does not matter:
```html
<ul>
  <li>Item</li>
</ul>
```

**Ordered list** - when order matters:
```html
<ol>
  <li>Step 1</li>
</ol>
```
- To list items if there is no order, unordered list is used
- To have added sequence we use ordered list

---

## `<figure>` and `<figcaption>`
```html
<figure>
  <img src="chart.png" alt="chart">
  <figcaption>Description of the image</figcaption>
</figure>
```
- `<figure>` - tells the browser and screen readers that the content inside it forms a single unit; used to wrap self-contained content
- `<figcaption>` - provides information or description about the image

---

## `<em>`
```html
<em>emphasized text</em>
```
- Emphasizes specific words or phrases in a sentence
- Screen readers change tone when reading `<em>` content

---

## `<strong>`
```html
<strong>important text</strong>
```
- Specifies specific words or phrases as important or urgent to highlight
- `<b>` vs `<strong>` - `<b>` is only visual (bold styling, no meaning), `<strong>` has semantic meaning and tells the browser this content is important. Always prefer `<strong>`.

---

## Forms
```html
<form action="/path" method="POST">
  <!-- inputs here -->
</form>
```
- To get user information as input, we use forms
- `action` - specifies where the user input should be sent (path)
- `method` - GET or POST
  - **GET** - data is sent in the URL, visible to everyone, never use for passwords or sensitive data
  - **POST** - data is sent in the request body, not visible in the URL, use for login forms and sensitive data

---

## `<input>`
```html
<input type="text" name="username" placeholder="Enter name" required>
```
- Void element - no closing tag
- Takes various types of input
- `type` - specifies which kind of input (text, email, password, checkbox, radio button etc.)
- `name` - specifies name for an input; used to identify the data when form is submitted
- `placeholder` - gives the user a hint about what to enter as input
- `required` - makes the field required; the form cannot be submitted without that input

---

## `<input>` id
```html
<input type="text" id="username">
```
- `id` attribute gives a unique id for an element
- `id` should be unique - not to be repeated in the whole document

---

## `<button>`
```html
<button type="submit">Submit</button>
<button type="button">Click</button>
```
- Clickable event listener
- By default in a form it works as submit - uses entered input to the path where action attribute is specified
- When using with JavaScript, always set `type="button"` to prevent accidental form submission

---

## Radio Button
```html
<input type="radio" name="color" value="red"> Red
<input type="radio" name="color" value="blue"> Blue
```
- `type="radio"` - to choose one option from multiple choices
- We can select all the radio buttons without `name` - to avoid that, give the same `name` for all options in the group so only one option can be selected
- `value` - identifies which option was selected when the form is submitted

---

## `<label>`
```html
<label for="email">Email:</label>
<input type="email" id="email">
```
- Specifies the associated text for input fields, radio buttons, checkboxes etc.
- Clicking on that text also selects the input
- `for` value must match the `id` of the input it is associated with
- Screen readers read the label so the user knows what to type - important for accessibility

---

## `<fieldset>` and `<legend>`
```html
<fieldset>
  <legend>Choose your color:</legend>
  <input type="radio" name="color" value="red"> Red
  <input type="radio" name="color" value="blue"> Blue
</fieldset>
```
- `<fieldset>` - groups input tags to make them as one unit; makes them a block-level element
- `<legend>` - gives description of a fieldset; also gives a box around it; for example gives a question to select answers

---

## Void Elements - Quick Reference
Elements that have no closing tag:

| Element | Use |
|---|---|
| `<img>` | Image |
| `<input>` | Form input |
| `<br>` | Line break |
| `<hr>` | Horizontal divider |
| `<link>` | Link a CSS file |
| `<meta>` | Page metadata |

---

## Resources
- MDN Docs
- W3 Schools
- freeCodeCamp
- The Odin Project
