---
marp: true
---

# CSS

- CSS stands for "Cascading Style Sheets".
- Cascading refers to the procedure that determine which style will apply to a certain section, if you have more than one style rule.
- Style refers how you want a certain part of your page to look. You can set colors, fonts, margins etc.
  for things like table, paragraphs, headings etc.

---

# Basic structure of a Style (CSS syntax)

```
                h1 {color:blue; font-size:12px;}

```

- h1 -> is a selector identifies the HTML elements you want to style.
- color:blue -> here color is the property which is a style attribute you want to change. Each property has a value here the value is blue.
- color:blue; -> this is the declaration part that includes property and value.
- {color:blue; font-size:12px;} -> this is the declaration block which contains multiple declaration including the curly braces.

---

# How to add CSS

- Inline Style
- Internal Style sheet
- External Style sheet

---

# CSS Selectors

- CSS selectors are used to select the content you want to style. Selectors are the part of CSS rule set. CSS selectors select HTML elements according to its id, class, type, attribute etc.

---

## Types of CSS Selectors:

### Simple selectors (select elements based on name, id, class)

- Id selector: The id selector uses the id attribute of an HTML element to select a specific element. To use id selector, you must use (#) followed by id name of your CSS.

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      #firstPara {
        color: green;
      }
    </style>
  </head>
  <body>
    <h1>This heading is styled with CSS.</h1>
    <p id="firstPara">Me too!</p>
    <p>And me!</p>
  </body>
</html>
```

---

- Class-selector: The class selector selects HTML elements with a specific class attribute. To use class selector, you must use (.) followed by class name of your CSS.

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      .center {
        text-align: center;
        color: blue;
      }
    </style>
  </head>
  <body>
    <h1 class="center">This heading is blue and center-aligned.</h1>
    <p class="center">This paragraph is blue and center-aligned.</p>
  </body>
</html>
```

---

### Pseudo-class selectors (select elements based on a certain state)

---

### CSS Pseudo Classes

- A Pseudo class in CSS is used to define the special state of an element.
- It can be combined with a CSS selector to add an effect to existing elements based on their states.
- For Example, changing the style of an element when the user hovers over it, or when a link is visited. All of these can be done using Pseudo Classes in CSS.

https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes

```
  Syntax

  selector: pseudo-class{
      property: value;
  }

```

---

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      /* unvisited link */
      a:link {
        color: red;
      }

      /* visited link */
      a:visited {
        color: green;
      }

      /* mouse over link */
      a:hover {
        color: hotpink;
      }

      /* selected link */
      a:active {
        color: blue;
      }
    </style>
  </head>
  <body>
    <h2>Styling a link depending on state</h2>

    <p>
      <b
        ><a href="https://skill-lync.com/" target="_blank"
          >This is a link to skill-lync website</a
        ></b
      >
    </p>
    <p>
      <b>Note:</b> a:hover MUST come after a:link and a:visited in the CSS
      definition in order to be effective.
    </p>
    <p>
      <b>Note:</b> a:active MUST come after a:hover in the CSS definition in
      order to be effective.
    </p>
  </body>
</html>
```

---

- :hover Pseudo-class: This pseudo-class is used to add special effect to an element when our mouse pointer is over it. The below example demonstrates that when your mouse enters the box area, its background color changes from yellow to orange.

https://jsbin.com/rokitinuri/1/edit?html,css,output

```html
<!DOCTYPE html>
<html>
<head>
	<title>CSS Pseudo Classes property</title>
<body>
	<h1>CSS Pseudo Classes</h1>
	<h2>:hover Pseudo-class</h2>
	<div class="box">
		My color changes if you hover over me!
	</div>
</body>
</html>
```

---

```css
.box {
  background-color: yellow;
  width: 300px;
  height: 200px;
  margin: auto;
  font-size: 40px;
  text-align: center;
}

.box:hover {
  background-color: orange;
}

h1,
h2 {
  color: green;
  text-align: center;
}
```

---

- :focus Pseudo-class: This pseudo-class is used to select an element which is currently focused by the user. It works on user input elements used in forms and is triggered as soon as the user clicks on it.
- In the following example, the background color of the input field which is currently focused changes.

https://jsbin.com/ketomotudo/1/edit?html,css,output

---

```html
<!DOCTYPE html>
<html>
  <head>
    <title>CSS Pseudo class property</title>
  </head>
  <body>
    <h1>CSS Pseudo class property</h1>
    <h2>:focus Pseudo-class</h2>
    <form>
      <label for="emailid">Email-Id:</label>
      <input type="email" name="emailid" placeholder="Enter your email-id" />

      <label for="Password">Password:</label>
      <input
        type="password"
        name="Password"
        placeholder="Enter your password"
      />
    </form>
  </body>
</html>
```

---

```css
body {
  border: 2px solid green;
}

form {
  width: 200px;
  height: 100px;
  margin: 0 auto;
  text-align: center;
  line-height: 2rem;
}

label {
  width: 30%;
}

input {
  background-color: default;
  float: right;
}

input:focus {
  background-color: grey;
}

h1,
h2 {
  color: green;
  text-align: center;
}
```

---

### Pseudo-elements selectors (select and style a part of an element)

---

### CSS Pseudo-Elements

- A CSS pseudo-element is used to style specified parts of an element.
- it can be used to:
  Style the first letter, or line, of an element
  Insert content before, or after, the content of an element
- Syntax:
  selector::pseudo-element {
  property: value;
  }

- The ::placeholder selector: selects form elements with placeholder text, and let you style the placeholder text.

- The placeholder text is set with the placeholder attribute, which specifies a hint that describes the expected value of an input field.

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      ::placeholder {
        color: blue;
      }
    </style>
  </head>
  <body>
    <p>
      Use the ::placeholder selector to change the color of the placeholder
      text:
    </p>

    <input type="text" name="fname" placeholder="First name" />
  </body>
</html>
```

---

# Google Fonts

- https://fonts.google.com
- select the font-style
- attach the css, select the @import part.
  @import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@1,100&family=Roboto:wght@300&display=swap');
- body {
  font-family: 'Poppins', sans-serif;
  }

- p {
  font-family: 'Roboto', sans-serif;
  }

---

# CSS Colors

CSS Color property is used to set the color of HTML elements. This property is used to set font color, background color etc.

```html
<html>
  <head>
    <title>CSS color property</title>
  </head>
  <body>
    <h1>CSS Colors</h1>
  </body>
</html>
```

---

Color of an element can be defined in the following ways:

- Built-In Color : These are a set of predefined colors which are used by its name. For example: red, blue, green etc.

```
Syntax :

h1 {
    color: color-name;
}
```

```
h1 {
        color:green;
    }
```

---

- RGB Format : The RGB(Red, Green, Blue) format is used to define the color of an HTML element by specifying the R, G, B values range between 0 to 255. For example: RGB value of Red color is (255, 0, 0), Green color is (0, 255, 0), Blue color is (0, 0, 255) etc.

```
Syntax:
h1 {
        color: rgb(R, G, B);
}
```

```
 h1{
        color: rgb(0, 153, 0);
    }
```

---

- RGBA Format : The RGBA format is similar to the RGB, but the difference is RGBA contains A (Alpha) which specify the transparency of elements. The value of alpha lies between 0.0 to 1.0 where 0.0. represents fully transparent and 1.0 represents not transparent.

```
Syntax:

h1 {
        color:rgba(R, G, B, A);
}

```

```
h1 {
        color:rgba(0, 153, 0, 0.5);
    }
```

---

- Hexadecimal Notation : The hexadecimal notation begins with # symbol followed by 6 characters each range from 0 to F. For example: Red #FF0000, Green #00FF00, Blue #0000FF etc.

```
Syntax:

h1 {
    color:#(0-F)(0-F)(0-F)(0-F)(0-F)(0-F);
}
```

```
h1{
    color:#009900;
}
```

- Apart from applying the color to the content of the specific element alone.

---

### CSS Text Color

It is used to set the color of the text.

```
h1 {
   color:color_name;
}
```

---

### CSS Background Color

It is used to set the background color of an HTML element.

```
h1 {
  background-color:color_name;
}
```

---

### CSS Border Color

It is used to set the border color of an element. Border-style is used to set the border type.

```
h1 {
   border-style:solid/dashed/dotted
   border-color:color_name;
}
```

---

## CSS Units

- CSS has several different units for expressing a length.
- There are two types of length units: absolute and relative.

### Absolute lengths:

- The absolute length units are fixed and a length expressed in any of these will appear as exactly that size.

- Absolute length units are not recommended for use on screen, because screen sizes vary so much.
  However, they can be used if the output medium is known, such as for print layout.
- px - pixels (1px = 1/96th of 1in)

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      h1 {
        font-size: 50px;
      }
      h2 {
        font-size: 30px;
      }
      p {
        font-size: 15px;
        line-height: 20px;
      }
    </style>
  </head>
  <body>
    <h1>This is heading 1</h1>
    <h2>This is heading 2</h2>
    <p>This is a paragraph.</p>
    <p>This is another paragraph.</p>
  </body>
</html>
```

### Relative length:

- Relative length units specify a length relative to another length property.
  Relative length units scale better between different rendering medium.

- em - Relative to the font-size of the element (2em means 2 times the size of the current font)

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      p {
        font-size: 16px;
        line-height: 2em;
      }

      div {
        font-size: 30px;
        border: 1px solid black;
      }

      span {
        font-size: 0.5em;
      }
    </style>
  </head>
  <body>
    <p>These paragraphs have a calculated line-height of: 2x16px = 32px.</p>
    <p>These paragraphs have a calculated line-height of: 2x16px = 32px.</p>
    <p>These paragraphs have a calculated line-height of: 2x16px = 32px.</p>
    <div>
      The font-size of the div element is set to 30px.
      <span
        >The span element inside the div element has a font-size of 0.5em, which
        equals to 0.5x30 = 15px</span
      >.
    </div>
  </body>
</html>
```

- rem Relative to font-size of the root element

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      html {
        font-size: 16px;
      }

      div {
        font-size: 3rem;
        border: 1px solid black;
      }

      #top-div {
        font-size: 2rem;
        border: 1px solid red;
      }
    </style>
  </head>
  <body>
    <p>The font-size of this document is 16px.</p>

    <div id="top-div">
      The font-size of this div element is 2rem, which translates to 2 x the
      browser's font size.
      <div>
        The font-size of this div element is 3rem. It also shows that it does
        not inherit from its parent element font size.
      </div>
    </div>

    <p>
      The rem unit sets the font-size relative to the browsers base font-size,
      and will not inherit from its parents.
    </p>
  </body>
</html>
```

---

# CSS Borders

CSS border properties allow us to set the style, color, and width of the border. Different properties can be set for all the different borders i.e.top border, right border, bottom border, and left border.

---

- Border style : The border-style property specifies the type of border. None of the other border properties will work without setting the border style.

Following are the types of borders:

- dotted – It describes a dotted border
- dashed – It describes a dashed border
- solid – It describes a solid border
- double – It describes a double border
- none – It describes no border
- hidden – It describes the hidden border

---

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      p.dotted {
        border-style: dotted;
      }

      p.dashed {
        border-style: dashed;
      }

      p.solid {
        border-style: solid;
      }

      p.double {
        border-style: double;
      }
    </style>
  </head>

  <body>
    <h2>The CSS border-style Property</h2>
    <p class="dotted">A dotted border.</p>
    <p class="dashed">A dashed border.</p>
    <p class="solid">A solid border.</p>
    <p class="double">A double border.</p>
  </body>
</html>
```

---

- Border-Width : Border width sets the width of the border. The width of the border can be in px, pt, cm or thin, medium and thick.

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      p {
        border-style: solid;
        border-width: 8px;
      }
    </style>
  </head>
  <body>
    <p>CSS Border-Width properties</p>
  </body>
</html>
```

---

- Border Color: This property is used to set the color of the border. Color can be set using the color name, hex value, or RGB value. If the color is not specified border inherits the color of the element itself.

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      p {
        border-style: solid;
        border-color: red;
      }
    </style>
  </head>
  <body>
    <p>CSS Border-Color properties</p>
  </body>
</html>
```

---

- Border sides: Using border property, we can provide width, style, and color to all the borders separately for that we have to give some values to all sides of the border.

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      h2 {
        border-top-style: dotted;
      }
    </style>
  </head>

  <body>
    <h2>CSS Border sides</h2>
  </body>
</html>
```

---

- Rounded Border: This property allows you to add rounded corners to elements.

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      p {
        background-color: #ffffff;
        border: 1px solid black;
        border-radius: 50px;
        padding: 5px;
        width: 250px;
      }
    </style>
  </head>
  <body>
    <h1>The border-radius Property</h1>
    <p>This is the CSS border radius property</p>
  </body>
</html>
```

---

# CSS Margins

CSS margins are used to create space around the element. We can set the different sizes of margins for individual sides(top, right, bottom, left).
Margin properties can have the following values:

- Length in cm, px, pt, etc.
- Width % of the element.
- Margin calculated by the browser: auto.

```
Syntax:

body
{
    margin: size;
}
```

---

```html
<html>
  <head>
    <style>
      p {
        border: 2px solid black;
        margin: 80px 100px 50px 80px;
        color: red;
        width: 120px;
      }
    </style>
  </head>

  <body>
    <p>Margin properties</p>
  </body>
</html>
```

---

# CSS Padding

CSS paddings are used to create space around the element, inside any defined border. We can set different paddings for individual sides(top, right, bottom, left).

Padding properties can have the following values:

- Length in cm, px, pt, etc.
- Width % of the element.

```
Syntax:

body
{
    padding: size;
}
```

---

```html
<html>
  <head>
    <style>
      p {
        border: 2px solid black;
        padding: 80px 100px 50px 80px;
        color: red;
        width: 150px;
      }
    </style>
  </head>

  <body>
    <p>Padding Properties</p>
  </body>
</html>
```

---

## Margin vs Padding

https://jsbin.com/sozugosiro/edit?html,css,output

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Margin vs Padding</title>
  </head>
  <body>
    <h4>This element has margin.</h4>
    <h3>This element has padding.</h3>
  </body>
</html>
```

---

```css
h4 {
  background-color: lime;
  margin: 50px 20px 10px 20px;
}

h3 {
  background-color: cyan;
  padding: 80px 50px 60px 110px;
}
```

---

## CSS Box-model property

- is a container that contains multiple properties including borders, margin, padding, and the content itself.
  It is used to create the design and layout of web pages.
- content: This property is used to displays the text, images, etc, that can be sized using
  the width & height property.
- padding: This property is used to create space around the element, inside any defined border.
- border: This property is used to cover the content & any padding, & also allows to set the style,
  color, and width of the border.
- margin: This property is used to create space around the element ie., around the border area.
- (padding, border, margin)

```html
<!DOCTYPE html>
<head>
	<style>
	  #box {
		padding-top: 40px;
		width: 400px;
		height: 100px;
		border: 50px solid red;
		margin: 50px;
		text-align: center;
		font-size: 32px;
		font-weight: bold;
	  }
	</style>
</head>
<body>
      <div id="box">CSS Box Model</div>
</body>
</html>
```

---

# CSS Position property

The CSS position property defines the position of an element in a document.

- static
- relative
- absolute
- fixed
- sticky

---

### static

This method of positioning is set by default. If we don’t mention the method of positioning for any element, the element has the position: static method by default. By defining Static, the top, right, bottom and left will not have any control over the element. The element will be positioned with the normal flow of the page.

https://jsbin.com/fewogujeza/1/edit?html,css,output

there's no change? This confirms the fact that the left and bottom properties do not affect an element with position: static.

---

### relative

Elements with position: relative remain in the normal flow of the document. But, unlike static elements, the left, right, top, bottom properties affect the position of the element.

https://jsbin.com/fewogujeza/2/edit?html,css,output

---

### absolute

- Elements with position: absolute are positioned relative to their parent elements. In this case, the element is removed from the normal document flow. The other elements will behave as if that element is not in the document. No space is created for the element in the page layout. The values of left, top, bottom and right determine the final position of the element.
- an element with position: absolute is positioned relative to its closest positioned ancestor. That means that the parent element has to have a position value other than position: static.
- If the closest parent element is not positioned, it is positioned relative to the next parent element that is positioned. If there's no positioned ancestor element, it is positioned relative to the <html> element.
  https://jsbin.com/zumecexeru/2/edit?html,css,output

---

### fixed

- Fixed position elements are similar to absolutely positioned elements. They are also removed from the normal flow of the document. But unlike absolutely positioned element, they are always positioned relative to the <html> element.

- fixed elements are not affected by scrolling. They always stay in the same position on the screen.

https://jsbin.com/xetugewida/3/edit?html,css,output

---

### sticky

- Element with position: sticky and top: 0 played a role between fixed & relative based on the position where it is placed.
- If the element is placed at the middle of the document then when the user scrolls the document, the sticky element starts scrolling until it touches the top. When it touches the top, it will be fixed at that place in spite of further scrolling. We can stick the element at the bottom, with the bottom property.

https://jsbin.com/xegugafeyu/1/edit?html,css,output

---

# CSS Flex Box

- CSS flexbox layout allows you to easily format HTML.
- Flexbox makes it simple to align items vertically and horizonatally using rows and columns.

---

# Flex Container

- is an element that contains items.

### Flex Container Properties

- display : defines a flex container – flex formatting context.
- flex-direction : defines the main axis inside the container.
- flex-wrap : allows flex items to wrap onto more than one line.
- justify-content : allows items to align along main axis.
- align-content : allows items to align along cross axis in a single line.
- align-items : aligns multiple lines of items on the cross axis.

https://jsbin.com/vaxosexuvo/1/edit?html,css,output

---

https://www.freecodecamp.org/news/css-flexbox-tutorial-with-cheatsheet/

- flex-direction property :

This property allows us to set the direction and orientation in which our flex-items should be distributed inside the flex-container.

- flex-wrap :

This property helps you set the number of flex-items you want in a line or row.
This works on the .container parent class.

- justify-content property :

This property arranges flex-items along the MAIN AXIS(Row-wise) inside the flex-container.

- align-content property :

This property arranges flex-items along the CROSS AXIS inside the flex-container.
This is similar to justify-content.

- align-items property :

This property distributes Flex-items along the Cross Axis(column).

---

# Flex Items

- are the immediate children in a flex container.

### Flex Items Properties

- order : allows the change of order of items without altering the source order.
- flex-grow : allows an item to fill up the available free space.
- flex-shrink : allows an item to shrink if there is no enough free space available.

https://jsbin.com/pimedabomo/1/edit?html,css,output

https://jsbin.com/tokilayezi/edit?html,css,output

---

The properties we'll discuss now will work when we resize the window.

* flex-grow : This property grows the size of a flex-item based on the width of the flex-container.

* flex-shrink : This property helps a flex item shrink based on the width of the flex-container.
It's the opposite of flex-grow.

* flex-order : allows the change of order of items without altering the source order.

---

# CSS Box-Shadow

- The box-shadow property in CSS is used to give a shadow-like effect to the frames of an element.
- The box-shadow can be described using X and Y offsets relative to the element, blur and spread radius, and color.

```
Syntax:

box-shadow: [horizontal offset] [vertical offset] [blur radius] [color];
```

---

Property Value: All the properties are described well with the example below.

- h-offset: It is required to set the position of the shadow horizontally. The positive value is used to set the shadow on the right side of the box and a negative value is used to set the shadow on the left side of the box.
- v-offset: It is required to set the position of shadow value vertically. The positive value is used to set the shadow below to the box and a negative value is used to set the shadow above the box.
- blur: It is an optional attribute, the work of this attribute is to blur the shadow of the box. The higher the number, the more blurred it will be

https://jsbin.com/qifiruceha/edit?html,css,output

---

```html
<!DOCTYPE html>
<html>
  <head>
    <title>CSS Box Shadow</title>
  </head>
  <body>
    <div id="shadow">
      <p>A div element with a shadow.</p>
    </div>
  </body>
</html>
```

```css
#shadow {
  border: 1px solid;
  margin: 30px;
  padding: 30px;
  box-shadow: 20px 20px 10px grey;
  width: 200px;
}
```

---

## CSS Overflow

- The overflow property specifies what should happen if content overflows an element's box.
- This property specifies whether to clip content or to add scrollbars when an element's content is too big to
  fit in a specified area.
- Note: The overflow property only works for block elements with a specified height.
- visible - The overflow is not clipped. It renders outside the element's box. This is default.
- hidden - The overflow is clipped, and the rest of the content will be invisible.
  Content can be scrolled programmatically (e.g. by setting scrollLeft or scrollTo())
- clip - The overflow is clipped, and the rest of the content will be invisible. Forbids scrolling,
  including programmatic scrolling.
- scroll - The overflow is clipped, but a scroll-bar is added to see the rest of the content.
- auto - If overflow is clipped, a scroll-bar should be added to see the rest of the content

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      div.ex1 {
        background-color: lightblue;
        width: 110px;
        height: 110px;
        overflow: scroll;
      }

      div.ex2 {
        background-color: lightblue;
        width: 110px;
        height: 110px;
        overflow: hidden;
      }

      div.ex3 {
        background-color: lightblue;
        width: 110px;
        height: 110px;
        overflow: auto;
      }

      div.ex4 {
        background-color: lightblue;
        width: 110px;
        height: 110px;
        overflow: clip;
      }

      div.ex5 {
        background-color: lightblue;
        width: 110px;
        height: 110px;
        overflow: visible;
      }
    </style>
  </head>
  <body>
    <h1>The overflow Property</h1>

    <p>
      The overflow property specifies whether to clip content or to add
      scrollbars when an element's content is too big to fit in a specified
      area.
    </p>

    <h2>overflow: scroll:</h2>
    <div class="ex1">
      Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy
      nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.
    </div>

    <h2>overflow: hidden:</h2>
    <div class="ex2">
      Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy
      nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.
    </div>

    <h2>overflow: auto:</h2>
    <div class="ex3">
      Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy
      nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.
    </div>

    <h2>overflow: clip:</h2>
    <div class="ex4">
      Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy
      nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.
    </div>

    <h2>overflow: visible (default):</h2>
    <div class="ex5">
      Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy
      nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.
    </div>
  </body>
</html>
```

## Overflow Wrap

- The overflow-wrap property specifies whether or not the browser can break lines with long words,
  if they overflow the container.

- normal - Long words will not break, even if they overflow the container. This is default
- anywhere - Long words will break if they overflow the container.
- break-word - Long words will break if they overflow the container

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      div {
        width: 150px;
        border: 1px solid #000000;
      }

      div.a {
        overflow-wrap: normal;
      }

      div.b {
        overflow-wrap: break-word;
      }

      div.c {
        overflow-wrap: anywhere;
      }
    </style>
  </head>
  <body>
    <h1>The overflow-wrap Property</h1>

    <h2>overflow-wrap: normal (default):</h2>
    <div class="a">
      This div contains a very long word:
      thisisaveryveryveryveryveryverylongword. The long word will not break and
      wrap to the next line.
    </div>

    <h2>overflow-wrap: break-word:</h2>
    <div class="b">
      This div contains a very long word:
      thisisaveryveryveryveryveryverylongword. The long word will break and wrap
      to the next line.
    </div>

    <h2>overflow-wrap: anywhere:</h2>
    <div class="c">
      This div contains a very long word:
      thisisaveryveryveryveryveryverylongword. The long word will break and wrap
      to the next line.
    </div>
  </body>
</html>
```

---

## Overflow-X

- The overflow-x property specifies whether to clip the content, add a scroll bar, or
  display overflow content of a block-level element, when it overflows at the left and right edges.

- visible - The overflow is not clipped. It renders outside the element's box. This is default.
- hidden - The overflow is clipped, and the rest of the content will be invisible.
  Content can be scrolled programmatically (e.g. by setting scrollLeft or scrollTo())
- clip - The overflow is clipped, and the rest of the content will be invisible. Forbids scrolling,
  including programmatic scrolling.
- scroll - The overflow is clipped, but a scroll-bar is added to see the rest of the content.
- auto - If overflow is clipped, a scroll-bar should be added to see the rest of the content.

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      div.ex1 {
        background-color: lightblue;
        width: 40px;
        overflow-x: scroll;
      }

      div.ex2 {
        background-color: lightblue;
        width: 40px;
        overflow-x: hidden;
      }

      div.ex3 {
        background-color: lightblue;
        width: 40px;
        overflow-x: auto;
      }

      div.ex4 {
        background-color: lightblue;
        width: 40px;
        overflow-x: visible;
      }
    </style>
  </head>
  <body>
    <h1>The overflow-x Property</h1>

    <p>
      The overflow-x property specifies whether to clip the content, add a
      scroll bar, or display overflow content of a block-level element, when it
      overflows at the left and right edges.
    </p>

    <h2>overflow-x: scroll:</h2>
    <div class="ex1">
      Lorem ipsum dolor sit amet, consectetuer adipiscing elit...
    </div>

    <h2>overflow-x: hidden:</h2>
    <div class="ex2">
      Lorem ipsum dolor sit amet, consectetuer adipiscing elit..
    </div>

    <h2>overflow-x: auto:</h2>
    <div class="ex3">
      Lorem ipsum dolor sit amet, consectetuer adipiscing elit...
    </div>

    <h2>overflow-x: visible (default):</h2>
    <div class="ex4">
      Lorem ipsum dolor sit amet, consectetuer adipiscing elit...
    </div>
  </body>
</html>
```

---

## Overflow-Y

- The overflow-y property specifies whether to clip the content, add a scroll bar, or
  display overflow content of a block-level element, when it overflows at the top and bottom edges.

- visible - The overflow is not clipped. It renders outside the element's box. This is default.
- hidden - The overflow is clipped, and the rest of the content will be invisible.
  Content can be scrolled programmatically (e.g. by setting scrollLeft or scrollTo())
- clip - The overflow is clipped, and the rest of the content will be invisible. Forbids scrolling,
  including programmatic scrolling.
- scroll - The overflow is clipped, but a scroll-bar is added to see the rest of the content.
- auto - If overflow is clipped, a scroll-bar should be added to see the rest of the content.

---

# CSS Outline property

- An outline is a line that is drawn around elements, outside the borders, to make the element "stand out".
- If outline-color is omitted, the color applied will be the color of the text.

- Note: Outlines differ from borders! Unlike border, the outline is drawn outside the element's border,
  and may overlap other content. Also, the outline is NOT a part of the element's dimensions;
  the element's total width and height is not affected by the width of the outline.

## Outline-Width

- The outline-width specifies the width of an outline.
- medium - Specifies a medium outline. This is default
- thin - Specifies a thin outline
- thick - Specifies a thick outline
- px range.

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      <style > h2 {
        outline-style: solid;
        outline-width: medium;
      }

      div.a {
        outline-style: solid;
        outline-width: medium;
      }

      div.b {
        border: 1px solid red;
        outline-style: solid;
        outline-width: medium;
      }
    </style>
  </head>
  <body>
    <h1>The outline-width Property</h1>

    <h2>A Heading with a medium outline</h2>

    <div class="a">A div element with a medium outline.</div>
    <br />

    <div class="b">Notice that the outline is outside of any border.</div>
  </body>
</html>
```

## Outline-Style

- The outline-style property specifies the style of an outline.
- none Specifies no outline. This is default
- hidden - Specifies a hidden outline
- dotted - Specifies a dotted outline
- dashed - Specifies a dashed outline
- solid - Specifies a solid outline

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      p {
        border: 1px solid red;
      }
      p.a {
        outline-style: dotted;
      }
      p.b {
        outline-style: dashed;
      }
      p.c {
        outline-style: solid;
      }
      p.d {
        outline-style: double;
      }
      p.e {
        outline-style: groove;
      }
      p.f {
        outline-style: ridge;
      }
      p.g {
        outline-style: inset;
      }
      p.h {
        outline-style: outset;
      }
    </style>
  </head>
  <body>
    <h1>The outline-style Property</h1>

    <p class="a">A dotted outline</p>
    <p class="b">A dashed outline</p>
    <p class="c">A solid outline</p>
    <p class="d">A double outline</p>
    <p class="e">A groove outline</p>
    <p class="f">A ridge outline</p>
    <p class="g">An inset outline</p>
    <p class="h">An outset outline</p>
  </body>
</html>
```

---

## Outline-color

- The outline-color property specifies the color of an outline.
- Specifies the color of the outline.

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      h2 {
        outline-style: solid;
        outline-color: #92a8d1;
      }

      div.a {
        outline-style: solid;
        outline-color: #92a8d1;
      }

      div.b {
        border: 1px solid black;
        outline-style: solid;
        outline-color: #92a8d1;
      }
    </style>
  </head>
  <body>
    <h1>The outline-color Property</h1>

    <h2>A heading with a colored outline</h2>

    <div class="a">
      The outline-color can be specified with a hexadecimal value.
    </div>
    <br />

    <div class="b">Notice that the outline is outside of any border.</div>

    <p>
      <strong>Note:</strong> The outline-color property does not work if it is
      used alone. Use the outline-style property to set the outline first.
    </p>
  </body>
</html>
```

---

## Outline-offset

- The outline-offset property adds space between the outline and the edge or border of an element.
- The space between an element and its outline is transparent.
- length - The distance the outline is outset from the border edge. Default value is 0

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      div.ex1 {
        margin: 20px;
        border: 1px solid black;
        background-color: yellow;
        outline: 4px solid red;
        outline-offset: 15px;
      }

      div.ex2 {
        margin: 10px;
        border: 1px solid black;
        background-color: yellow;
        outline: 5px dashed blue;
        outline-offset: 5px;
      }
    </style>
  </head>
  <body>
    <h1>The outline-offset Property</h1>

    <div class="ex1">
      This div has a 4 pixels solid red outline 15 pixels outside the border
      edge.
    </div>
    <br />

    <div class="ex2">
      This div has a 5 pixels dashed blue outline 5 pixels outside the border
      edge.
    </div>
  </body>
</html>
```

---

## CSS outline-shorthand property

- The outline property is a shorthand property for:
- outline-width
  outline-style (required)
  outline-color

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      h2 {
        border: 1px solid red;
        outline: 5px dotted green;
      }

      div.a {
        border: 1px solid red;
        outline: 2px dashed blue;
      }
    </style>
  </head>
  <body>
    <h1>The outline Property</h1>

    <h2>A Heading with a 5 pixels green dotted outline</h2>

    <div class="a">
      A div element with a 2 pixels blue dashed outline. Also notice that the
      outline is outside of any border.
    </div>
  </body>
</html>
```

---
## Task : Create a user card using CSS
