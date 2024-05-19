# Boolean & Conditions

## Truthly values

Các giá trị dược coi là `true`:

- Tất cả các `number` khác 0 (bao gồm cả số âm) đều là `true`
- Tất cả các `string` không empty đều là `true`
- `Boolean` có value `true`

## Falsy values

Các giá trị được coi là `false`:

- 0
- 0n
- null
- undefined
- NaN
- Boolean `false`
- Empty string

## Compare

- `==`: so sánh **giá trị**
- `===`: so sánh **giá trị** và **kiểu dữ liệu**

```javascript
console.log(3 == 2)             // false, because 3 is not equal to 2
console.log(3 != 2)             // true, because 3 is not equal to 2
console.log(3 == '3')           // true, compare only value
console.log(3 === '3')          // false, compare both value and data type
console.log(3 !== '3')          // true, compare both value and data type
console.log(3 != 3)             // false, compare only value
console.log(3 !== 3)            // false, compare both value and data type
console.log(0 == false)         // true, equivalent
console.log(0 === false)        // false, not exactly the same
console.log(0 == '')            // true, equivalent
console.log(0 == ' ')           // true, equivalent
console.log(0 === '')           // false, not exactly the same
console.log(1 == true)          // true, equivalent
console.log(1 === true)         // false, not exactly the same
console.log(undefined == null)  // true
console.log(undefined === null) // false
console.log(NaN == NaN)         // false, not equal
console.log(NaN === NaN)        // false
```

## `if` condition

```javascript
// syntax
if (condition) {
  // this part of code runs for truthy condition
} else {
  // this part of code runs for false condition
}

// syntax
if (condition) {
     // code
} else if (condition) {
   // code
} else {
    //  code
}
```

## `switch` condition

```javascript
switch(caseValue){
  case 1:
    // code
    break
  case 2:
   // code
   break
  case 3:
   // code
   break
  default:
   // code
}
```

- Sử dụng `break` statement tại một `case` để sau khi thực thi xong code của case đó thì `switch` không nhảy xuống `case` tiếp theo phía dưới

Example sử dụng condition trong switch

```javascript
let num = prompt('Enter number');
switch (true) {
  case num > 0:
    console.log('Number is positive');
    break;
  case num == 0:
    console.log('Numbers is zero');
    break;
  case num < 0:
    console.log('Number is negative');
    break;
  default:
    console.log('Entered value was not a number');
}
```

## Ternary Operators (toán tử hai ngôi)

```javascript
let isRaining = true
isRaining
  ? console.log('You need a rain coat.')
  : console.log('No need for a rain coat.')
```
