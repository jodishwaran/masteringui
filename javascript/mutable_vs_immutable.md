
https://codesandbox.io/s/bold-hopper-rie8d?file=/src/index.js

## Primitives are pass by value and immutable (when value is updated, the latest value is stored in memory locaation and the previous memory location is not used and will be garbage collected)

`var x = 10; <br>
var y = true;<br>

var z = x;
x = 11;

console.log(z);` // 10



## Objects are pass by referrence (address is passed around, not value) and mutable (we can update the same reference (memory) without creating new memory location)
`
var a = { age: 1 };
var b = a;
var c = b;

a.age = 2;
console.log(c);  // {age : 2}

a = {age: 3};
console.log(c);  // {age : 2}
console.log(a);  // {age : 3}

`