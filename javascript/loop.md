# Loop

## for

```javascript
for(let i = 0; i <= 5; i++){
  console.log(i)
}

for(let i = 5; i >= 0; i--){
  console.log(i)
}
```

## for of

```javascript
const numbers = [1, 2, 3, 4, 5]

for (const num of numbers) {
  console.log(num)
}
```

## while, do while

```javascript
let i = 0
while (i <= 5) {
  console.log(i)
  i++
}
```

```javascript
let i = 0
do {
  console.log(i)
  i++
} while (i <= 5)
```

## break

Được sử dụng để ngắt vòng lặp

```javascript
for(let i = 0; i <= 5; i++) {
  if(i == 3) {
    break
  }
  console.log(i)
}
// 0 1 2
```

## continue

Skip step hiện tại của vòng lặp

```javascript
for(let i = 0; i <= 5; i++){
  if(i == 3){
    continue
  }
  console.log(i)
}
// 0 1 2 4 5
```
