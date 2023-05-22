# Tutorial

## [Building your first web page](https://learn.shayhowe.com/html-css/building-your-first-web-page/)

- Build it with HTML and CSS.

## [What are HTML and CSS?](https://learn.shayhowe.com/html-css/building-your-first-web-page/#what-are-html-and-css)

- HTML: Gives content structure and meaning by defining that content as different things, ie headings, paragraphs, images.
- CSS: (Cascading Style Sheets) is a presentation language made to style the appearance of content, ie fonts, colours.
- The two languages are independent of each other. CSS should not be written inside of an HTML document and vice versa. As a rule HTML is for content and CSS is for the appearance of content.

## [Understanding Common HTML terms](https://learn.shayhowe.com/html-css/building-your-first-web-page/#common-html-terms)

- Elements:
  - Designators that define the structure and contentof objects within a page:
    - Multiple levels of headings `<h1>` to `<h6>`
    - Parapgraphs `<p>`
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
  
