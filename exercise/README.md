<h1>
  <span class="headline">Intro to JavaScript Objects Lab</span>
  <span class="subhead">Exercise</span>
</h1>


## Part 1: Arrays

### Exercise 1: Read the menu

Create an array named `menuItems` containing these strings, in this order:

- `'Tea'`
- `'Coffee'`
- `'Sandwich'`
- `'Cookie'`

Then log:

1. The first item.
2. The third item.
3. The number of items.
4. The last item, using `.length` to calculate its index.

**Expected output:**

```text
Tea
Sandwich
4
Cookie
```

### Exercise 2: Update the waiting list

Start with:

```js
const waitingCustomers = ['Aisha', 'Omar', 'Noor'];
```

Complete these steps **in order**:

1. Replace `'Omar'` with `'Ali'` using an index.
2. Add `'Dana'` to the end using `push()`.
3. Log the number of customers. It should now be `4`.
4. Remove the last customer using `pop()` and store the returned value in `removedCustomer`.
5. Log `removedCustomer`.
6. Log the final array.

**Final results:**

```js
removedCustomer // 'Dana'
waitingCustomers // ['Aisha', 'Ali', 'Noor']
```

> 💡 `pop()` both changes the array and returns the removed element.

### Exercise 3: Print a numbered menu

Start with:

```js
const drinks = ['Water', 'Tea', 'Coffee', 'Juice'];
```

Use a **regular `for` loop** to print:

```text
1. Water
2. Tea
3. Coffee
4. Juice
```

**Requirements:**

- Use `drinks.length` in your loop condition.
- Calculate each displayed number from the index.
- Your loop should still work if another drink is added.

### Exercise 4: Calculate the prices

Start with:

```js
const prices = [2, 5, 3, 6, 4];
```

1. Create a variable named `totalPrice`, starting at `0`.
2. Create a variable named `expensiveItemCount`, starting at `0`.
3. Use **`forEach()`** to:
   - Add every price to `totalPrice`.
   - Count how many prices are **greater than or equal to `4`** using `expensiveItemCount`.
4. Log both results after the iteration finishes.

**Expected results:**

```text
Total price: 20
Items costing 4 or more: 3
```

> 💡 Variables that keep a running total or count usually need `let`.

---

## Part 2: Objects

### Exercise 5: Describe the café

Create an object named `cafe` with these properties:

| Property | Value |
|---|---|
| `name` | `'Campus Café'` |
| `location` | `'Building A'` |
| `seats` | `24` |
| `isOpen` | `true` |

Use dot notation to log:

```text
Campus Café is located in Building A.
Available seats: 24
```

**Requirement:** Build the messages using the object’s properties.

### Exercise 6: Update a drink

Start with:

```js
const drink = {
  name: 'Iced Coffee',
  price: 3,
  size: 'small',
  temporaryCode: 'TEMP-01',
};
```

Using dot notation:

1. Change `size` to `'large'`.
2. Increase `price` by `1`, using its current value.
3. Add an `isAvailable` property with the value `true`.
4. Delete `temporaryCode`.
5. Log the final object.

**Expected final object:**

```js
{
  name: 'Iced Coffee',
  price: 4,
  size: 'large',
  isAvailable: true,
}
```

### Exercise 7: Check an order

Start with:

```js
const order = {
  customerName: 'Mariam',
  itemName: 'Sandwich',
  price: 4,
  quantity: 3,
  isPaid: false,
};
```

1. Calculate the order total using `price` and `quantity`. Store it in `orderTotal` (`orderTotal` is a new property you should add to the object).
2. Using template literal notation and your `order` object, log:

```text
Mariam ordered 3 Sandwich items.
Order total: 12
```

3. Use an `if/else` statement:
   - If the order is paid, log `'Ready to prepare'`.
   - Otherwise, log `'Waiting for payment'`.
4. Change `order.isPaid` to `true` and run your code again to check the other message.

**Requirements:** Use the object’s properties. No arrays or loops are needed.

---

## Part 3: Arrays & Objects Together

### Exercise 8: Plan a study session

**Learning objective:** Access and update an array stored inside an object.

Start with:

```js
const studySession = {
  title: 'JavaScript Practice',
  room: 'Lab 2',
  topics: ['Variables', 'Arrays'],
};
```

1. Log the first topic.
2. Add `'Objects'` to the `topics` array using `push()`.
3. Log the number of topics.
4. Use `forEach()` to print each topic on a separate line.
5. Change `room` to `'Lab 3'`.
6. Log:

```text
JavaScript Practice will take place in Lab 3.
```

**Expected topics after the update:**

```js
['Variables', 'Arrays', 'Objects']
```

> 💡 Follow the structure: `studySession` is an object, and `studySession.topics` is an array.

### Exercise 9: Manage the products

**Learning objective:** Read and update objects stored inside an array.

Start with:

```js
const products = [
  { name: 'Tea', price: 2 },
  { name: 'Sandwich', price: 4 },
  { name: 'Cookie', price: 1 },
];
```

1. Log the name of the second product.
2. Change the second product’s price to `5`.
3. Use `push()` to add this product:

```js
{ name: 'Juice', price: 3 }
```

4. Use a regular `for` loop or `forEach()` to print every product in this format:

```text
Tea costs 2 BD.
Sandwich costs 5 BD.
Cookie costs 1 BD.
Juice costs 3 BD.
```

**Requirement:** Read each name and price from the corresponding object.

### Exercise 10: Check the study group

**Learning objective:** Process an array of objects stored inside another object.

Start with:

```js
const studyGroup = {
  name: 'JavaScript Crew',
  members: [
    { name: 'Aisha', completedHomework: true },
    { name: 'Omar', completedHomework: false },
    { name: 'Noor', completedHomework: true },
  ],
};
```

1. Log the group name.
2. Log the number of members.
3. Create a variable named `completedCount`, starting at `0`.
4. Loop through `studyGroup.members`.
5. For each member:
   - If they completed their homework, increase `completedCount`.
   - Otherwise, print their name in a reminder message.
6. After the loop, print the completion count.

**Expected output:**

```text
JavaScript Crew
3
Omar needs to finish the homework.
Completed homework: 2
```

**Requirement:** Calculate the count by checking the members. Your solution should still work if another member is added.

