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

|  | Once | Twice | Thrice | Got it?
| :--- | :---: | :---: | :---: | :--- |
|1. Welcome| 18/5/23 |||50%|
|2	Introduction|	22/5/22 |||50%|
|3	Install Software|	22/5/22 | ||50%|
|4	Getting Started|22/5/22 | ||50%|
|5	Creating an HTML Skeleton|27/5/22 	| ||%|
|6	Classes, IDs, and Names|		| ||%|
|7	Practice Problems: Semantics|		| ||%|
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
