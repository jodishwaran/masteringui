# **Scopes**

*var* keywords creates 2 scopes:
1. Global scope
2. Function scope


Watch out below for global scope variable (*a* and *b*) and local scope variable (*b*) created by *var* and not using *var* keyword in non strict mode

```js 

var a = 1;
var b;

function someFun(b) { <br>
    b = "some randome string"; // local variable update
    c = "some randome string"; // oops! created global variable in non strict mode
}

someFun(a);

console.log(a);
console.log(c);
```


## **Lexical scoping in action**

```js 

//Global scope 
var b = 1;

function someFun() {
  //someFun scope

  // var b = 10;

  var someM = function () {
    //someM scope
    
    console.log(b);  // 1
  };

  someM();
}

someFun();
```