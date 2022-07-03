# HTML Part 2

## Table of Contents

- [We Know HTML Now What?](#afterhtml)
- [What Is CSS](#css)
- [How To Write CSS Code?](#writecss)
- [What Is JavaScript](#javascript)
- [How To Write JavaScript Code To Add Interactivity?](#interactivejs)
- [References](#references)

## <a name="afterhtml"></a> We Know HTML Now What?

As we have seen before HTML is used to define a webpage's structure. If we design websites only with HTML we will have something that can only display text. So how can we make it so that it is pleasing to look at? and how can we make it so that users can interact with our website?

We do that by using CSS and JavaScript!

## <a name="css"></a> What Is CSS ?

CSS stands for Cascading Style Sheet. It is a design language that makes websites look more appealing that just plain text. It is used to layout the visuals, and aesthetics of a webpage.

For instance if we have a simple HTML page like this:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My Webpage</title>
  </head>
  <body>
    <h1>Heading</h1>
    <p>Paragraph</p>
  </body>
</html>
```

If you render this code in the browser you would get something like this:

<div style="background-color: #fff; padding: 1rem; color: #333; border: 1px solid #000;">
<h1 style="border: none">Heading</h1>
<p>Paragraph</p>
</div>

And this isn't all that great. What if our website's color scheme included a nice green color? Well we can change all of that with CSS!

After applying the CSS magic we would get this:

<div style="background-color: #CDEAC0; padding: 1rem; color: #333; border: 1px solid #000;">
<h1 style="border: none">Heading</h1>
<p>Paragraph</p>
</div>

## <a name="writecss"></a> How To Write CSS Code?

Writing CSS code is very simple. A CSS rule consists of a `selector` and a `declaration` block.

Let's talk about the aforementioned terms individually:

- `selector` : A selector is something which CSS can use to _"select"_ something so that it can apply style to it. It can be an HTML tag name, a class attribute, an id attribute etc.
- `declaration block` : A declaration block is a block in which you write CSS rules that will be applied to the selector.

Let us look at an example. Let's say we want to change the text-color of paragraph elements and make their font-size 20 pixels. In order to do that we can write the following CSS code:

```css
p {
  color: "red";
  font-size: 20px;
}
```

In the above code `p` is our selector and everything between the two curly brackets is the declaration block. As you can see each property inside the declaration block has to be separated by semicolons.

## <a name="javascript"></a> What Is JavaScript?

JavaScript was created to add some interactivity to webpage or in other words, to make them _"alive"_. JavaScript is not a compiled language and is very different from _Java_ even though it may look like it has some connection to Java.

JavaScript was originally called _LiveScript_ but because Java was very popular at the time so it was decided that positioning a new language as a _"younger brother"_ of Java would help.

Today, JavaScript can execute not only in a browser, but also on the server using something called NodeJS. It's safe to say that if you want to work with the web, one way or the other you will have to use JavaScript if you want to add any interactivity to your webpage.

What does it mean when we say _"add interactivity to the webpage"_? It means that a user can come to a website and interact with it, like they would click a button and something would pop up. You can define your own complex actions using JavaScript.

## <a name="interactivejs"></a> How To Write JavaScript Code To Add Interactivity?

Let's say you want to build a very simple web application that would keep track of how many times a user has clicked on a specific button. Now if we break this application down to smaller parts, this is what we would need:

- A button element to the application.
- An element that would display the number of time the user has clicked on the button.
- A way to increase the count every time a user clicks on the button.

Adding a button and an element that contains the counter can be done using just HTML. Let's look at what the code will look like.

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My Application</title>
  </head>
  <body>
    <h1>Click Count</h1>
    <p>0</p>
    <button>Click Me!</button>
  </body>
</html>
```

As you can see the HTML code is pretty basic we have 3 elements that make up our entire application.

Right now if we click on out button nothing will happen to the counter because it is a static HTML page. So how can we make if so that if we click on the button the text above the button changes? Well, we can do that using JavaScript!

First, let's modify our HTML code to add id's to both, the button and the counter element so it will be easy for JavaScript to grab them.

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My Application</title>
  </head>
  <body>
    <h1>Click Count</h1>
    <p id="counter">0</p>
    <button id="click">Click Me!</button>
  </body>
</html>
```

You can give it any id but make sure to assign an id that makes sense to you.

Now let's look at what the JavaScript code will look like:

```js
let counterElement = document.getElementById("counter");
let button = document.getElementById("click");
let counter = 0;

button.addEventListener("click", function () {
  counter = counter + 1;
  counterElement.textContent = counter;
});
```

And that's it! This is all the JavaScript you need to make an application that tracks how many times a user has clicked on a button.

Now let's take that JavaScript code apart and talk about each individual parts

- `let counterElement` : This is called a variable in JavaScript. A variable is something that holds a value. It can be any value. In this case it is holding the counter element as a value.
  - You can create a variable in JavaScript using the `let` keyword.
- `document` : document here refers to the entire webpage that you can see in the browser.
- `getElementById("idName")` : This is a function that grabs an element that matches the id provided.
- `addEventListener(type, action)` : This is how you can attach event listeners to anything. An event listener is something that listens to an event and does something if that type of event is fired. In our example we were saying that _"I want to attach a click event listener to my button. Once the click event is fired, I want the counter to be updated."_

Our final application code will look like this

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My Application</title>
    <script defer>
      let counterElement = document.getElementById("counter");
      let button = document.getElementById("click");
      let counter = 0;

      button.addEventListener("click", function () {
        counter = counter + 1;
        counterElement.textContent = counter;
      });
    </script>
  </head>
  <body>
    <h1>Click Count</h1>
    <p id="counter">0</p>
    <button id="click">Click Me!</button>
  </body>
</html>
```

And there you have it! You have created your first web application!

## <a name="references"></a> References

- [CSS Introduction](https://www.w3schools.com/css/css_intro.asp) - Introduction to CSS by W3Schools.
- [Introduction To JavaScript](https://javascript.info/intro) - An excellent resource to learn JavaScript.
- [JavaScript Algorithms and Data Structures](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/) - Another excellent resource to learn JavaScript.
