# goit-js-hw-06

Task 1. User Account

Perform this task in the file task-1.js

Before the release, the developer hacked the source code for managing user accounts for our food delivery service. Refactor the methods of the customer object by placing the missing this when accessing the object properties.

Use this starting code and refactor. After declaring the object, we added method calls. The results of their work will be displayed in the console. Please do not change anything there.

const customer = {
username: "Mango",
balance: 24000,
discount: 0.1,
orders: ["Burger", "Pizza", "Salad"],
// Change code below this line
getBalance() {
return balance;
},
getDiscount() {
return discount;
},
setDiscount(value) {
discount = value;
},
getOrders() {
return orders;
},
 addOrder(cost, order) {
 balance -= cost - cost * discount;
 orders.push(order);
 },
 // Change code above this line
};

customer.setDiscount(0.15);
console.log(customer.getDiscount()); // 0.15
customer.addOrder(5000, "Steak");
console.log(customer.getBalance()); // 19750
console.log(customer.getOrders()); // ["Burger", "Pizza", "Salad", "Steak"]

Leave this code for a mentor to review.



What the mentor will pay attention to when checking:

The customer variable is declared
The value of the customer variable is an object with properties and methods
Calling customer.getDiscount() returns the current value of the discount property
Calling customer.setDiscount(0.15) updates the value of the discount property
Calling customer.getBalance() returns the current value of the balance property.
The call to customer.getOrders() returns the current value of the orders property
The call to customer.addOrder(5000, "Steak") adds "Steak" to the orders property values ​​array and updates the balance
The getBalance method of the customer object uses this
The getDiscount method of the customer object uses this
The setDiscount method of the customer object uses this
The getOrders method of the customer object uses this
The addOrder method of the customer object uses this

Task 2. Warehouse

Perform this task in the task-2.js file

Create a Storage class that will create objects to manage the inventory of products. The class expects only one argument — an initial array of products, which is written to the created object in the private property items.

Declare the following methods of the class:

getItems() — returns an array of current products in the private property items.
addItem(newItem) — takes a new item newItem and adds it to the items array in the private property items of the object.
removeItem(itemToRemove) — takes a string with the item name itemToRemove and removes it from the items array in the private property items of the object.

Take the code below with the instance initialization and method calls and insert it after the class declaration to verify that it works correctly. The results of their work will be displayed in the console. Please do not change anything there.

const storage = new Storage(["Nanitoids", "Prolonger", "Antigravitator"]);
console.log(storage.getItems()); // ["Nanitoids", "Prolonger", "Antigravitator"]

storage.addItem("Droid");
console.log(storage.getItems()); // ["Nanitoids", "Prolonger", "Antigravitator", "Droid"]

storage.removeItem("Prolonger");
console.log(storage.getItems()); // ["Nanitoids", "Antigravitator", "Droid"]

storage.removeItem("Scaner");
console.log(storage.getItems()); // ["Nanitoids", "Antigravitator", "Droid"]

Leave this code for review by a mentor.

What the mentor will pay attention to when checking:

Storage class declared
Storage class declared getItems method
Storage class declared addItem method
Storage class declared removeItem method
Item property in Storage class declared private
The getItems method returns the value of the private items property of the class instance that calls it
The addItem method changes the value of the private items property of the class instance that calls it
The removeItem method changes the value of the private items property of the class instance that calls it
As a result of calling new Storage(["Nanitoids", "Prolonger", "Antigravitator"]), the value of the storage variable is an object
The storage object does not have a public items property
The first call to storage.getItems() immediately after the instance is initialized returns the array ["Nanitoids", "Prolonger", "Antigravitator"]
The second call to storage.getItems() after calling storage.addItem("Droid") returns the array ["Nanitoids", "Prolonger", "Antigravitator", "Droid"]
The third call to storage.getItems() after the call to storage.removeItem("Prolonger") returns the array ["Nanitoids", "Antigravitator", "Droid"]
The fourth call to storage.getItems() after the call to storage.removeItem("Scaner") returns the array ["Nanitoids", "Antigravitator", "Droid"]

Task 3. String constructor

Perform this task in the file task-3.js

Write a StringBuilder class that takes one parameter initialValue — an arbitrary string that is written to the private value property of the object being created.

Declare the following class methods:

getValue() — returns the current value of the private value property.
padEnd(str) — gets the str (string) parameter and adds it to the end of the value of the private value property of the object that calls this method.
padStart(str) — gets the str (string) parameter and adds it to the beginning of the value of the private value property of the object that calls this method.
padBoth(str) — gets the str (string) parameter and adds it to the beginning and end of the value of the private value property of the object that calls this method.
Take the code below with the instance initialization and method calls and insert it after the class declaration to verify that it works correctly. The results of their work will be displayed in the console. Please don't change anything there.

const builder = new StringBuilder(".");
console.log(builder.getValue()); // "."
builder.padStart("^");
console.log(builder.getValue()); // "^."
builder.padEnd("^");
console.log(builder.getValue()); // "^.^"
builder.padBoth("=");
console.log(builder.getValue()); // "=^.^="

Leave this code for review by a mentor.

What the mentor will pay attention to when checking:

The StringBuilder class is declared
The value property in the StringBuilder class is declared private
The getValue method is declared in the StringBuilder class
The getValue method returns the value of the private value property of the class instance that calls it
The padEnd method is declared in the StringBuilder class
The padEnd method changes the value of the private value property of the class instance that calls it
The padStart method is declared in the StringBuilder class
The padStart method changes the private value property of the class instance that calls it
The padBoth method is declared in the StringBuilder class
The padBoth method changes the value of the private value property of the class instance that calls it
As a result of calling new StringBuilder("."), the value of the private builder variable is an object
The builder object does not contain a public value property
The first call to builder.getValue() immediately after initialization of the instance returns a string .
The second call to builder.getValue() after calling builder.padStart("^") returns the string ^.
The third call to builder.getValue() after calling builder.padEnd("^") returns the string ^.^
The fourth call to builder.getValue() after calling builder.padBoth("=") returns the string =^.^=
