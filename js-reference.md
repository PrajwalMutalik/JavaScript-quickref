# 🧠 JavaScript Quick Reference

A curated cheat sheet for modern JavaScript — covering key functions, methods, tricks, and patterns used in day-to-day development.

> ✅ Perfect for revision, interviews, or keeping as a developer handbook.

## 📌 Table of Contents
- [🔤 String Methods](#-string-methods)
- [🔢 Number & Math](#-number--math)
- [📚 Arrays](#-arrays)
- [📦 Objects](#-objects)
- [🧰 Utility & Built-ins](#-utility--built-ins)
- [⏲️ Timers](#️-timers)
- [🌐 Browser APIs](#-browser-apis)
- [🧪 Type Checking](#-type-checking)
- [💡 Bonus Snippets](#-bonus-snippets)



# 🔤 String Methods

```js
const str = "Hello World";

str.length;               // 11
str.toUpperCase();        // "HELLO WORLD"
str.toLowerCase();        // "hello world"
str.includes("World");    // true
str.startsWith("He");     // true
str.endsWith("ld");       // true
str.slice(0, 5);          // "Hello"
str.split(" ");           // ["Hello", "World"]
str.trim();               // removes whitespace

---
## 🔢 Number & Math

Number("42");           // 42
parseInt("42.9");       // 42
parseFloat("42.9");     // 42.9
isNaN("abc");           // true
Math.floor(4.9);        // 4
Math.ceil(4.1);         // 5
Math.round(4.6);        // 5
Math.max(1, 4, 6);      // 6
Math.random();          // 0 to 1

---
## 📚 Arrays

const arr = [1, 2, 3, 4];

// Modification
arr.push(5);            // [1,2,3,4,5]
arr.pop();              // removes 5
arr.shift();            // removes 1
arr.unshift(0);         // [0,2,3,4]
arr.splice(2, 1);       // remove 1 item at index 2

// Access & Iteration
arr.includes(3);        // true
arr.indexOf(3);         // 2
arr.find(x => x > 2);   // 3
arr.filter(x => x % 2 === 0); // [2, 4]
arr.map(x => x * 2);    // [2,4,6,8]
arr.reduce((a,b) => a + b, 0); // sum

// Spread
const copy = [...arr];

---

## 📦 Objects

const user = { name: "Prajwal", age: 22 };

// Access
user.name;              // "Prajwal"
user["age"];            // 22

// Add / Update / Delete
user.email = "a@b.com";
delete user.age;

// Object methods
Object.keys(user);      // ['name', 'email']
Object.values(user);    // ['Prajwal', 'a@b.com']
Object.entries(user);   // [['name', 'Prajwal'], ['email', 'a@b.com']]

---

## 🧰 Utility & Built-ins

JSON.stringify(obj);    // object → JSON string
JSON.parse(jsonStr);    // JSON string → object

const now = new Date(); // current time/date
now.getFullYear();      // 2025

typeof null;            // "object" (quirk)
typeof undefined;       // "undefined"

---

## ⏲️ Timers

setTimeout(() => {
  console.log("After 1 sec");
}, 1000);

const interval = setInterval(() => {
  console.log("Repeating...");
}, 1000);

clearInterval(interval);  // stop interval

---

## 
🌐 Browser APIs

console.log("Debug");

alert("Hello!");

prompt("Enter name:"); // user input

navigator.userAgent;
window.innerWidth;

document.getElementById("myId");
document.querySelector(".class");

---

## 🧪 Type Checking

typeof "hello";         // "string"
Array.isArray([]);      // true
value === null;         // null check
value !== undefined;    // defined check

---

## 💡 Bonus Snippets

// Swap variables
[a, b] = [b, a];

// Default parameters
function greet(name = "Guest") {
  return `Hi, ${name}`;
}

// Ternary
const msg = isLoggedIn ? "Logout" : "Login";

// Optional chaining
user?.profile?.email;

// Nullish coalescing
const val = input ?? "default";

