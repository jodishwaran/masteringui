# **Variables**

## Declare variable:

1. var
2. let (only available from es6)
3. const (only available from es6)

## Using _var_ keyword:

```js
var age; //declare first without value (by default undefined will be assigned)
age = 10; //assign value after declartion above
var name = "ganesh"; //declare and assign value
```

Notice that variables declared using _var_ keyword does not create block scope. WHen we say block we are referring code between {}. var keyword only creates global and function scope. So variables created inside any block like _if_, _for_, _while_ can be accessed outside!

```js
if (true) {
  var declaredInside =
    "I am declared inside if block but can be accessed outside this block";
}

console.log(declaredInside); // we can access !!
```

```js
for (var i = 0; i < 2; i++) {
  //do nothing
}

console.log(i); // we can access "i" !!
```

```js
for (var j = 0; j < 5; j++) {
  setTimeout(() => {
    console.log("printing j: ", j);
  }, 100);
}
```
