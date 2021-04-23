# Arrays

## Array Creation:

```js
let arr = [1, 2, 3];

let arr = new Array("1", "2", "3"); // not preferable as its not simple, and slow compared to first one
```

## Add:

```js
let arr = [];
arr.push(1); // mutable
let newArr = arr.concat("apple"); // immutable , newArr = ["apple"]
```

## Read:

```js
let arr = [1];
console.log(arr[0]); // 1
```

## **splice** can be used to remove, replace or add elements (mutable! be careful, avoid if possible)

### add using splice

`splice(start, deleteCount, item1, item2, itemN)` // only _start_ is mandatory

```js
const fruits = ["apple", "banana", "mango"];
fruits.splice(1, 0, "orange"); // inserts at index 1
console.log(fruits); // ["apple", "orange", "banana", "mango"]
```

### remove using splice

```js
const fruits = ["apple", "banana", "mango"];
fruits.splice(1, 1); // removes one item at index 1
console.log(fruits); // ["apple", "mango"]
```

### replace using splice

`slice(start, end) //arguments are optional`

```js
const fruits = ["apple", "banana", "mango"];
fruits.splice(1, 1, "orange"); // removes one item at index 1 and inserts at index 1
console.log(fruits); // ["apple", "orange", "mango"]
```

## Array slicing using _slice_ (immutable)

```js
const animals = ["dog", "cat", "horse", "tiger", "lion"];
console.log(animals.slice(2)); // ["horse", "tiger", "lion"]
console.log(animals.slice(2, 4)); // ["horse", "tiger"]
console.log(animals.slice(1, 5)); // ["cat", "horse", "tiger", "lion"]
console.log(animals.slice()); // ["dog", "cat", "horse", "tiger", "lion"]
```

### iteration

```js
const fruits = ["apple", "banana", "mango"];

// for loop
for(let i =0; i<fruits.length; i++;){
    console.log(fruits[i]);
}

// for each
fruits.forEach(function(item, i){
    console.log(item);
})

// for of
for(const item of fruits){
    console.log(item);
}
```

## modify each element in array (map)

```js
const fruits = ["apple", "banana", "mango"];

const upperCaseFruits = fruits.map((item) => {
  return item.toUpperCase();
});

console.log(upperCaseFruits); // ["APPLE", "BANANA", "MANGO"]
```

## filter items in array (filter)

```js
const numbers = [1, 2, 3, 4, 5, 6];

const even = fruits.filter((item) => {
  return item % 2 == 0;
});

console.log(even); // [2, 4, 6]
```

## reduce elements to single value in array (reduce)

```js
const numbers = [1, 2, 3, 4, 5, 6];

const sum = numbers.reduce((acc, next) => {
  return acc + next;
}, 0);

console.log(sum); // 21
```

## check if any elements satisfy condition(some)

```js
const numbers = [1, 2, 3, 4, 5, 6];

const result = numbers.some((item) => {
  return item > 3;
}, 0);

console.log(result); // true
```

```js
const numbers = [1, 2, 3, 4, 5, 6];

const result = numbers.some((item) => {
  return item < -3;
}, 0);

console.log(result); // false
```

## check if all elements satisfy condition(some)

```js
const numbers = [1, 2, 3, 4, 5, 6];

const result = numbers.every((item) => {
  return item % 2 == 0;
});

console.log(result); // false
```

```js
const numbers = [2, 4, 6];

const result = numbers.every((item) => {
  return item % 2 == 0;
});

console.log(result); // true
```
