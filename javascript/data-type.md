# **Data Types**


### Declare **string**
`var name = "some string";`

### Declare **number**
`var x = 100;`
`var pi = 3.142;`
`var someFraction = 3/5;`

### Declare **boolean**
`var enabled = false;`

### Declare **null**
`var name = null;`

### Declare **Undefined**
`var name = undefined;`

### **Gotchas**
`var n = 0.1 + 0.2;`

`console.log(n);` // 0.30000000000004

`console.log(Math.floor(0.3));` // 0
`console.log(Math.ceil(0.3));` // 1
`console.log(Number.parseFloat(n).toFixed(1));` // 0.3
