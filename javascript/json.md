# JSON

## JSON → Object

Để parse JSON sang Object, ta sử dụng `JSON.parse()`.

```javascript
JSON.parse(text)
JSON.parse(text, reviver)
```

- `text`: JSON string cần được convert sang Object.
- `reviver` (optional): callback cho phép thay đổi value khi mapping từ JSON sang Object.

    ```javascript
    JSON.parse(
    '{"p": 5}',
    (key, value) =>
        typeof value === "number"
        ? value * 2 // return value * 2 for numbers
        : value, // return everything else unchanged
    );
    // { p: 10 }
    ```

## Object → JSON

Để parse Object sang JSON, ta sử dụng `JSON.stringify()`

```javascript
JSON.stringify(value)
JSON.stringify(value, replacer)
JSON.stringify(value, replacer, space)
```

- `value`: value cần được convert sang JSON.
- `replacer`: 
- `spacer`: số lượng white space được chèn vào JSON (bao gồm thụt lề, xuống dòng,...).

    ```javascript
    function replacer(key, value) {
    // Filtering out properties
    if (typeof value === "string") {
        return undefined;
    }
    return value;
    }

    const foo = {
    foundation: "Mozilla",
    model: "box",
    week: 45,
    transport: "car",
    month: 7,
    };
    
    JSON.stringify(foo, replacer); // '{"week":45,"month":7}'

    JSON.stringify(foo, ["week", "month"]); // '{"week":45,"month":7}', only keep "week" and "month" properties
    ```
