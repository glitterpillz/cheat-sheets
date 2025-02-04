# 🎈 JAVASCRIPT METHODS - CHEAT SHEET


## 🔢 Arrays

```javascript
[1, 2, 3].length;   // 3
[1, 2, 3].push(4);  // 4
[1, 2, 3].unshift(0);   // 4
[1, 2, 3].pop();    // 3
[1, 2, 3].shift();  // 1
[1, 2, 3].at(2);    // 3
[1, 2, 3].indexOf(3);   // 2
[1, 2, 3].includes(3);  // true
[1, 2, 3].map((num) => num * 2);    // [2, 4, 6]
[1, 2, 3].filter((num) => num > 1); // [2, 3]
[1, 2, 3].every((num) => num > 0);  // true
[1, 2, 3].some((num) => num > 2);   // true
[1, 2, 3].fill(0);  // [0, 0, 0]
[1, 2, 3].reduce((acc, num) => acc + num, 0);   // 6
[1, 2, 3].concat([4, 5]);   // [1, 2, 3, 4, 5]
[1, 2, 3].reverse() // [3, 2, 1]
[3, 2, 1].sort();   // [1, 2, 3]
[1, 2, 3].join("-");    // "1-2-3"
[1, 2, 3].flat();   // [1, 2, 3]
[1, 2, 3].find((num) => num === 1); // 1
[1, 2, 3].findIndex((num) => num === 2);    // 1
[1, 2, 3].toString();   // "1,2,3"
[1, 2, 3].toLocaleString(); // "1,2,3"
[1, 2, 3].slice(1, 2);  // [2]
[1, 2, 3].splice(1, 1, "a");    // returns: [2] / mutated array: [1, "a", 3]
Array.isArray([1, 2, 3]);   // true
Array.from("123");  // ['1', '2', '3']
```


## 🧵 Strings

```javascript
"JavaScript".length();  // 10
"JavaScript"[2];    // "v"
"JavaScript".charAt(2); // "v"
"JavaScript".charCodeAt(2); // 118
"JavaScript".indexOf("S");  // 4
"JavaScript".toLowerCase(); // "javascript"
"JavaScript".tpUpperCase(); // "JAVASCRIPT"
"JavaScript".slice(2, 5);   // "vaS"
"JavaScript".substring(2, 5);   // "vaS"
"JavaScript".substr(2, 2);  // "va"
"JavaScript".concat(" Dev");    // "JavaScript Dev"
```


## 📆 Date Methods

### Initialization

```javascript
new Date();    // 2025-02-04T17:35:15.072Z
new Date(1738690410256);   // 2025-02-04T17:33:30.256Z
new Date("2025-01-30");    // 2025-01-30T00:00:00.000Z
new Date("2025-01-30T01:10:00");   // 2025-01-30T06:10:00.000Z
new Date(2025, 1, 30, 1, 10, 0, 0);    // 2025-03-02T06:10:00.000Z
// year, month, day, hour, min, sec, misc
```

### Conversions

```javascript
date.toString();   // Tue Feb 04 2025 12:33:30 GMT-0500 (Eastern Standard Time)
date.toDateString();   // Tue Feb 04 2025
date.toTimeString();   // 12:33:30 GMT-0500 (Eastern Standard Time)
date.toISOString();    // 2025-02-04T17:33:30.256Z
date.toLocaleString(; // 2/4/2025, 12:33:30 PM
date.toLocaleDateString()); // 2/4/2025
date.toLocaleTimeString(); // 12:33:30 PM
date.getTime();    // 1738690410256
```

### Get Methods

```javascript
date.getFullYear();    // 2025
date.getMonth();   // 1
date.getDate();    // 4
date.getDay(); // 2
date.getHours();   // 12
date.getMinutes(); // 39
date.getSeconds(); // 30
date.getMilliseconds();    // 831
date.getTime();    // 1738690770831
date.getTimezoneOffset();  // 300
```

### Set Methods

```javascript
date.setFullYear(2025);    // 1738691023214
date.setMonth(1);  // 1738691023214
date.setDate(25);  // 1740505423214
date.setHours(10); // 1740498223214
date.setMinutes(20);   // 1740496843214
date.setSeconds(20);   // 1740496820214
date.setMilliseconds(20);  // 1740496820020
date.setTime(1740496820020)    // 1740496820020
```


## 📄 DOM Methods

### Accessing Elements

```javascript
document.getElementById("id");  // find element by id
document.getElementsByClassName("class");   // find elements by class
document.getElementByTagName("tag");    // find elements by tag name
document.querySelector("selector"); // find first element matching selector
document.querySelectorAll("selector");  // find all elements matching selector
```

### Creating/Appending Elements

```javascript
document.createElement("name"); // create element node
document.createTextNode("text");    // create text node
elem.appendChild(child);    // append child to element
elem.removeChild(child);    // remove child from element
elem.replaceChild(newChild, oldChild);  // replace child with new child
```

### Modifying Elements

```javascript
elem.innerHTML = "<h2>outerHTML</h2>";  // set HTML
elem.innerText = "inner text";  // set inner text
elem.textContent = "text content"   // set text content
elem.style.color = "pink";  // set style
elem.outerHTML = "<p>Coding with Karen</p>";    // replace HTML
```

### Accessing Parent, Children, Siblings

```javascript
elem.parentElement; // access parent element
elem.children;  // access element children
elem.firstElement;  // access first child
elem.lastElementChild;  // access last child
elem.nextElementSibling;    // access next sibling
elem.previousElementSibling;    // access previous sibling
```

### Modifying Attributes

```javascript
elem.getAttribute("attr");  // get attribute value
elem.setAttribute("attr", "value"); // set attribute value
elem.removeAttribute("attr");   // remove attribute
```

### Modifying Element Classes

```javascript
elem.classList.add("my-class"); // add class
elem.classList.remove("my-class");  // remove class
elem.classList.toggle("my-class");  // toggle class
elem.classList.contains("my-class")l    // check for class
```


## 🎡 DOM Events

### Event Listeners

```javascript
document.addEventListener('click', (event) => {
    console.log('Click Event', event);
});

// unregister event listener:
document.removeEventListener('click', (event) => {
    console.log('Unregistered Event', event);
});
```

| KeyBoard Events | |
| --------------- | --- |
| **keydown** | key is pressed down |
| **keyup** | key is released |

-

| Form Events | |
| ----------- | --- |
| **blur** | element has lose focused
| **change** | use modified value of input, select, or textarea |
| **focus** | element has received focus |
| **select** | text has been selected in an element |
| **submit** | fires on form when submitted |
| **reset** | fires on form is reset |

-

| Mouse Events | |
| ------------ | --- |
| **click** | left mouse button click |
| **dbclick** | left mouse button double click |
| **mousedown** | pointing device button is pressed when inside element |
| **mouseup** | mouse button released over an element |
| **mouseover** | mouse button enter an element |
| **mousemove** | mouse pointer moves over on element |

-

| Window Events | |
| ------------- | --- |
| **abort** | resource was not full loaded, but not due to an error |
| **error** | error event occurs if resource failed to load or can't be used |
| **load** | document has finished loading |
| **unload** | document has being unloaded |
| **scroll** | document is scrolled |
| **resize** | window is resized |