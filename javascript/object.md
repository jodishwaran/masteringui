# **Object**

## Object Creation:

### 1. Object literal form :
`var obj = {
  name: "ganesh",
  age: 11,
  x: true,
  address: {
    zip: 1111
  }
};`


**Update property** <br>
`obj.age = 12;` 

**Add property** <br>
`obj.y = "some value";` <br>

**Read property** <br>
`console.log(obj.age);` <br>
`console.log(obj["age"]);`

**Delete property** <br>
`delete obj.name;`

`console.log(obj.name);`