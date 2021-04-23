# **Object**

## Object Creation:

### 1. Object literal form :

```js
var obj = { name: "ganesh", age: 11, x: true, address: { zip: 1111 } };
```

**Update property**:

```js
obj.age = 12;
```

**Add property**:

```js
obj.y = "some value";
```

**Read property**:

```js
console.log(obj.age);
console.log(obj["age"]);
```

**Delete property**:

```js
delete obj.name;
console.log(obj.name);
```

## Object iteration:

### using for in

```js
const object = { age: 10, name: "madhur", salary: 300 };

for (const property in object) {
  console.log(`${property}: ${object[property]}`);
}
```

### using for of

```js
const object = { age: 10, name: "madhur", salary: 300 };

for (const [property, value] of Object.entries(object)) {
  console.log(`${property}: ${value}`);
}
```

### using forEach

```js
const obj = { name: "madhur", age: 12 };
Object.entries(obj).forEach(([key, value]) => console.log(`${key}: ${value}`)); // "name: madhur", "age: 12"
```
