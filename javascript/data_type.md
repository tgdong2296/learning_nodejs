# Data Type

**Mọi thứ trong Javascript đều là object**

## Premitive data types (Kiểu dữ liệu nguyên thủy)

- **String**
  - Integer
  - Float
- **Number**
- **Boolean**
- **undefined:** biến được khai báo nhưng chưa được assign giá trị.
- **null:** null trong Javascript có nghĩa là empty value hoặc không có value.
- **Symbol:** giá trị duy nhất được khởi tạo bởi Symbol constructor

### Note

- Sau khi premitive data type được khởi tạo, chúng ta sẽ không thể modifine chúng.

```javascript
let word = 'JavaScript'
word[0] = 'Y' // throw error
```

- Premitive data type có thể compare value (==).

## Non-Premitive data types

- Object
- Array

### Note

- Sau khi non-premitive data type được khởi tạo, chúng ta có thể sửa đổi chúng.

```javascript
let nums = [1, 2, 3]
nums[0] = 10
```

- Non-premitive data type không thể comapre value (==) vì với các non-premitive thì javascript đang thực hiện so sánh reference thay vì so sánh value. Hai object được coi là bằng nhau nếu chúng cùng trỏ tới một instance.

## Checking Data Type

Để kiểm tra kiểu dữ liệu của mọt property, ta sử dụng `typeof`.

``` javascript
console.log(typeof 'Asabeneh') // string
console.log(typeof 5) // number
console.log(typeof true) // boolean
console.log(typeof null) // object type
console.log(typeof undefined) // undefined
```

## Khai báo biến (Declare variables)

Để khai báo một biến trong Javascript, ta sử dụng từ khóa `let`, `var`, `const`.

- `let`: khai báo các biến có thể thay đổi giá trị
- `const`: khai báo các hằng số không thể thay đổi giá trị sau khi đã được khởi tạo
