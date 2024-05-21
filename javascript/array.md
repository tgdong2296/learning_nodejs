# Array

- Array sử dụng để lưu trữ nhiều value.
- Mỗi value trong array có một index, mỗi index đều có một reference tới một memory address.
- Dữ liệu được truy xuất thông qua index.
- Các element trong Array có thể có kiểu dữ liệu khác nhau.

## Create an empty array

```javascript
const arr = Array()
const arr = []

const eightEmptyValues = Array(8) // it creates eight empty values
console.log(eightEmptyValues) // [ <8 empty items> ]
```

## Create array with value

```javascript
const numbers = [0, 3.14, 9.81, 37, 98.6, 100]
const fruits = ['banana', 'orange', 'mango', 'lemon']

const eight0values = Array(8).fill(0) // it creates eight element values filled with '0'
console.log(eight0values) // [0, 0, 0, 0, 0, 0, 0, 0]
```

## Array có thể chứa các element khác kiểu dữ liệu

```javascript
const arr = [
    'Asabeneh',
    250,
    true,
    { country: 'Finland', city: 'Helsinki' },
    { skills: ['HTML', 'CSS', 'JS', 'React'] }
]
```

## Operators

- `indexOf`: kiểm tra item có trong array hay không. Nếu có, return index của value, nếu không return -1.

    ```javascript
    const numbers = [1, 2, 3, 4, 5]

    console.log(numbers.indexOf(5)) // -> 4
    console.log(numbers.indexOf(0)) // -> -1
    ```

- `lastIndexOf`: trả về index cuối cùng của một item trong array. Nếu có, return index của value, nếu không return -1.

    ```javascript
    const numbers = [1, 2, 3, 4, 5, 3, 1, 2]

    console.log(numbers.lastIndexOf(2)) // 7
    console.log(numbers.lastIndexOf(0)) // -1
    ```

- `includes`: kiểm tra một item có trong array hay không.

    ```javascript
    const numbers = [1, 2, 3, 4, 5]

    console.log(numbers.includes(5)) // true
    console.log(numbers.includes(0)) // false
    ```

- `Array.isArray`: kiểm tra kiểu dữ liệu của một biến xem có phải array hay không.

    ```javascript
    const numbers = [1, 2, 3, 4, 5]
    console.log(Array.isArray(numbers)) // true

    const number = 100
    console.log(Array.isArray(number)) // false
    ```

- `push`: add item vào cuối array

    ```javascript
    const arr  = ['item1', 'item2','item3']
    arr.push('new item')
    ```

- `pop`: remove item cuối cùng

    ```javascript
    const numbers = [1, 2, 3, 4, 5]
    numbers.pop()
    ```

- `shift`: remove item đầu tiên

    ```javascript
    const numbers = [1, 2, 3, 4, 5]
    numbers.shift()
    ```

- `unshift`: add item vào đầu array

    ```javascript
    const numbers = [1, 2, 3, 4, 5]
    numbers.unshift(0)
    ```

- `reverse`: đảo chiều sắp xếp của array

    ```javascript
    const numbers = [1, 2, 3, 4, 5]
    numbers.reverse()
    ```
