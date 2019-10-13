# What-I-Learned-In-Week-5
### DOM Manipulation
Use JS to manipulate the HTML and CSS in a web page.
```
const dinoUrl = 'http://sample.com/abcd.jpg'

const list = document.querySelector('ul')
list.style.backgroundImage = `url(${dinoUrl})`
```

We can create an element and append it to the existing HTML.
```
const footer = document.createElement('h3');
footer.style.color = 'red';
footer.innerText = 'I am the footer.';

const wrappingDiv = document.querySelector('#app');
wrappingDiv.appendChild(footer);

footer.id = 'red-footer';
```

`inner.HTML` is BAD!

---
### Ugly Query
We practiced how to alter the CSS by using JS only. The biggest challenge for me was trying to target specific elements.

---
### Notes
DRY - Don't Repeat Yourself

WET - Write Everything Twice

AHA - Avoid Hasty Abstractions

Instead of having multiple lines of the same code, you can create a function to make it less dry.
```
const item = document.querySelector('#item-1');
addDinoBG(item)
const item2 = document.querySelector('#item-2');
addDinoBG(item)

function addDinoBG(element) {
    element.style.backgroundImage = './dino/jpg';
}
```

Search a certain element and add the dino bg.
```
function addDinoBGToTag(tagName) {
    const element = document.querySelector(tagName);
    element.style.backgroundImage = './dino.gif';
}

addDinoBGToTag('h1');
```

Function Hoisting - JS moves all the functions to the top and scans.

Application Programming Interface (API) - the code you write in JS is talking to another collection of code.
