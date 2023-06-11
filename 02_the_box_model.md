# [The Box Model](https://launchschool.com/lessons/f039db62/assignments)

## [Introduction](https://launchschool.com/lessons/f039db62/assignments/70151955)

- In this lesson we will look at:
  - Different types of display objects
  - Dimensions / spacing
  - The box model
- Testing and Validation: In the last lesson LS nudged us to do this. Now we have to build up the habit for ourselves.
- The following steps should become 2nd nature:
  - Update your code
  - Test the results ion the browser
  - Validate your HTML
  - Validate your CSS
  - Check your work on other browsers (don't wait till the end of your project for this)
  - Repeat

### What to focus on

- The CSS box model, which browsers use to construct a web-page. 
  - It's a crucial concept.
  - Go through this lesson multiple times.
  - Learn what to expect from your browser when it processes your html/css, and how that depends on:
    - The visual display model
    - box-sizing model
    - box properties

#### Vocabulary

- The box model
  - box properties
    - width and height
    - padding and margins
    - borders
  - visual display models
    - `block`
    - `inline`
    - `inline-block`
  - Box sizing model
    - `content-box`
    - `border box`
  - Dimensions
    - absolute units
    - relative units
- Also
  - container
  - physical pixels
  - CSS reference pixels

#### Box Properties

- Every box has
  - width
  - height
  - padding
  - margins
  - border
- Padding, margins, border have top, bottom, left, right
- How does the visual display model interact with margins borders and padding?

#### Visual Display Models

- Understand the difference between `inline`, `block` and `inline-block`.
- Containers are almost always block elements, non-containers are almost always `inline`. When in doubt check MDN.
- Don't try to memorize which elements are block or inline.
- How/when do you change an element's visual display model.

#### Box Sizing Models

- Understand the `content-box` and `border-box` sizing models.
- How and when can you change the box-sizing model for an element?

#### Dimensions

- Know the difference between `px`, `rem`, `em`, `%` and `auto`.
- Underdstand physical pixels v CSS reference pixels.
- Use `auto` margins to center block elements horizontally.

#### HTML

- Don't try and memorize the new HTML elements.

#### CSS

- Become comfortable with and memorize the following CSS properties:
  - `border`
  - `display`
  - `box-sizing`
  - `width`
  - `height`
  - `padding`
  - `margin`

#### Try the examples

- Don't just copy and paste the examples.
- After you're done, play around, try and break them, see what happens.

#### Using documentation

- This lesson will have new CSS/HTML which won't be explained - you have to look it up.
- For example, you might have to change the appearance of a list.

#### Study from the Summary

- This is a list of things you should have mastered by the end of the course.

## [Everything is a box](https://launchschool.com/lessons/f039db62/assignments/cee8258b)

- Browsers render HTML the same way that a word processor reads letters from left to right and then wraps around to start again.
- Each line reads objects that start on the same horizontal plain.
- These objects (referred to here as "elements") can be many things, including:
  - images
  - media players
  - containers
- The browser renders a web page one object at a time:
  - It sees each objects and determines how much vertical and horizontal space it needs to draw it.
  - It calculates the required dimentions using:
    -  the browser defaults
    -  your CSS.
  - If there's enough horizontal space left in the line, it puts it there, if not it wraps around.
  - Each line uses enough vertical space to contain all its boxes.
  - This process repeats for every box on the page.
- The most important take-aways from this are:
  - Every element requires a box shaped segment on the page.
  - Every character of text content also requires a boxed portion of the page.
  - The browser calculates the dimensions of the box usisng your browser defaults and your CSS.
- BUT there's more than one way to determine a box` size. It's perhaps the most important concept in HTML/CSS so be sure to grock it.

### Widths and heights

- The browser displays `inline-block` elements side by side up to the page width.
- So the same elements would be displayed as follows on two browsers of differing widths:

<img width="901" alt="Screenshot 2023-06-08 at 10 37 25" src="https://github.com/SandyRodger/LS202_html_and_css/assets/78854926/8148713f-4e41-434c-9dce-08e454035c1b">

### Box Properties

- Every element has the following properties (possibly ignored by the browser), even if they are set to 0:
  - Width/height (may/may not include padding and borders) 
    - in the example below 928 pixels wide and 168 high.
  - Padding: The area surrounding the content area, seperating the contetnt from its border. Normally opaque, concealing anything benath it.
    - in the example below 10 pixels each of top and bottom padding plus 20 pixels each of left and right padding,
  - Border: surrounds the padding.
    - in the example below the border is 1 px thick.
  - Margin: A transparent area outside the border and seperating the elements.
    - In the example below, a 28-pixel bottom margin (the left, right, and top margins are 0).
  - The display property: tells the browser how to lay out an element relative to its neighbours.

<img width="253" alt="Screenshot 2023-06-08 at 10 44 27" src="https://github.com/SandyRodger/LS202_html_and_css/assets/78854926/03c9e0d8-3706-45c4-bff7-e6c031be8bdd">


## [The Visual Formatting Model](https://launchschool.com/lessons/f039db62/assignments/b7312e44)

- The previous example assumed that the boxes have the property of `inline-block`. But there are more than 24 `display` values and each one complicates the browser's job a lot more.
- The top 3 are:
  - `block`
  - `inline-block` 
  - `inline`

### Block elements

- [Block elements](https://developer.mozilla.org/en-US/docs/Glossary/Block-level_content) appear on almost all web pages
- You can have blocks within blocks.
-  Some examples of block elements:
  - Headings
  - Headers (`h1` to `h6`)
  - Footers
  - Blockquote
  - `ul`, `ol` and `dl`.
  - 'figure' and 'figcaption'.
  - 'form' and 'fieldset' 
  - Paragraphs
  - Sections
  - Article
  - Aside
  - tables
  - forms
  - lists
- Every block is a container that organises the elements within itself.
- The master container is the `body` element.
- This relationship can be described as parent/child. Containers can be ancestors, descendents, siblings,cousins etc.
- By default block elements take up the whole row. The rest of the line will just be blank. So 3 block elements will stack on top of each other. They are therefore predictable and easy to use.
- Block elements use normal box properties to determine the size of the element. The browser reserves this space on the page and this is where it draws the content. 
- For example if an element is:
  - 928 px wide
  - 168 pdx high
  - 20 px padding on each side
  - 10 px padding top and bottom
  - 1 px border
  - 28 px bottom margin
- ... the overall dimensions will be (928 + 20 + 20 + 1 + 1) 970px X (168 + 10 + 10 + 1 + 1 + 28) 218 px. (This example assumes browser default settigs).
- Any element can be a block element with the `display: block` css property. It's common to do this with `a` and `img` elements.

#### Some finicky notes about width and height

- `w/h MAY INCLUDE `padding` and `border`.
- By default w/h exclude the `padding` and `border` from the measured content area. This is covered more in the 'box-sizing' chapter.
- h/w values never include the margins.

### Inline elements

- Provide a small piece of semantic meaning to an element. Browsers use these to make a small change in how they display the element.

## [Box Sizing](
## [Practice Problems: The Box Model](
## [Padding and Margins](
## [Dimensions](
## [Practice Problems: Spacing and Dimensions](
## [Summary](
## [Quiz 2](
## Overview

|  | Once | Twice | Thrice | Got it?
| :--- | :---: | :---: | :---: | :--- |
|1. Introduction| 1/06/23 ||||
|2	Everything is a box|
|3 The Visual Formatting Model|
|4 Box Sizing|
|5 Practice Problems: The Box Model|
|6 Padding and Margins|
|7 Dimensions|
|8 Practice Problems: Spacing and Dimensions|
|9 Summary|
|10 Quiz 2|
