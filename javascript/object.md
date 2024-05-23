# Object

## Global & Local scope

- Mọi thứ được khai báo nếu không sử dụng các keyword `let`, `var`, `const` sẽ có scope thuộc Global Level.

### Window Global Object

- Code example được viết trong file `scope.js`
- `a` và `b` là 2 biến thuộc window global object

    ```javascript
    //scope.js
    a = 'JavaScript' // declaring a variable without let or const make it available in window object and this found anywhere
    b = 10 // this is a global scope variable and found in the window object
    function letsLearnScope() {
    console.log(a, b)
    if (true) {
        console.log(a, b)
    }
    }
    console.log(a, b) // accessible
    ```

### Global scope

- Code example được viết trong file `scope.js`
- `a` và `b` là 2 biến global và có thể access từ mọi nơi trong file

    ```javascript
    //scope.js
    //scope.js
    let a = 'JavaScript' // is a global scope it will be found anywhere in this file
    let b = 10 // is a global scope it will be found anywhere in this file
    function letsLearnScope() {
    console.log(a, b) // JavaScript 10, accessible
    if (true) {
        let a = 'Python'
        let b = 100
        console.log(a, b) // Python 100
    }
    console.log(a, b)
    }
    letsLearnScope()
    console.log(a, b) // JavaScript 10, accessible
    ```

### Local scope

- Biến được khai báo local chỉ có tác dụng trong phạm vi của block code nó được khai báo

    ```javascript
    //scope.js
    let a = 'JavaScript' // is a global scope it will be found anywhere in this file
    let b = 10 // is a global scope it will be found anywhere in this file
    // Function scope
    function letsLearnScope() {
    console.log(a, b) // JavaScript 10, accessible
    let value = false
    // block scope
    if (true) {
        // we can access from the function and outside the function but 
        // variables declared inside the if will not be accessed outside the if block
        let a = 'Python'
        let b = 20
        let c = 30
        let d = 40
        value = !value
        console.log(a, b, c, value) // Python 20 30 true
    }
    // we can not access c because c's scope is only the if block
    console.log(a, b, value) // JavaScript 10 true
    }
    letsLearnScope()
    console.log(a, b) // JavaScript 10, accessible
    ```

## Object

### Common

- Object là một cặp `key`/`value`.
- Các `Key` của Object không có thứ tự sắp xếp.

### Khởi tạo Object

#### Khởi tạo Object Empty

```javascript
const person = {}
```

#### Khởi tạo Object với các giá trị

```javascript
const person = {
  firstName: 'Asabeneh',
  lastName: 'Yetayeh',
  age: 250,
  country: 'Finland',
  city: 'Helsinki',
  skills: [
    'HTML',
    'CSS',
    'JavaScript',
    'React',
    'Node',
    'MongoDB',
    'Python',
    'D3.js'
  ],
  getFullName: function() {
    return `${this.firstName}${this.lastName}`
  },
  'phone number': '+3584545454545'
}
```

### Truy xuất dữ liệu trong Object

- Truy xuất trực tiếp thông qua các property
  
    ```javascript
    console.log(person.firstName)
    console.log(person.lastName)
    console.log(person.age)
    console.log(person.location) // undefined
    ```

- Truy xuất thông qua `Key`

    ```javascript
    console.log(person['firstName'])
    console.log(person['lastName'])
    console.log(person['age'])
    console.log(person['age'])
    console.log(person['location']) // undefined

    // for instance to access the phone number we only use the square bracket method
    console.log(person['phone number']) 
    ```

### Object method

Method của Object là một function được lưu trữ trong một property.

```javascript
const person = {
  firstName: "John",
  lastName : "Doe",
  id       : 5566,
  fullName : function() {
    return this.firstName + " " + this.lastName;
  }
}
```

### Add new Key for an object

Object là một mutable data strcuture, vậy nên chúng ta có thể modify object sau khi nó được khởi tạo.

```javascript
const person = {
  firstName: 'Asabeneh',
  lastName: 'Yetayeh',
  age: 250,
  country: 'Finland',
  city: 'Helsinki',
  skills: [
    'HTML',
    'CSS',
    'JavaScript',
    'React',
    'Node',
    'MongoDB',
    'Python',
    'D3.js'
  ],
  getFullName: function() {
    return `${this.firstName} ${this.lastName}`
  }
}
person.nationality = 'Ethiopian'
person.country = 'Finland'
```
