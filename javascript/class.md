```js
class Fruit {
  constructor(price, name, img) {

  }

  discount() {
  }

  renderFruitDetail() {}
}


class FruitList {
  constructor() {
    this.fruitList = [];

    this.fetchFruits();
  }

  fetchFruits() {
    //xhr call
  }

  renderList() {
  }
}

const fruitList = new FruitList();
fruitList.renderList();

```
---


```cs
 .fruit {
        display: block;
        box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
        list-style: none;
        margin-bottom: 10px;
        max-width: 400px;
      }

      .fruit-content {
        display: flex;
        justify-content: space-around;
        padding: 5px 0;
      }
```

```js
console.clear();

class Fruit {
  constructor(price, name, img) {
    this.name = name;
    this.price = price;
    this.img = img;
  }

  discount() {
    return this.price - 10;
  }

  renderFruitDetail() {}
}

const fruits = [
  new Fruit(
    10,
    "mango",
    "https://images.unsplash.com/photo-1568702846914-96b305d2aaeb?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80"
  ),
  new Fruit(
    100,
    "apple",
    "https://images.unsplash.com/photo-1582655299221-2b6bff351df0?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80"
  )
];

class FruitList {
  constructor() {
    this.fruitList = [];

    this.fetchFruits();
  }

  fetchFruits() {
    //xhr call
    this.fruitList = fruits;
  }

  renderList() {
    const wrapper = document.querySelector("#app");
    const parentEl = document.createElement("ul");

    for (const fruit of this.fruitList) {
      const fruitEl = document.createElement("li");
      fruitEl.className = "fruit";

      fruitEl.innerHTML = `
        <img src="${fruit.img}"/>
        <div class="fruit-content">
          <div> <strong>Name</strong> : ${fruit.name} </div>
          <div> <strong>Price</strong> : ${fruit.price} </div>
        </div>
        <br/>
    `;

      parentEl.append(fruitEl);
    }

    wrapper.append(parentEl);
  }
}

const fruitList = new FruitList();
fruitList.renderList();

```
