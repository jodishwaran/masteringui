# **DOM Manipulation:**

## Access DOM Element:

```html
<html>
  <body>
    <p id="app" class="hello"></p>
    <p class="hello"></p>

    <div id="main"></div>

    <script>
      document.getElementById("app").innerHTML = "Hello World!";
    </script>
  </body>
</html>
```

```js
document.getElementById("app").innerHTML = "Hello World!";
document.getElementsByClassName("hello")[0].innerHTML = "Hello World!";
document.querySelector("#main").innerHTML = "Hello World!";
document.querySelectorAll(".hello").innerHTML = "Hello World!";
```
---

```js
console.clear();

const wrapper = document.getElementById("app");

const divEl = document.createElement("div");
divEl.className = "box";
divEl.innerHTML = `

<p> Hello world</p>

`;

wrapper.append(divEl);
```
---
## Create an Element:

```html
<html>
  <body>
    <style>
      .fruit {
        display: block;
        list-style: none;
        border: 1px solid rgb(53, 43, 43);
        padding: 4px;
        margin-bottom: 10px;
      }
    </style>
    <div id="main"></div>
  </body>
</html>
```

```js
const fruits = [
  { name: "apple", price: 100, description: "some text" },
  { name: "orange", price: 40, description: "some fruit text" },
  { name: "mango", price: 70, description: "some more text" },
];

const mainEl = document.querySelector("#main");
const listParentEl = document.createElement("ul");

for (const fruit of fruits) {
  const listEl = document.createElement("li");
  listEl.className = "fruit";
  listEl.innerHTML = `
        <div> <strong>Name</strong> : ${fruit.name} </div>
        <div> <strong>Price</strong> : ${fruit.price} </div>
        <div> <strong>Description</strong> : ${fruit.description} </div>
        <br/>
    `;
  listParentEl.append(listEl);
}
mainEl.append(listParentEl);
```


