# Part 03 — Encapsulation & Inheritance

## Encapsulation

Hide data inside a class — only expose what is needed.

```js
class BankAccount {
  #balance = 0 // private

  deposit(amount) {
    this.#balance += amount
  }

  getBalance() {
    return this.#balance
  }
}

let account = new BankAccount()
account.deposit(1000)
console.log(account.getBalance()) // 1000 ✅
console.log(account.#balance)     // Error ❌
```

---

## Inheritance

Child class gets all properties and methods of parent class.

```js
class Animal {
  speak() { console.log("Animal speaks") }
}

class Dog extends Animal {
  bark() { console.log("Dog barks") }
}

let dog = new Dog()
dog.speak() // Animal speaks ✅
dog.bark()  // Dog barks ✅
```

> JavaScript Error & OOP Series
