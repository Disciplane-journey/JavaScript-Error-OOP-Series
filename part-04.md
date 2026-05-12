# Part 04 — Polymorphism & Abstraction

## Polymorphism

Same method name — different behavior in each class.

```js
class Animal {
  sound() { console.log("Some sound") }
}

class Dog extends Animal {
  sound() { console.log("Woof") }
}

class Cat extends Animal {
  sound() { console.log("Meow") }
}

let dog = new Dog()
let cat = new Cat()

dog.sound() // Woof ✅
cat.sound() // Meow ✅
```

Child class overrides the parent method with its own version.

---

## Abstraction

Hide complex details — show only what is needed.

```js
class Car {
  #engineStart() {
    console.log("Engine started")
  }

  drive() {
    this.#engineStart()
    console.log("Car is moving") ✅
  }
}

let car = new Car()
car.drive()        // Car is moving ✅
car.#engineStart() // Error ❌
```

---

## All 4 OOP Concepts

| Concept | Meaning |
|---------|---------|
| Encapsulation | Hide data |
| Inheritance | Child gets parent features |
| Polymorphism | Same method, different behavior |
| Abstraction | Hide complexity |

> Part 04/04 — JavaScript Error & OOP Series
