## ✅ Differences Between Interfaces and Types in TypeScript

When working with TypeScript, both `interface` and `type` allow you to define the shape of an object. However, they have key differences that are important to understand for writing clean, maintainable code.

---

### 🔍 Comparison Table

| Feature   | Interface                          | Type Alias                          |
| --------- | ---------------------------------- | ----------------------------------- |
| Syntax    | `interface Person {}`              | `type Person = {}`                  |
| Extension | Can **extend** interfaces or types | Can **extend** types or interfaces  |
| Merging   | Can be **merged**                  | Cannot be merged                    |
| Use Cases | Recommended for objects & classes  | Useful for unions, primitives, etc. |

---

### ✅ Pros of `Interface`

- Supports **declaration merging**
- Better suited for **OOP-style development** (e.g., class implementations)
- Cleaner and more intuitive syntax for defining objects

### ❌ Cons of `Interface`

- Can only describe **object-like** structures
- Less flexible with advanced types like **unions**

---

### ✅ Pros of `Type`

- Can represent **union**, **intersection**, **tuples**, and **primitives**
- More powerful for **complex type compositions**
- Easier to use when **combining multiple types**

### ❌ Cons of `Type`

- Cannot **merge multiple declarations** like interfaces
- Less intuitive for beginners when used for **large object shapes**

---

## 🔀 Mastering Union and Intersection Types in TypeScript: With Real Examples

TypeScript provides powerful ways to compose types using **union** and **intersection**. Here's how you can use them effectively:

---

### 🔹 Union Type Example

Union types allow a value to be one **of multiple types**.

```ts
function printId(id: number | string) {
  console.log("Your ID is: " + id);
}

printId(101);        // ✅ Valid
printId("XYZ123");   // ✅ Valid
