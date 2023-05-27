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
  - Minimize the use of tags that are not semantically meaningful, like `<div>` and `<span>`.
  - Use [ARIA attributes](https://www.lullabot.com/articles/what-heck-aria-beginners-guide-aria-accessibility) (Accessible Rich Internet Applications) to add additional information to HTML tags. For example, `aria-label` or `aria-describedby`
  - You can even link more data with an [RDFa](https://rdfa.info), but this is extra.

## [Identifying divisions and spans](https://learn.shayhowe.com/html-css/getting-to-know-html/#divs-and-spans)

- `<div>`s and `<span>`s are HTML elements that act as containers, just for styling. They don't have any intrinstic meaning. That means that `<p>` element is understood to be a paragraph, but a `div` and `span` are just neutral containers.

## Block v. inline elements

- Most elements are one of these.
- Block-level elements:
  - begin on a new line.  
  - Stack one on top of the other.
  - Occupy any available width.
  - May be nested one inside the other.
  - Commonly for larger sections of content, like paragraphs.
- Inline-level elements:
  - Do not begin on a new line.
  - They fall into the normal flow of a document, lining up one after the other.
  - They maintain the width of their content.
  - They can nest inside other inline-level elements, but cannot nest block-level elements.
  - For smaller pieces of content, like a few words.
- Both allow us to target a specific set of content for styling.
- A `<div>` is a block-level element for identifying large groupings of content.
- A `<span>` is an inline level element used to identify smaller groupings of text within a block-level element.
- Divs and Spans will usually have a class or id attribute so that they can be styled properly. THis is where semantic HTML comes in. You want the class/id attribute value to descibe what the div/span is, not what you want it to look like. So 'introduction text' rather than 'large block of text'.
- Shay's example is a box with social media information. The box is orange. Don't call it orange box, because it might change. Call it social:

```html
<!-- Division -->
<div class="social">
  <p>I may be found on...</p>
  <p>Additionally, I have a profile on...</p>
</div>

<!-- Span -->
<p>Soon we'll be <span class="tooltip">writing HTML</span> with the best of them.</p>
```
  
### Comments with HTML and CSS

- The `!`s above are for comments.
- HTML comments start with `<!--` and end with `-->`.
- CSS comments start with `/*` and end with `*/`.

## [Text-based elements](https://learn.shayhowe.com/html-css/getting-to-know-html/#text-based-elements)

- Text is what you find a whole lot of online. So Here's how we do text:
  - Headings
  - Paragraphs
  - Bold Text
  - Italics.

### Headings

- These are Block-level.
- There are 6 rankings.
- They break up content and establish hierarchy.
- They help search engines to index and determine the content on a page.
- Their order is important and should fit the page's content.
- Don't use headings as a lazy way to embolden text.

### Paragraphs

- Headings are often followed by a paragraph.
- `<p>`

### Bold text with strong

- `<strong>` inline-level element. This gives a text strong importance.
- or `<b>`, which is less commonly used, just means to make it look bold, "stylistically offset" -  is how Shay puts it.
```
<!-- Strong importance -->
<p><strong>Caution:</strong> Falling rocks.</p>

<!-- Stylistically offset -->
<p>This recipe calls for <b>bacon</b> and <b>baconnaise</b>.</p>
```

### Italicize text with emphasis

- `<em>` inline-level elements put a stress on the text.
- `<i>` semantically conveys the text with an alternative tone, like quotation marks.

```html
<!-- Stressed emphasis -->
<p>I <em>love</em> Chicago!</p>

<!-- Alternative voice/tone -->
<p> The name <i>Shay</i> means 'a gift'.</p>
```

- These are text-level elements and are great at bringing content to life. Unline structural elements which group content into sections like headers, footers, articles etc.

## [Building Structure](https://learn.shayhowe.com/html-css/getting-to-know-html/#building-structure)

- For a long time web-pages were built with lots of divisions. But they were not great at indicating what the divisions were dividing, so now, since HTML5, we have:
- Structurally based-elements:
  - `<header>`
  - `<nav>`
  - `<article>`
  - `<section>`
  - `<aside>`
  - `<footer>`
- These impove our 'structural semantics'.
- They are block-level elements.
- They have no implied position or style.
- Each of these can be used as many times as you want.

<img width="738" alt="Screenshot 2023-05-24 at 14 07 37" src="https://github.com/SandyRodger/LS202_html_and_css/assets/78854926/f1f86e43-eeb7-4f94-940b-f98d18dfd306">

- It's like a newspaper.

### Header

- Is for the top of the page/article/section - duh.
- It can contain:
  - a header
  - an introductory text
  - a navigation.

- `<header>`, `<head>`, and `<h1>` to `<h6>` elements aren't the same:
  - `<header>` is a structural element that outlines the beginning of a segment. It comes within the `<body>` element.
  - `<head>` is not displayed on a webpage. It's for meta-data, like document title. It goes in the `<html>` element.
  - `<h1>` to `<h6>` which are for different levels of sub-headings.

### Navigation

- A `<nav>` element is for sections of major navigatonal links on a page.
- This element should be reserved for primary navigation sections only, like:
  -  global navigation.
  -  table of contents
  -  previous/next links
  -  other important navigation links.
-  These links are just for links within the same web-site. Outside this website links should use `<a>` elements.

### Article

- The `<article>` element si for a section of independent, self-contained content. Like:
  - Blog posts
  - newspaper articles
  - user-submitted content
- When deciding whether or not to use `<article>` try and see if the content could be replicated anywhere else. It should be able to. It could be in an email, or a leaflet, without losing meaning.

### Section

- Used to Identify a thematic grouping of content. So usually with a heading at the top of it.
- `<section>`s are used to break up the content of a page, usually according to a hierarchy.

### Deciding between `<article>`, `<section>` and `<div>` elements

- Base your decision on the content.
- `<article>` and `<section>` elements are part of a document's structure.
- If you're only dividing the material for style purposes use a `<div>` element.
- If the content adds to the document structure, use the `<article>` element.
- If the content adds to the document structure AND is part of a thematic group of content, use `<section>`.

### Aside

- `<aside>` element is for content such as sidebars, inserts or brief explanations. They are tangentially related to the main content.
- It's block-level, so will always appear on a new line.
```html
<aside> ... </aside>
```

### Footer

- Is for the end or close of a page/article/section.

## In practice

- Add these elements to our `index.html` file.

### Encoding special characters

- Encoded characters will begin with an `&` and end with a `;`.
- For example the word “resumé” would be encoded as 'resum&eacute;'
- Character encodings can be found [here](http://copypastecharacter.com/)

## [Creating hyperlinks](https://learn.shayhowe.com/html-css/getting-to-know-html/#creating-hyperlinks)

- Using `<a>` which is an inline-element.
- Also necessary is the `href` attribute.
- It looks like this: `<a href="http://shayhowe.com">Shay</a>`

### Wrapping block-level elements with anchors

- `<a>` is an inline element and so should not wrap block-level elements, BUT `<a>` is an exception and can wrap anything, including entire blocks of content.

### Relative and Absolute paths

These are differentiated by their href attribute values, which will be their paths.
- Absolute:
  - Links to other websites.
  - href would be `http://google.com` for example.
- Relative: 
  - Links to other pages on the same website. 
  - Does not include their domain name (`.com`, `.org` etc)
  - Path is just the filename of the page. eg `about.html` or `pages/about.html`.
- This is what that looks like:

```html
<!-- Relative Path -->
<a href="about.html">About</a>

<!-- Absolute Path -->
<a href="http://www.google.com/">Google</a>
```

### Linking to an email address

- To create a hyper-link to an email address ("email me!"), that opens a users email, and maybe even populates part of the email.
- At a minimum the sender address will be populated. 
- Other fields which might be populated are subject line, body text.
- To make an email link the `href` attribute should be followed by `mailto:` and then the email address. ie `mailto:abmrodger@gmail.com`.
- To add a subject line, include `subject=` after the email address, seperated from email address by a `?`. Encode spaces with `%20` and line breaks with ` %0A`.
- Body text is added with `body=`. 
- Parameters are seperated with `&`s. 
- Altogether it could look like this: 
`<a href="mailto:shay@awesome.com?subject=Reaching%20Out&body=How%20are%20you">Email Me</a>`

### Opening links in a new window

- Typically links open in the same window, but you can make them open in new windows.
- To do this we use the `target` attribute with a value of `_blank`, which means new window.
- For example: `<a href="http://shayhowe.com/" target="_blank">Shay Howe</a>`

### Linking to parts of a new page

- A common example is 'back-to-top` links.
- We do this by setting the `id` attribute on the element we want to link, then referencing that `id` attribute in the anchor element's `href` attribute.

```html
<body id="top">
  ...
  <a href="#top">Back to top</a>
  ...
</body>
```

## In practice

- Adding multiple pages to the `styles-conference` website and hyper-linking them.

## Summary

- Semantics are for giving our HTML structure and meaning.
- We covered:
  - What semantics are and why they are important.
  - `<div>`s and `<span>`s and the difference between block/inline elements.
  - Different text-based elements for representing content on a page.
  - The HTML5 structural elements.
  - Hyperlinks for navigating to different pages. 

# [Lesson 3: Getting to know CSS](https://learn.shayhowe.com/html-css/getting-to-know-css/)

- Allows us to:
  - Add layout/design to our pages.
  - Share those styles among specific elements and across pages.
- Here we will look at how styles are rendered, specifically:
  - How different types of selectors work.
  - How the order of those selectors can affect the rendering of the styles.
  - Properties used a lot in CSS, specifically color and length.

## [The Cascade](https://learn.shayhowe.com/html-css/getting-to-know-css/#cascade)

- In CSS all styles cascade from the top of the style sheet to the bottom.
- Different styles are added and overwritten in this process.
- Here is an example of overriding where the web-page will render as green with 24 pixel text:

```css
p {
  background: orange;
  font-size: 24px;
}
p {
  background: green;
}

```

### Cascading properties

- This also applies to properties within elements.
- Here is an example of this, where the paragraphs will render in green:
```css
p {
  background: orange;
  background: green;
}
```

## [Calculating Specificity](https://learn.shayhowe.com/html-css/getting-to-know-css/#specificity)

-  We can cause errors in the cascade by using contradictory selectors.
-  Every CSS selector has a specificity weight.
-  Its specificity weight + position in the cascade = how well it will be rendered.
-  In lesson 1 we looked at `id`, `type` and `class` selectors, each of which have a different weight.

|Selector| specifity weight | point value | example in HTML| and corresponding example in CSS
| :--- | :---: | :---: |:---: |:---: |
|`type`| lowest| `0-0-1`|`<p> ... </p>`|p {background: orange}|
|`class`| medium| `0-1-0`|`<div class=ball>;<p> ... </p> ; </div>`|`.hotdog p {background: brown;}`|
|`ID`| high | `1-0-0`| `<p id="food">...</p>` |`#food { ... }`

-  Specificity points are calculated with these three columns.
-  Specificity points are intentionally hyphenated because they are not computed using base-10 (decimal).So `class` selectors don't have a value of 10.
-  The higher the points, the more precedence they have when a style clashes with another.
-  For example is a paragraph element is styled in one place with a type selector and in another place with a ID selector, the ID selector will win, no matter where the it appears in the cascade.

```html
<p id="food">...</p>
```

```css
#food {                  /* => here is the 'ID' selector, with a higher specificity weight */
  background: green;    
}
p {                      /* => here is the 'type' selector, with a lower specificity weight. */
  background: orange;    /* => So even though `p` is read last, `#food` takes precedence and the paragraph will be green. */
}
```

## [Combining Selectors](https://learn.shayhowe.com/html-css/getting-to-know-css/#combining-selectors)

- We combine selectors to be more specific.
- So the following example is for all paragraphs, IF they are wrapped in an element of the `hotdog` class THEN turn them brown UNLESS the sub-class attribute is `mustard` in which cass turn it yellow.

```html
<div class="hotdog">
  <p>...</p>
  <p>...</p>
  <p class="mustard">...</p>
</div>

```

```css
.hotdog p {               */ here the combined selector is .hotdog p and the key selector is p /*
  background: brown;
}
.hotdog p.mustard {      */ here the combined selector is .hotdog p.mustard and the key selector is .mustard /*
  background: yellow;
}
```
- When combined, selectors are read right to left.
- The selector farthest to the right (ie, read first) is called the 'key selector'
- The 'key selector' will determine exactly which element the styles will be applied to. The other elements are 'pre-qualifiers'.
- The line `.hotdog p.mustard` targets paragraphs with a class of `mustard` wrapped in an element with the class `hotdog`.
- 

### Spaces within selectors

- `.hotdog p.mustard` why is there a space after `hotdog`, but not after `mustard` ?
- Spaces are key in selectors, so this difference important.
- The absence of a space between `p` and `.mustard` means the selector will only select paragraphs with a class of `mustard`. Without the `p` and surrounded by spaces, `mustard` would tell the selector to select everything with a `mustard` class.
- Best practice is to not prefix a class selector with a type selector. So `.hotdog .mustard.` should be enough.

### Specificity within combined selectors

- Combining selectors creates a new specificity weight. We can calculate the new specificity weight by adding together the combined weights of the elements.
- For example:
  - `.hotdog p`
  - class selector + type selector.
  - `0-1-0` + '`0-0-1`
  - = `0-1-1`
- Example 2:
  - `.hotdog p.mustard`
  - `0-1-0` + '`0-1-1`
  - = `0-2-1`
- So example 2 would take precedence even if example 1 came after example 2 in the stylesheet.
- Keep an eye on these specificity weights because the higher they get the more likely the cascade is to break.

## [Layering Styles with Multiple Classes](https://learn.shayhowe.com/html-css/getting-to-know-css/#multiple-classes)

- We can keep the specificity weight of our elements low by being as modular as possible. We do this by using multiple classes to layer on styles.
- HTML elements can have more than one class attribute value, they just need to be seperated by a space.
- In the following example we target buttons. We want the buttons to be 16px, but the background to vary depending on where they are.

```html
<a class="btn btn-danger">...</a>
<a class="btn btn-success">...</a>
```

```css
.btn {
  font-size: 16px;
}
.btn-danger {
  background: red;
}
.btn-success {
  background: green;
}
```
- Our styles here are clean and modular. This keeps specificity weights low and is best-practice.

## [Common CSS property Values](https://learn.shayhowe.com/html-css/getting-to-know-css/#css-property-values)

- We'll look at color and length here, but there are lots more.

### Colors

- CSS uses sRGB (Standard Red Green Blue), like TV and monitors. 
- There are 4 ways to write this:
  - keywords
  - hexadecimal
  - RGB
  - HSL

### Keyword Colors

- easy to rememeber, but fewer options.

|Color	Name|	Hex Values	|RGB Values|	HSL Values|
| :--- | :---: | :---: |:---: |
|black|	#000000|	rgb(0, 0, 0)|	hsl(0, 0%, 0%)|
|silver|	#c0c0c0	|rgb(192, 192, 192)|	hsl(0, 0%, 75%)|
|gray|	#808080	|rgb(128, 128, 128)|	hsl(0, 0%, 50%)|
|white|	#ffffff|	rgb(255, 255, 255)|	hsl(0, 100%, 100%)|
|maroon|	#800000	|rgb(128, 0, 0)|	hsl(0, 100%, 25%)|
|red|	#ff0000|	rgb(255, 0, 0)|	hsl(0, 100%, 50%)|
|purple|	#800080|	rgb(128, 0, 128)|	hsl(300, 100%, 25%)|
|fuchsia|	#ff00ff|	rgb(255, 0, 255)|	hsl(300, 100%, 50%)|
|green|	#008000	|rgb(0, 128, 0)|	hsl(120, 100%, 25%)|
|olive|	#808000|	rgb(128, 128, 0)|	hsl(60, 100%, 25%)|
|lime|	#00ff00|	rgb(0, 255, 0)|	hsl(120, 100%, 50%)|
|yellow|	#ffff00|	rgb(255, 255, 0)|	hsl(60, 100%, 50%)|
|navy|	#000080|	rgb(0, 0, 128)|	hsl(240, 100%, 25%)|
|blue|	#0000ff|	rgb(0, 0, 255)|	hsl(240, 100%, 50%)|
|teal|	#008080|	rgb(0, 128, 128)|	hsl(180, 100%, 25%)|
|aqua|	#00ffff|	rgb(0, 255, 255)|	hsl(180, 100%, 50%)|


- ie `red`, `green`, `blue`.

```css
.task {
  background: maroon;
}
.count {
  background: yellow;
}
```

### Hexadecimal colors

- The most popular of the 4 options
- `#` followed by 3 or 6 characters.
- The chars are 0-9, a-f and A-F.
- They form 3 columns that map to R, G and B
<img width="287" alt="Screenshot 2023-05-27 at 09 33 30" src="https://github.com/SandyRodger/LS202_html_and_css/assets/78854926/65930bc5-1204-43e6-ae7e-29e9cfd18a68">
- 0 is black, f is white.

#### The millions of Hexadecimal colors

- There are more than 16.7 million hexadecimal colours:
  - 16 options for each characer.
  - Paired characters have 256 options. 16 squared.
  - Three pairs with 256 options is 16.7 million. 256 * 256 * 256 or 256 cubed.

```css
.task {
  background: #800000;
}
.count {
  background: #ff0;
}
```

- It can be useful to use a service like [Adobe Color](https://color.adobe.com/create/color-wheel) to find the right color and then note down its RBG hex number.

### RGB and RGBa colors

- Use the `rgb()` function, which takes 3 comma seperated values of 0 - 255.
- 0 is black, 255 pure white.

```css
.task {
  background: rgb(128, 0, 0);
}
.count {
  background: rgb(255, 255, 0);
}
```
- the `rgba()` function can also be used to add a fourth value for transparency. This fourth value is between 0.0 and 1, where 0 is fully transparent.

```css
.task {
  background: rgba(128, 0, 0, .25);
}
.count {
  background: rgba(255, 255, 0, 1);
}
```

### HSL & HSLa colors

- Hue, saturation, light.
- `hsl()` function.
- Hue is a number 0 - 360 representing the degree on the colour wheel.
- Saturation is 0 - 100 % on a grey-scale.
- Lightness is 0 - 100% for white to black.

```css
.task {
  background: hsl(0, 100%, 25%);
}
.count {
  background: hsl(60, 100%, 50%);
}
```
- HSL colours can also include transparency with the `hsla()` function:
```css
.task {
  background: hsla(0, 100%, 25%, .25);
}
.count {
  background: hsla(60, 100%, 50%, 1);
}
```
- hsl is relatively new and so less commonly used.

### Lengths

- Absolute and relative.

### Absolute lengths

- Use physical measurements (ie inches, centimeters). Most popularly pixels: `px`.

### Pixels

- 1/96th inch.
- Slight variation between high-density and low-density viewing devices.
- Viewing devices are changing fast so pixels aren't as universal as they once were. But they are still the 'old faithful' of measurement.

### Relative Lengths

- rely on the measurement of other elements.

### Percentages

- Will be the % of its parent element:

```css
.col {
  width: 50%;
}
```

### Em

- 1 em is the element's font-size. 
- So you might set the width of an element to `5em`, which would be 5 times the size of the font:

```css
.banner {
  font-size: 14px;
  width: 5em;
}
```
- If the element has no explicit font size, the reader will look up the parent-chain until a parent element is found with an explicit font size.

## [Summary](https://learn.shayhowe.com/html-css/getting-to-know-css/#summary)

- How style-sheets cascade from top to bottom of a file.
- What specificity is and how to calculate it.
- Combining selectors to target specific elements/groups of elements.
- Using multiple classes on a single element to layer different stlyes of modular code.
- Different colour values in CSS.
- Different length values in CSS.
