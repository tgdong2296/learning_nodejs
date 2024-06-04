# Class

- Class là một Object Constructor, có chứa các property và method.
- Class được sử dụng để định nghĩa các thuộc tính (attribute) và hành vi (behavior) của Object.

## Define Class

```javascript
// syntax
class ClassName {
    //  code goes here
}
```

**Example**

```javascript
class Person {
  // code goes here
}
const person = new Person()
```

## Constructor

Constructor là một builtin function chịu trách nghiệm khởi tạo một Object từ Class.

```javascript
class Person {
  constructor(firstName, lastName) {
    console.log(this) // Check the output from here
    this.firstName = firstName
    this.lastName = lastName
  }
}

const person = new Person()
console.log(person) // Person {firstName: undefined, lastName:undefined}

const person1 = new Person('Asabeneh', 'Yetayeh')
console.log(person1) // Person {firstName: "Asabeneh", lastName: "Yetayeh"}
```

**Default value**

```javascript
class Person {
  constructor(
    firstName = 'Asabeneh',
    lastName = 'Yetayeh',
    age = 250,
    country = 'Finland',
    city = 'Helsinki'
  ) {
    this.firstName = firstName
    this.lastName = lastName
    this.age = age
    this.country = country
    this.city = city
    this.score = 0
    this.skills = []
  }
}

// it will take the default values
const person1 = new Person() // Person {firstName: "Asabeneh", lastName: "Yetayeh", age: 250, country: "Finland", city: "Helsinki", score: 0, skills: []}
```

## Method

Method là một Javascript function nằm bên trong Class.

```javascript
class Person {
  constructor(firstName, lastName, age, country, city) {
    this.firstName = firstName
    this.lastName = lastName
    this.age = age
    this.country = country
    this.city = city
  }

  getFullName() {
    const fullName = this.firstName + ' ' + this.lastName
    return fullName
  }
}

// call function
const person1 = new Person('Asabeneh', 'Yetayeh', 250, 'Finland', 'Helsinki')
person1.getFullName() // Asabeneh Yetayeh
```

## Getter

Getter là method cho phép truy xuất các value của object.

```javascript
class Person {
  constructor(firstName, lastName, age, country, city) {
    this.firstName = firstName
    this.lastName = lastName
    this.age = age
    this.country = country
    this.city = city
    this.score = 0
    this.skills = []
  }
  getFullName() {
    const fullName = this.firstName + ' ' + this.lastName
    return fullName
  }
  get getScore() {
    return this.score
  }
  get getSkills() {
    return this.skills
  }
}
```

## Setter

Setter là method cho phép sửa đổi value của property trong Object.

```javascript
class Person {
  constructor(firstName, lastName, age, country, city) {
    this.firstName = firstName
    this.lastName = lastName
    this.age = age
    this.country = country
    this.city = city
    this.score = 0
    this.skills = []
  }
  getFullName() {
    const fullName = this.firstName + ' ' + this.lastName
    return fullName
  }
  get getScore() {
    return this.score
  }
  get getSkills() {
    return this.skills
  }
  set setScore(score) {
    this.score += score
  }
  set setSkill(skill) {
    this.skills.push(skill)
  }
}
```

## Kế thừa (inheritance)

- Một class kế thừa sẽ được thừa hưởng toàn bộ property và method của class cha.
- Từ khoá `super()` được sử dụng để refer tới parent class.
- Khi call `super()` method trong constructor, sub-class đang họi tới parent constructor và access được vào toàn bộ property cùng method của class cha.

```javascript
class Car {
  constructor(brand) {
    this.carname = brand;
  }
  present() {
    return 'I have a ' + this.carname;
  }
}

class Model extends Car {
  constructor(brand, mod) {
    super(brand);
    this.model = mod;
  }
  show() {
    return this.present() + ', it is a ' + this.model;
  }
}
```
