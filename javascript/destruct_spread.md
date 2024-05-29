# Destruct & Spread

## Destruct

### Destruct Array

Destruct là việc lấy các value trong array, object và asign nó vào một biến mới.

```javascript
const numbers = [1, 2, 3]

let [numOne, numTwo, numThree] = numbers

let [numOne, , numThree] = numbers // 2 is omitted
```

Lấy tất cả value trong Array

```javascript
const nums = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

let [num1, num2, num3, ...rest] = nums

console.log(num1, num2, num3) // 1 2 3
console.log(rest) // [4, 5, 6, 7, 8, 9, 10]
```

Có thể sử dụng default value nếu value undefined

```javascript
const names = [undefined, 'Brook', 'David']
let [
  firstPerson = 'Asabeneh',
  secondPerson,
  thirdPerson,
  fourthPerson = 'John'
] = names
console.log(firstPerson, secondPerson, thirdPerson, fourthPerson) // Asabeneh Brook David John
```

### Destruct Object

Để có thể destruct object, các biến phải được khai báo với tên trong với tên key của object.

```javascript
const rectangle = {
  width: 20,
  height: 10,
  area: 200
}
let { width, height, area, perimeter } = rectangle // 20 10 200 undefined
```

### Có thể đặt tên khác cho biến khi destruct object

```javascript
const rectangle = {
  width: 20,
  height: 10,
  area: 200
}
let { width: w, height: h, area: a, perimeter: p } = rectangle

console.log(w, h, a, p) // 20 10 200 undefined
```

### Gán giá trị default trong trường hợp biến undefined

```javascript
const rectangle = {
  width: 20,
  height: 10,
  area: 200
}
let { width, height, area, perimeter = 60 } = rectangle
```

### Sử dụng parameter destruct với object

```javascript
const rect = {
  width: 20,
  height: 10
}

const calculatePerimeter = ({ width, height }) => {
  return 2 * (width + height)
}

console.log(calculatePerimeter(rect)) // 60
```

## Spread

Spread Operator (Rest Operator) được sử dụng với ba dấu chấm liên tiếp nhau `...`. Dùng để khai báo sẽ lấy toàn bộ dữ liệu của array hoặc object.

### Get value array

```javascript
const nums = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
let [num1, num2, num3, ...rest] = nums
```

### Copy array

```javascript
const evens = [0, 2, 4, 6, 8, 10]
const evenNumbers = [...evens]
```

### Copy object

```javascript
const user = {
  name:'Asabeneh',
  title:'Programmer',
  country:'Finland',
  city:'Helsinki'
}

const copiedUser = {...user}
```

### Modify object khi copy

```javascript
const user = {
  name:'Asabeneh',
  title:'Programmer',
  country:'Finland',
  city:'Helsinki'
}

const copiedUser = {...user, title:'instructor'}
```
