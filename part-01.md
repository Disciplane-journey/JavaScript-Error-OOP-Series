# Part 01 — try/catch & Error Handling

## Without try/catch — app crashes

```js
let data = JSON.parse("invalid json")
console.log("this never runs") ❌
```

---

## With try/catch — error handled

```js
try {
  let data = JSON.parse("invalid json")
  console.log(data)
} catch(error) {
  console.log(error.message) ✅
}
```

---

## finally — always runs

```js
try {
  let data = JSON.parse("invalid json")
} catch(error) {
  console.log("error caught") ✅
} finally {
  console.log("always runs") ✅
}
```

---

## throw — create custom errors

```js
function divide(a, b) {
  if(b === 0) {
    throw new Error("Cannot divide by zero")
  }
  return a / b
}

try {
  divide(10, 0)
} catch(error) {
  console.log(error.message) // "Cannot divide by zero" ✅
}
```

---

## error object properties

```js
try {
  null.name
} catch(error) {
  console.log(error.name)    // "TypeError"
  console.log(error.message) // "Cannot read properties of null"
}
```

---

## Quick Reference

| | Meaning |
|---|---|
| try | Code to run |
| catch | Runs if error occurs |
| finally | Always runs |
| throw | Create custom error |
| error.message | Error description |
| error.name | Error type |

> JavaScript Error & OOP Series
