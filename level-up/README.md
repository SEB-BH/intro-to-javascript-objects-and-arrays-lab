<h1>
  <span class="headline">Intro to JavaScript Objects Lab</span>
  <span class="subhead">Level Up</span>
</h1>


## Part 4: Add Functions

### Exercise 11: A reusable price calculator

**Learning objective:** Write a function that accepts an array and returns a total.

Write a function named `calculateTotal` with one parameter named `itemPrices`.

The function should:

1. Start a local total at `0`.
2. Use a regular `for` loop or `forEach()` to add the prices.
3. **Return** the total after iteration finishes.

Test it using:

```js
console.log(calculateTotal([2, 5, 3])); // 10
console.log(calculateTotal([4, 4]));    // 8
console.log(calculateTotal([7]));       // 7
console.log(calculateTotal([]));        // 0
```

**Requirements:**

- Use the parameter rather than an array defined outside the function.
- Keep the calculation inside the function.
- Leave the supplied array unchanged.
- Return the answer; place your checking `console.log()` calls outside the function.

> 💡 Returning a value lets the code that called your function use the answer.

### Exercise 12: Give the bill a method

**Learning objective:** Add and call an object method that calculates a result from an array of objects.

Start with:

```js
const bill = {
  customerName: 'Noor',
  items: [
    { name: 'Tea', price: 2, quantity: 2 },
    { name: 'Sandwich', price: 4, quantity: 1 },
    { name: 'Cookie', price: 1, quantity: 3 },
  ],
};
```

Add a method named `getTotal` to `bill`.

Inside the method:

1. Create a local total starting at `0`.
2. Loop through `bill.items`.
3. For each item, calculate `price * quantity`.
4. Add that amount to the total.
5. Return the total after iteration finishes.

Use `bill.items` to access the items, following the object-method pattern from the lesson.

Test it:

```js
console.log(bill.getTotal()); // 11
```

Then add another item:

```js
bill.items.push({
  name: 'Water',
  price: 1,
  quantity: 2,
});

console.log(bill.getTotal()); // 13
```

**Requirements:**

- Call the method using `bill.getTotal()`.
- Calculate the result from the current items each time it is called.
- Start the local total at `0` on every call.
- Leave the items and their quantities unchanged.

> 💡 A **method** is a function stored as a property on an object.

