# Function

## Function Declaration

```javascript
//declaring a function without a parameter
function functionName() {
  // code goes here
}
functionName() // calling function by its name and with parentheses
```

## Function returning value

```javascript
function addTwoNumbers() {
    let numOne = 2
    let numTwo = 3      
    let total = numOne + numTwo
    return total
}
```

## Function with a parameter

### One param

```javascript
// function with one parameter
function functionName(parm1) {
  //code goes her
}
functionName(parm1) // during calling or invoking one argument needed
```

### Two param

```javascript
// function with two parameters
function functionName(parm1, parm2) {
  //code goes her
}
functionName(parm1, parm2) // during calling or invoking two arguments needed
```

### Many parameters

```javascript
// function with multiple parameters
function functionName(parm1, parm2, parm3,...){
  //code goes here
}
functionName(parm1,parm2,parm3,...) // during calling or invoking three arguments needed
```

### Unlimited parameters

Mỗi regular function sẽ có `arguments` object là một array chứa các parameters đầu vào.

```javascript
function sumAllNums() {
  let sum = 0
  for (let i = 0; i < arguments.length; i++) {
    sum += arguments[i]
  }
  return sum
}

console.log(sumAllNums(1, 2, 3, 4)) // 10
console.log(sumAllNums(10, 20, 13, 40, 10))  // 93
console.log(sumAllNums(15, 20, 30, 25, 10, 33, 40))  // 173
```

Arrow function không có `arguments` object. Thay vào đó, nó sẽ sử dụng spread operator `...`.

```javascript
const sumAllNums = (...args) => {
 console.log(args)
}

sumAllNums(1, 2, 3, 4) // [1, 2, 3, 4]
```

### Default parameter

```javascript
function greetings(name = 'Peter') {
  let message = `${name}, welcome to 30 Days Of JavaScript!`
  return message
}

console.log(greetings())
console.log(greetings('Asabeneh'))
```

## Anonymous function

Là function không có tên.

```javascript
const anonymousFun = function() {
  console.log(
    'I am an anonymous function and my value is stored in anonymousFun'
  )
}
```

## Expression function

Expression function là Anonymous function. Sau khi tạo ra một anonymous function, ta sẽ gán nó vào một biến. 
Để lấy output của function ta cần phải gọi tới biến đó.

```javascript
// Function expression
const square = function(n) {
  return n * n
}
square(2) // -> 4
```

## Self invoking function

Self invoking function là anonymous function nhưng ta không cần gọi tới nó để lấy output.

```javascript
(function(n) {
  console.log(n * n)
})(2) // 4, but instead of just printing if we want to return and store the data, we do as shown below

let squaredNum = (function(n) {
  return n * n
})(10)

console.log(squaredNum)
```

## Arrow function

Arrow function sử dụng `=>` thay cho keyword `function` để khai báo.

```javascript
function square(n) {
  return n * n
}

const square = n => {
  return n * n
}

const square = n => n * n
```
