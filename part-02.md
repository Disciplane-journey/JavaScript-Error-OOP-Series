# Part 02 — Classes & Objects

## Class — blueprint

```js
class Person {
  constructor(name, age) {
    this.name = name
    this.age = age
  }

  greet() {
    console.log(`Hi I am ${this.name}`)
  }
}
```

constructor → runs when object is created

this → refers to the current object

---

## Object — instance of a class

```js
let ali  = new Person("Ali", 20)
let sara = new Person("Sara", 25)

console.log(ali.name) // "Ali" ✅
ali.greet()           // Hi I am Ali ✅
```

---

## Inheritance

```js
class Student extends Person {
  constructor(name, age, grade) {
    super(name, age)
    this.grade = grade
  }

  study() {
    console.log(`${this.name} is studying`)
  }
}

let ahmed = new Student("Ahmed", 18, "A")

ahmed.greet() // Hi I am Ahmed ✅
ahmed.study() // Ahmed is studying ✅
```

extends → inherit from another class

super() → call parent constructor

---

## Quick Reference

| | Meaning |
|---|---|
| class | Blueprint for objects |
| constructor | Runs when object is created |
| this | Current object |
| new | Create object from class |
| extends | Inherit from another class |
| super() | Call parent constructor |

> JavaScript Error & OOP Series
