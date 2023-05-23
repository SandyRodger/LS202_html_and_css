# [Lesson 1 : Building your first web page](https://learn.shayhowe.com/html-css/building-your-first-web-page/)

- Build it with HTML and CSS.

## [What are HTML and CSS?](https://learn.shayhowe.com/html-css/building-your-first-web-page/#what-are-html-and-css)

- HTML: Gives content structure and meaning by defining that content as different things, ie headings, paragraphs, images.
- CSS: (Cascading Style Sheets) is a presentation language made to style the appearance of content, ie fonts, colours.
- The two languages are independent of each other. CSS should not be written inside of an HTML document and vice versa. As a rule HTML is for content and CSS is for the appearance of content.

## [Understanding Common HTML terms](https://learn.shayhowe.com/html-css/building-your-first-web-page/#common-html-terms)

- Elements:
  - Designators that define the structure and content of objects within a page:
    - Multiple levels of headings `<h1>` to `<h6>`
    - Paragraphs `<p>`
    - `<a>`
    - `<div>`
    - `<span>`
    - `<strong>`
    - `<em>`
  - These are written between `<` and `>`.
- Tags:
  - These are what is created by surrounding an element with `<` and `>`.
  - In fact `<...>` is and opening tag. With a `/` at the beginning it is a closing tab\; `</...>. These mark the beginning and end of an element.
- Attributes
  - Properties used to provide additional information about an element.
    - Most commonly:
      - id attribute: identifies and element.
      - class attribute: classifies an element.
      - src attribute: specifies a source for embeddable content.
      - href attribute: provides hyperlink to a linked resource.
  - The format is `attribute name` + `"quoted attribute value"'. For example
    - `<a href="http://shayhowe.com/">Shay Howe</a>`

<img width="606" alt="Screenshot 2023-05-22 at 12 31 43" src="https://github.com/SandyRodger/LS202_html_and_css/assets/78854926/213af917-12f5-455b-8aaa-7f2d114c5062">

## [Setting up the HTML document structure](https://learn.shayhowe.com/html-css/building-your-first-web-page/#html-document-structure)

- HTML documents are plain text documents saved with a `.html` extension rather than `.txt`.
- Microsoft Word and Pages are rich text editors, not text editors, so these won't be suitable for writing HTML.
- All HTML documents must have these elements:
  - `<!DOCTYPE html>`. This is the document type declaration. It says, we are using the latest version of html.
  - `<html>`. This signifies the beginning of the HTML document.
  - `<head>`. Identifies the top of the document, including any metadata. This content in the `head` element will not be displayed on the web-page, but might include:
    - document title
    - links to any external files
    - Any other beneficial meta-data.
  - `<body>`. This is what will be the visible content within a web-page.
- A typical HTML document might look like this:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Hello World</title>
  </head>
  <body>
    <h1>Hello World</h1>
    <p>This is a web page</p>
  </body>
</html>
```
  - Notice how the `head` and `body` come inside the `html` element.
  - The `head` element includes the character encoding of the page via the `<meta charset="utf-8">` tag.
  - The `body` element includes a heading with the `<h1>` element and a paragraph with the `<p>` element.
  - This is called 'nesting'. Nesting is represented with indentation.

### Self closing elements

- Like the `<meta>` tag in the example above, some elements are self-closing.
- Other common self-closing elements are:
  - `<br>`
  - `<img>`
  - `<meta>`
  - `<wbr>`
  - `<embed>`
  - `<input>`
  - `<param>`
  - `<hr>`
  - `<link>`
  - `<source>`

### Code validation

- Use these W3C [HTML](http://validator.w3.org/) and [CSS](http://jigsaw.w3.org/css-validator/) validators to avoid errors. These teach us best practice as well as ironing out mistakes.

## [In Practice](https://learn.shayhowe.com/html-css/building-your-first-web-page/#practice-1)

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Styles Conference</title>
  </head>
  <body>
    <h1>Styles Conference</h1>
    <p>Every year the brightest web designers and front-end developers descend on Chicago to discuss the latest technologies. Join us this August!</p>
  </body>
</html>
```

## [Understanding Common CSS terms](https://learn.shayhowe.com/html-css/building-your-first-web-page/#common-css-terms)

### Selectors

- Which elements in the html page should have a style applied to it. For example, every paragraph, or only a specific paragraph.
- Selectors usually target a class or id value, or target the type of element, like `<p>` or `<h1>`.
- In CSS selectors are followed by curly brackets.
- For example, this selector targets all `p` elements: `p { ... }`.

### Properties

- Once an element has been selected, the properties of these elements' style must be chosen. So these come after a selector, within curly brackets and before a colon.
- Properties include:
  - font-size
  - background
  - color
  - height
  - width
- The example below has us defining the font-size and colour of all `p` elements:

```css
p {
  color: ... ; 
  font-size ...;
  }
```

### Values

- Values are the text between the colon and the semi-colon:

```css
p {
  color: orange ;
  font-size: 16px ;
}
```

<img width="319" alt="Screenshot 2023-05-22 at 14 49 50" src="https://github.com/SandyRodger/LS202_html_and_css/assets/78854926/31a54d36-5788-4940-8ad6-b55e69a1212a">

## [Working with Selectors](https://learn.shayhowe.com/html-css/building-your-first-web-page/#working-with-selectors)

- Type
- Class
- Id

### Type Selectors

- Type selectors target elements by their type. For example we could use a type selector of `div` to target all `<div>` elements.
- For example this css : `div {...}` would select the following html:

```html
<div>...</div>
<div>...</div>
```

### Class Selectors

- Let us select an element based on their class attribute. So you can apply the same style to different elements at the same time by using the same class attribute value across multiple elements.
- In CSS classes are demarked by a leading full-stop followed by the class attribute value. So here the class selector will select any element containing the class attribute value of `awesome` (both division and paragraph elements):
```css
.awesome { ... }
```
selects the following html:
```html
<div class="awesome">...</div>
<p class="awesome">...</p>
```

### ID selectors

- ID selectors are even more precise than class selectors. They use an element's ID attribute as the selector.
- Within CSS, ID selectors are denoted with a leading hash sign, followed by the id attribute value.
```css
#shayhowe { ... }
```
selects the following html:
```html
<div id="shayhowe">...</div>
```

### Additional selectors

- There are many more selectors. See some [here](https://learn.shayhowe.com/advanced-html-css/complex-selectors/)
- For example:
  - Child selectors
    - The descendant selector
    - Direct child selector
  - Sibling selectors
    - general sibling selector
    - adjacent sibling selector
  - Attribute selectors

## [Referencing CSS](https://learn.shayhowe.com/html-css/building-your-first-web-page/#referencing-css)

- To make our CSS talk to our HTML we have to reference the CSS file in our HTML file.
- Best practice is to include all of our styles in a single external style-sheet. This should be referenced from within the `head` element of our HTML document.
- This is helpful for organising our styles so that they are uniformly applied site-wide and changes can be easily implemented.
- (Another options for adding CSS is to use internal and inline styles, but these methods are quite unwieldy and cumbersome).
- Then an exercise to add a `main.css` stylesheet and reference it in `index.html`.

## Using CSS Resets

- Browsers have default settings for CSS.To ensure cross-browser compatibility CSS resets are now commonly used.
- CSS cascades from top to bottom, so we put the reset at the top to override default settings. 
- Many resets are available. A popular one is the [Eric Meyers](http://meyerweb.com/eric/tools/css/reset/) reset.

### Cross browser compatibility testing

- Websites don't have to look the same in every browser, but they should be close.
- You must decide which browsers you want to support and to what degree.

## [In Practice 2](https://learn.shayhowe.com/html-css/building-your-first-web-page/#practice-2)

- Add assets folder
- override defaults with Eric Meyers css settings.

## [Summary](https://learn.shayhowe.com/html-css/building-your-first-web-page/#summary)

- The difference between HTML and CSS
- HTML elements, Tags and Attributes.
- The structure of your first webpage.
- CSS selectors properties and values
- CSS selectors
- CSS in your HTML
- CSS resets

# [Lesson 2: Getting to know HTML](https://learn.shayhowe.com/html-css/getting-to-know-html/)

- Which HTML elements are best used for which types of content.
- How are elements visually displayed on a web-page.
- What do different elements mean semantically.        ----> ?
- Using the right elements goes a long way.

## [Semantics overview](https://learn.shayhowe.com/html-css/getting-to-know-html/#semantics-overview)

- Semantic: 'relating to meaning in language or logic'.
- [Semantics in HTML](https://boagworld.com/dev/semantic-code-in-html/): Giving content on the page structure and meaning by using the proper element.
- It desctribes the value of the content regardless of its style or appearance.
- So the HTML describes what the resource is, and never crosses over into how it should be displayed, ie "large-image".
- Why write semantic HTML:
  - Accessibility: for services that render a web-page for the disabled.
  - SEA (Search Engine Optimisation)
  - Maintainability and Readability
  - Cross device compatibility.
  - Future-proofing.
  - Improved collaboration
  - Faster page-load times
- How to make code more semantic:
  - Make sure HTML tags match their content. so `<h1>` for main headings, `<ul>` and `<ol>` for lists.
  - Minimize the use if tags that are not semantically meaningful, like `<div>` and `<span>`.
  - Use [ARIA attributes](https://www.lullabot.com/articles/what-heck-aria-beginners-guide-aria-accessibility) (Accessible Rich Internet Applications) to add additional information to HTML tags. For example, `aria-label` or `aria-describedby`
  - You can even link more data with an [RDFa](https://rdfa.info), but this is extra.

## Identifying divisions and spans
### Block v. inline elements
### COmments with HTML and CSS
## Text-based elements
### Headings
### Paragraphs
### Bold text with strong
### Italicized text with emphasis
## Building Structure.
### Header
### Navigation
### Article
### Section
### Aside
### Footer
## In practice
### Encoding special characters
## Creating hyperlinks
### Wrapping block-level elements with anchors
### Relative and Absolute paths
### Linking to an email address
### Opening links in a new window
### Linking to parts of a new page
## In practice
## Summary

# [Getting to know CSS](https://learn.shayhowe.com/html-css/getting-to-know-css/)
