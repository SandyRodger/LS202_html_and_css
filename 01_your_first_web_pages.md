# [Your First Web Pages](https://launchschool.com/lessons/4495fbf7)

## [Welcome](https://launchschool.com/lessons/4495fbf7/assignments/7e8e0793)	

### A few words about mastery and this course.

- mastery isn't necessary

### Where to find more Information.

- google
- The [Mozilla Developer Netwrok](https://developer.mozilla.org/)
- The [W3C](http://www.w3.org/)

### [introduction](https://launchschool.com/lessons/4495fbf7/assignments/911a8332)

- type out all the examples and save the files in your development system. It's necessary for muscle memory and deeper learning.

#### What to focus on

- Understanding enough HTML and CSS to construct pretty web-pages. But you don't need to be an expert.

##### Vocabulary

- element and tag
- self-closing tag
- document type definition (DOCTYPE, DTD)
- attribute
- selector
- property
- id, class, name

##### Understanding the difference between html and css

- They intertwine and seem to do the same thing, but they are distinct.
  - HTML: structure and content of a web-page
  - CSS: apearance / presentation
- There can be some overlap.

##### HTML and CSS syntax

- There isn't a lot, so learnt it well.

##### Structure of a web-page

- Web-pages always start out with some boiler-plate code that define the general layout of the document. 
- This has 
  - DOCTYPE
  - `<html>`
  - `<head>`
  - `<body>`
  
##### Basic HTML elements
  
- Use html lots to learn it well, but don't aim to learn it all.
- Start by using the `<p>` (paragraph), `<a>` (anchor) and `<h1>` to `<h6>` header elements.
- Also:
  - `<em>`, `<strong>`
  - `<header>`, `<main>`
  - `<article>`, `<section>`, `<aside>`
  - `<div>` and `<span>`

##### Using CSS with HTML

- There are 3 ways to use CSS in a HTML document:
  - Inline
  - Internal
  - External
- Learn to use the `<style>` tag for internal CSS.

##### Basic CSS selectors

- Three primary types:
  - tag : selects elements based on tag name
  - id  : selects elements based on id attribute
  - class : selects elements based on class attribute.
- Learn their syntax, but not theit combinations. For this rely on documentation.

##### CSS Properties

- Rely on documentation, don't aim to memorise these. This way you'll only remember the stuff that comes up all the time.
- The most important properties (which you should memorise) in this lessons are:
  - `color`
  - `background-color`
  - `font-family`
  - `font-size`

##### Use your browser's inspector

- For looking at the structure of web-pages.

##### Study from the summary

- It is a good list of the topics and terminology you should know well.

## [Install Software](https://launchschool.com/lessons/4495fbf7/assignments/70abbf75)


### Browser:

- Google Chrome

### HTML and CSS validators

- Use [this](https://validator.w3.org/#validate_by_input) to check your HTML often.
- Do it:
  - after the first draft
  - after any significant changes
  - When you're having problems with the way your page rendersBefore submitting your HTML for a code-review
  - Before deploying your HTML
- And [this](https://jigsaw.w3.org/css-validator/#validate_by_input) for CSS.
- Validators help prevent bugs and will save time overall. Don't ignore them.

### Linters

- Check computer code for errors, misuse and style issues. (like Rubocop i guess, but without the conformance to standards).
- Not the same as validators 

| Linters | Validators | 
| :---: | :---: |
|detect poor indentation|Find uses of deprecated elements |
|detect poor formatting |Find uses of poor element nesting|
|detect failures to show best practice |Find uses of non-standard attributes|

- Most languages have linters

## [Getting Started](https://launchschool.com/lessons/4495fbf7/assignments/ea41131e)

- tutorial for the basics.

### Before you start

- The first 3 parts of the tutorial cover:
  - Vocabulary
  - Syntax of HTML and CSS.
  - Some HTML elements
  - CSS selectors and properties
  - `class` and `id` attributes (and coresponding class/id selectors, `.class-name`, `#id-name`)
- Also (slightly less importantly)
  - how to write comments in HTML and CSS.
  - The difference between `<header>`, `<head>` and `<h1>` to `<h6>`
  - Relative and absolute paths.
  - The CSS cascade and specificity.
- Get into the habit of looking up the MDN documentation for each HTML tag or CSS property.

### Read the tutorial

- [Lesson 1: Building your first web-page](https://github.com/SandyRodger/LS202_html_and_css/blob/main/shay_howe_tutorial.md#lesson-1--building-your-first-web-page)
- [Lesson 2: Getting to know HTML](https://github.com/SandyRodger/LS202_html_and_css/blob/main/shay_howe_tutorial.md#lesson-2-getting-to-know-html)
- [Lesson 3: Getting to know CSS](https://github.com/SandyRodger/LS202_html_and_css/blob/main/shay_howe_tutorial.md#lesson-3-getting-to-know-css)

### Afterthoughts

- Be aware of the difference between element and tag. Tags contain elements.
- Tag types:
  - Opening tag: `<p>`
  - Closing tag </p>  # this isn't rendering properly, but it's the closing `p` tag
    - AKA 'self-closing element', 'self-contained element', 'empty element', 'void element'. 
  - Self-closing tag `<br>` (most tags are not self closing).
- HTML elements will always have the first 2, or the 3rd.
- Terminology can be mixed up for this. We can talk about `p` as the tag or `<p>` as the tag. We may also say `p` element instead of `<p> ... </p>` element.
- Attributes can use double or single quotes:

```<a href="another_page.html">Next page</a>```. double quotes are better

or

```<a href='another_page.html'>Next page</a>```

- If your browser considers an attribute to be invalid it simply ignores them. This can make debugging hard.
- Do the rest of the tutorial if you feel like you want to know more HTML / CSS.

## [Creating a HTML skeleton](https://launchschool.com/lessons/4495fbf7/assignments/a52de9d4)

- like the `new_meal` template on cal-cou, you don't want to repeatedly type out the template of a HTML file. 
- This is your 'HTML skeleton' or 'HTML Scaffold'

### Creating the HTML Skeleton

- It could look like this:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>your page title goes here</title>
    <meta charset="utf-8">
  </head>
  <body>
  </body>
</html>
```

- There are 3 ways to have a skeleton on hand:
  - save it as a `skeleton.html` file.
  - Define a "snippet" in your editor with the code, to be inserted when you need it.
  - Create a personal "Gist" that contains the code and copy/paste it from there.
- The skeleton includes:
  - `<!DOCTYPE html>`: This is the **Document Type Definition** (aka **DTD** or **DOCTYPE**). Officially this isn't part of the HTML and isnt a tag or element, even though it looks like one. It just tells the browser what kind of markup to expect, ie `XML`. You can lower-case this, although twasen't ever so, this is to do with variation in previous HTML versions.
  - The `html` element encloses the whole html document. The `lang="en" attribute tells the browser that the web-page uses English. All other content and meta-data must be between these tags.
  - The `head` element wraps the document header, which consists of elements that provide additional (or meta) information to the browser. `title` gives the page a title. `<meta charset="utf-8">` tells the browser to expect UTF-8 encoding. Most browsers display the title in the title bar or tab, so be sure to write a title.
  - `meta` tags are self-closing. To close a self-closing tag is seen as incorrect by the W3C HTML Validator.
  - The 'body' area of the code is the content of the page.
  - Technically a HTML file requires all 4 of these things, but in practice they can each be ommitted. A browser will often fill in the gaps.

#### Indentation

- 2 spaces after each open tag.
- Self-closing tags don't indent. Also commonly `head` and `body`.

## [Classes, IDs and Names](https://launchschool.com/lessons/4495fbf7/assignments/0941b604_)

- [Shay Howe section on this](https://github.com/SandyRodger/LS202_html_and_css/blob/main/shay_howe_tutorial.md#working-with-selectors)
- There are 3 ways to identify elements:
  - Class
  - ID
  - Name (only for some elements)

### Classes

- This is for elements you want to style consistently. The example below is for 'teaching assistants'.

```html
<table>
  <tbody>
    <tr class="teaching-assistant">
      <td>Elizabeth</td>
      <td>JS230</td>
    </tr>

    <tr>
      <td>Nancy</td>
      <td>RB101</td>
    </tr>

    <tr>
      <td>Joe</td>
      <td>RB120</td>
    </tr>

    <tr class="teaching-assistant">
      <td>Pete</td>
      <td>JS225</td>
    </tr>

    <tr>
      <td>Kim</td>
      <td>LS202</td>
    </tr>
  </tbody>
</table>
```

```css
tr {
  background-color: lime;
  font-size: 200%;
}

.teaching-assistant {
  background-color: yellow;
}
```

<img width="202" alt="Screenshot 2023-05-30 at 08 36 18" src="https://github.com/SandyRodger/LS202_html_and_css/assets/78854926/d35fbdc7-23ab-4157-9488-52664e05e681">

Overview:
- `class` attributes assign class(es) to an element.
- No limit to elements assigned to a class.
- An element can belong to multiple classes. List them seperated by a space: `class="executive management full-time"`.
- Use semantic class names, ie 'teaching assistant' rather than 'yellow background'.
- Use css selectors (`.classname`) to select elements by class.
- Class selectors have lower specificity than ID selsctors, but higher than Tag Name selectors (so the order is ID, Class, Name). [More here](https://github.com/SandyRodger/LS202_html_and_css/blob/main/shay_howe_tutorial.md#calculating-specificity)

### IDs

- Is a unique string attached to a single element:

```html
<h1>This is a plain h1 heading</h1>
<h1 id="headline">This is my headline</h1>
```

```css
#headline {
  color: red;
  font-size: 48px;
}
```

Overview:
- Use `id` attribute to assign an ID to an element.
- Each ID on a page should be unique.
- Each element can have 1 or 0.
- Use semantic id names, like `headline`, rather than `big font`.
- Use CSS ID selectors (`#idname`) to identify elements by ID, eg `#headline`.
- ID selectors have higher specificity thatn class selectors.
- Browsers won't warn you about ID duplication, so be careful.

### Names

- We won't use this until much later.
- `name` attributes tie form elements to data on the server.
- It's not really for styling.
- You can use `[name="field-name"]` to select elements, but you should rather use a class or ID selector instead.
- When you submit a form the browser sends the form data to the server using name/value pairs, taking the name from the associated `name` attribute.

```html
<form method="get" action="#">
  <label for="first-name-field">First name:</label>
  <input type="text" name="first-name" id="first-name-field">

  <label for="last-name-field">Last name:</label>
  <input type="text" name="last-name" id="last-name-field">

  <input type="submit" value="Search">
</form>
```

- For this the browser sends a query string which looks like this (note the `id` attribute is not sent: 

``` first-name=Joe&last-name=Jones ```

#### For attributes

- More on this later, but...
- There is a 'for' attribute, which references an ID.
- It's accepted practice to use both `name` and `id` on form elements and have the same value for both:
```html
<form method="get" action="#">
  <label for="first-name">First name:</label>
  <input type="text" name="first-name" id="first-name">

  <label for="last-name">Last name:</label>
  <input type="text" name="last-name" id="last-name">

  <input type="submit" value="Search">
</form>
```

Overview:

- Use the `name` attribute to assign a name to a form-data element that the browser can then take to the server as a value.
- Not all tags can take a `name` attribute.
- ALWAYS use a `name` attribute on form elements tha accept them.
- Each name in a form should be unique, except for:
  - radio buttons that belong to a single group.
  - checkboxes that belong to a single group.
- Use descriptive names, not semantic. So `name="last-name"`, rather than `name="input-field"`.
- Avoid trying to select elements in CSS with the `name`  attribute.

## [Practice Problems: Semantics](https://launchschool.com/lessons/4495fbf7/assignments/0d4ac29e)

- Semantic HTML: Using HTML to show the structure and purpose of a document, not it's presentation.
- [Here](http://html5doctor.com/downloads/h5d-sectioning-flowchart.pdf) is a flow-chart to help see which tags should be used.

1. 
Semantic: <article>	 <aside> <div> <footer>	<h3>	<header>	<section>  <span>	
Not semantic:  <strong> <b>
  
Answer: `<div>` and `<span>` are not semantic, the rest are.
  
2.
  <section>, <aside>, <article>, or <div>

|  | Once | Twice | Thrice | Got it?
| :--- | :---: | :---: | :---: | :--- |
|1. Welcome| 18/5/23 |||50%|
|2	Introduction|	22/5/23 |||50%|
|3	Install Software|	22/5/23| ||50%|
|4	Getting Started|22/5/23 | ||50%|
|5	Creating an HTML Skeleton|27/5/23 	| ||%|
|6	Classes, IDs, and Names|30/5/23		| ||%|
|7	Practice Problems: Semantics|	30/5/23		| ||%|
|8	Walkthrough Project: A Simple Web Page|	| ||%|
|9	Walkthrough Project: Adding Style to Your Web Page|		| ||%|
|10	Guided Project: A Personal Profile|		| ||%|
|11	Practice Problems: Text Formatting|		| ||%|
|12	On Your Own: Creating a Simple Page	|	| ||%|
|13	Practice Problems: CSS Selectors|		| ||%|
|14	CSS Diner	|	| ||%|
|15	Using the Chrome Inspector	|	| ||%|
|16	HTML and CSS Style Guide|		| ||%|
|17	Summary|		| ||%|
|18	Quiz 1|	| ||%|
