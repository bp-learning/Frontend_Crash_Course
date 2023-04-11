---
marp: true
---

# What is DOM

- The Document Object Model (DOM) is the data representation of the objects that comprise the
  structure and content of a document on the web.

- The Document Object Model (DOM) is a programming interface for web documents.
  It represents the page so that programs can change the document structure, style, and content.
  The DOM represents the document as nodes and objects; that way, programming languages can interact with the page.

- A web page is a document that can be either displayed in the browser window or as the HTML source.
  In both cases, it is the same document but the Document Object Model (DOM) representation allows it to be manipulated.
  As an object-oriented representation of the web page, it can be modified with a scripting language such as JavaScript.

---

- DOM stands for Document Object Model. It is a programming interface that allows us to create, change,
  or remove elements from the document. We can also add events to these elements to make our page more dynamic.

  The DOM views an HTML document as a tree of nodes. A node represents an HTML element.

- The HTML DOM is a standard object model and programming interface for HTML. It defines:

  - The HTML elements as objects
  - The properties of all HTML elements
  - The methods to access all HTML elements
  - The events for all HTML elements

  The HTML DOM is a standard for how to get, change, add, or delete HTML elements.

---

# DOM Programming Interface

- The HTML DOM can be accessed with JavaScript (and with other programming languages).
  In the DOM, all HTML elements are defined as objects.
  The programming interface is the properties and methods of each object.
  A property is a value that you can get or set (like changing the content of an HTML element).
  A method is an action you can do (like add or deleting an HTML element).

- ```html
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <meta charset="UTF-8" />
      <meta name="viewport" content="width=device-width, initial-scale=1.0" />
      <meta http-equiv="X-UA-Compatible" content="ie=edge" />
      <title>DOM tree structure</title>
    </head>
    <body>
      <h1>DOM tree structure</h1>
      <h2>Learn about the DOM</h2>
    </body>
  </html>
  ```

- Our document is called the root node and contains one child node which is the <html> element.
  The <html> element contains two children which are the <head> and <body> elements.
  Both <head> and <body> elements have children of their own.
  We can access these elements in the document and make changes to them using JavaScript.

---

# DOM Methods To Select Element In The Document

- There are different methods for selecting an element in the HTML document.

## getElementById()

- In HTML, ids are used as unique identifiers for the HTML elements.
  This means you cannot have the same id name for two different elements.

  ```html
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <meta charset="UTF-8" />
      <meta name="viewport" content="width=device-width, initial-scale=1.0" />
      <meta http-equiv="X-UA-Compatible" content="ie=edge" />
      <title>DOM tree structure</title>
    </head>
    <body>
      <h1>DOM tree structure</h1>
      <h2>Learn about the DOM</h2>
      <p id="para1">This is my first paragraph.</p>
      <p id="para2">This is my second paragraph.</p>
    </body>
  </html>

  #Javascript const paragraph1 = document.getElementById("para1");
  console.log(paragraph1); // This code tells the computer to get the element
  with the id of 'para1' and print the element to the console. // Which would
  print the below line.

  <p id="para1">This is my first paragraph.</p>

  // If we wanted to just read the content of the paragraph, then we can use the
  textContent property inside the console.log() const paragraph1 =
  document.getElementById("para1"); console.log(paragraph1.textContent); //
  Which would print the below line. "This is my first paragraph."
  ```

## querySelector()

- You can use this method to find elements with one or more CSS selectors.
- The querySelector() method returns the first element that matches a CSS selector.

```
            <!DOCTYPE html>
            <html lang="en">
            <head>
                <meta charset="UTF-8">
                <meta name="viewport" content="width=device-width, initial-scale=1.0">
                <meta http-equiv="X-UA-Compatible" content="ie=edge">
                <title>DOM tree structure</title>
            </head>
            <body>
                <h1>Favorite TV shows</h1>
                <ul class="list">
                <li>Golden Girls</li>
                <li>Archer</li>
                <li>Rick and Morty</li>
                <li>The Crown</li>
                </ul>
            </body>
            </html>
```

- To print to the console the h1 element, I could use that tag name inside the querySelector().

```
    const h1Element = document.querySelector("h1");
    console.log(h1Element);
    // The above would print.
    <h1>Favorite TV shows</h1>

```

- To target the class="list" to print out the unordered list to the console, then I would use .list
  inside the querySelector().

- The "." before list tells the computer to target a class name.
  If you wanted to target an id then you would use a # symbol before the name.

```
    const list = document.querySelector(".list");
    console.log(list);
    // The above would print.
        <ul class="list">
            <li>Golden Girls</li>
            <li>Archer</li>
            <li>Rick and Morty</li>
            <li>The Crown</li>
        </ul>
```

---

# DOM Property To Access and Update Content In The Document

## innerHTML

- To Get or set the HTML content of an element and textContent Get or set the text content of an
  element properties can be used to access or update content.

- ```html
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <meta charset="UTF-8" />
      <meta name="viewport" content="width=device-width, initial-scale=1.0" />
      <meta http-equiv="X-UA-Compatible" content="ie=edge" />
      <title>DOM tree structure</title>
    </head>
    <body>
      <h1 id="myP">I have not changed.</h1>
    </body>
  </html>
  ```

- To get the HTML content of an element with id="myP"

- ```javascript
  let html = document.getElementById("myP").innerHTML;
  ```

- To change the HTML content of an element with id="myP"

- ```javascript
  document.getElementById("myP").innerHTML = "I have changed!";
  ```

- To delete the HTML content of a <p> element with id="myP":

- ```javascript
  document.getElementById("myP").innerHTML = "";
  ```

## classList

- The classList property returns the CSS classnames of an element.
- The classList property returns a DOMTokenList.
- The classList property is read-only, but you can use the methods listed below, to add, toggle or
  remove CSS classes from the list:

- ```
      Syntax:
              element.classList
  ```

## To Add Css Styles

```html
<!DOCTYPE html>
<html>
  <style>
    .myStyle {
      background-color: coral;
      padding: 16px;
    }
    .anotherClass {
      text-align: center;
      font-size: 25px;
    }
    .thirdClass {
      text-transform: uppercase;
    }
  </style>

  <body>
    <h1>The DOMToken Object</h1>
    <h2>The add() Method</h2>

    <button onclick="myFunction()">Add</button>
    <p>Click "Add" to add multiple classes to myDIV.</p>

    <div id="myDIV">
      <p>I am myDIV.</p>
    </div>

    <p>
      The classList property is not supported in Internet Explorer 9 and
      earlier.
    </p>

    <script>
      function myFunction() {
        document
          .getElementById("myDIV")
          .classList.add("myStyle", "anotherClass", "thirdClass");
      }
    </script>
  </body>
</html>
```

## To Remove a style

```html
<!DOCTYPE html>
<html>
  <style>
    .myStyle {
      background-color: coral;
      padding: 16px;
    }
    .anotherClass {
      text-align: center;
      font-size: 25px;
    }
    .thirdClass {
      text-transform: uppercase;
    }
  </style>

  <body>
    <h1>The DOMToken Object</h1>
    <h2>The remove() Method</h2>

    <button onclick="myFunction()">Remove</button>
    <p>Click "Remove" to remove multiple classes from myDIV.</p>

    <div id="myDIV" class="myStyle anotherClass thirdClass">
      <p>I am myDIV.</p>
    </div>

    <p>
      The classList property is not supported in Internet Explorer 9 and
      earlier.
    </p>

    <script>
      function myFunction() {
        document
          .getElementById("myDIV")
          .classList.remove("myStyle", "anotherClass", "thirdClass");
      }
    </script>
  </body>
</html>
```

## To check whether a style is applied or not.

```html
<!DOCTYPE html>
<html>
  <style>
    .myStyle {
      background-color: coral;
      padding: 16px;
    }
    .anotherClass {
      text-align: center;
      font-size: 25px;
    }
    .thirdClass {
      text-transform: uppercase;
    }
  </style>

  <body>
    <h1>The DOMToken Object</h1>
    <h2>The contains() Method</h2>

    <div id="myDIV" class="myStyle anotherClass thirdClass">
      <p>I am myDIV.</p>
    </div>

    <p>Does the "myDIV" element have a class of "myStyle"?</p>
    <p id="demo"></p>

    <script>
      let x = document.getElementById("myDIV").classList.contains("myStyle");
      document.getElementById("demo").innerHTML = x;
    </script>
  </body>
</html>
```

## style

- The Style object represents an individual style statement.

```html
<!DOCTYPE html>
<html>
  <body>
    <h1 id="myH1">How to change the style of a header</h1>

    <p>Click the button to change the style of the H1 element.</p>

    <button onclick="myFunction()">Try it</button>

    <script>
      function myFunction() {
        document.getElementById("myH1").style.color = "red";
      }
    </script>
  </body>
</html>
```

---

# Adding New Elements To The Document

## createElement()

- We can first create an <ul> element using document.createElement().
  Then will assign that to a variable called unorderedList.

  ```html
  // Initially our page looks like.
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <meta charset="UTF-8" />
      <meta name="viewport" content="width=device-width, initial-scale=1.0" />
      <meta http-equiv="X-UA-Compatible" content="ie=edge" />
      <title>DOM tree structure</title>
    </head>
    <body>
      <h1>Reasons We like pets:</h1>
    </body>
  </html>

  let unorderedList = document.createElement("ul");
  ```

- Then we need to add that <ul> element to the document using the appendChild() method.

  ```javascript
  document.body.appendChild(unorderedList);
  ```

- The next part is to add a couple of <li> elements inside the <ul> element using the
  createElement() method.

  ```javascript
  let listItem1 = document.createElement("li");
  let listItem2 = document.createElement("li");
  ```

- Then we can use the textContent property to add the text for our list items.

  ```javascript
  listItem1.textContent = "They are cute.";
  listItem2.textContent = "They are friendly.";
  ```

- The last part is to use the appendChild() method so the list items can be added to the unordered list.

  ```javascript
  unorderedList.appendChild(listItem1);
  unorderedList.appendChild(listItem2);
  ```

## appendChild()

- The appendChild() method appends a node (element) as the last child of an element.

- ```
      Syntax:
          element.appendChild(node)
              OR
          node.appendChild(node)
  ```

- To create a paragraph with a text. + Create a paragraph element

```
    ` const para = document.createElement("p");` + Create a text node
    ` const node = document.createTextNode("This is a paragraph.");` + Append the text node to the paragraph
    ` para.appendChild(node);` + Append the paragraph to the document.
    ` document.getElementById("myDIV").appendChild(para);`
```

---

- ```html
  <!DOCTYPE html>
  <html>
    <body>
      <h1>The Element Object</h1>
      <h2>The appendChild() Method</h2>

      <p>Click "Append" create a paragraph and append it to myDIV:</p>

      <button onclick="myFunction()">Append</button>

      <div id="myDIV">
        <h2>I am myDIV</h2>
      </div>

      <script>
        function myFunction() {
          // Create a p element:
          const para = document.createElement("p");

          // Create a text node:
          const node = document.createTextNode("This is a paragraph.");

          // Append text node to the p element:
          para.appendChild(node);

          // Append the p element to the body:
          document.getElementById("myDIV").appendChild(para);
        }
      </script>
    </body>
  </html>
  ```

# Events In DOM Objects

## The addEventListener() method

- This method attaches an event handler to an element.

- This method sets up a function that will be called whenever the specified event is delivered to
  the target.

- ```
  Syntax:
      document.addEventListener(event, function)
  ```
- On the occurence of the event, the function gets called automatically.

- ```html
  <!DOCTYPE html>
  <html>
    <body>
      <h1>The Document Object</h1>
      <h2>The addEventListener() Method</h2>

      <p>This example adds many events on the document.</p>

      <p id="demo"></p>

      <script>
        document.addEventListener("mouseover", myFunction);
        document.addEventListener("click", mySecondFunction);
        document.addEventListener("mouseout", myThirdFunction);

        function myFunction() {
          document.getElementById("demo").innerHTML = "Moused over!";
        }

        function mySecondFunction() {
          document.getElementById("demo").innerHTML = "Clicked!<br>";
        }

        function myThirdFunction() {
          document.getElementById("demo").innerHTML = "Moused out!<br>";
        }
      </script>
    </body>
  </html>
  ```

## The preventDefault() method

- This method cancels the event if it is cancelable, meaning that the default action that belongs to the event will not occur.

- The preventDefault() method does not prevent further propagation of an event through the DOM.

- ```html
  <!DOCTYPE html>
  <html>
    <body>
      Try to check this box: <input type="checkbox" id="myCheckbox" />

      <p>
        Toggling a checkbox is the default action of clicking on a checkbox. The
        preventDefault() method prevents this from happening.
      </p>

      <script>
        document
          .getElementById("myCheckbox")
          .addEventListener("click", function (event) {
            event.preventDefault();
          });
      </script>
    </body>
  </html>
  ```
