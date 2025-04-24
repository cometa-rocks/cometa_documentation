<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/logos/COMETAROCKS_LogoEslog_Y_W.png">
  <source media="(prefers-color-scheme: light)" srcset="https://github.com/cometa-rocks/cometa_documentation/blob/main/img/logos/COMETAROCKS_LogoEslog_Y_B.png">
  <img alt="Shows a black logo in light color mode and a white one in dark color mode." src="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
</picture>

<br />

# Questions

Here are some of the questions that we have received on how to test something inside co.meta.

## Table of Contents 

- [Can you create conditions?](#question1)
- [Randomly select/click](#question2)

<br />

---

<br />

## Can you create conditions? <a name="question1"></a>

### Detailed question
```
Can you create conditions? For example, click on this row of the table if the value "Canceled" is in the "Status" column.
```
### What is needed
We need to mark checkboxes to `true` if order status is `Canceled`.
### Example data structure
```html
<table>
    <tr>
        <th>Selected</th>
        <th>Order ID</th>
        <th>Products</th>
        <th>Order Date</th>
        <th>Status</th>
    </tr>
    <tr>
        <td><input type="checkbox" /></td>
        <td>Order #1</td>
        <td>Product #1, Product #2</td>
        <td>2022-03-24</td>
        <td>Canceled</td>
    </tr>
    <tr>
        <td><input type="checkbox" /></td>
        <td>Order #2</td>
        <td>Product #3, Product #4</td>
        <td>2022-03-25</td>
        <td>Pending</td>
    </tr>
    <tr>
        <td><input type="checkbox" /></td>
        <td>Order #3</td>
        <td>Product #1, Product #3</td>
        <td>2022-03-26</td>
        <td>Paid</td>
    </tr>
    <tr>
        <td><input type="checkbox" /></td>
        <td>Order #4</td>
        <td>Product #1, Product #2</td>
        <td>2022-03-27</td>
        <td>Canceled</td>
    </tr>
</table>
<button onClick="doSomething();">Do Something</button>
```
### How to solve this problem with co.meta
To solve this problem we can use `Run Javascript function "{function}"` step.
Inside the Javascript code we can create small function to achieve what we want, so we'll create small steps to solve the problem.
#### **1. Get all elements with status `Canceled`**

To get all elements with status `Canceled` we can use XPath or IF-Else condition inside JS, in this case we will be using XPath.

So we'll create a small function that returns all the elements that meet our XPath expression.

Code by <a name="credit" href="https://stackoverflow.com/a/42600459/18232031">**@Krisztián Balla**</a>:
```javascript
function getElementsByXPath(xpath, parent){
    let results = [];
    let query = document.evaluate(xpath, parent || document, null, XPathResult.ORDERED_NODE_SNAPSHOT_TYPE, null);
    for (let i = 0, length = query.snapshotLength; i < length; ++i) {
        results.push(query.snapshotItem(i));
    }
    return results;
}
```

Now that we have a function that returns all the elements using XPath we can get all the rows with status `Canceled` like so:
```javascript
const checkBoxes = getElementsByXPath("//tr[td[5][text()='Canceled']]/td/input");
```

#### **2. Check the checkboxes that we have found**
Now to check all the checkboxes inside the list we have found we can run a `forEach` loop like so:
```javascript
checkBoxes.forEach(checkBox => checkBox.checked = true);
```

### Final Step
This is how the step would look like after all
```
Run Javascript function "
// return all elements that meet the xpath expression
function getElementsByXPath(xpath, parent){
    let results = [];
    let query = document.evaluate(xpath, parent || document, null, XPathResult.ORDERED_NODE_SNAPSHOT_TYPE, null);
    for (let i = 0, length = query.snapshotLength; i < length; ++i) {
        results.push(query.snapshotItem(i));
    }
    return results;
}
// get all checkboxes of canceled orders
const checkBoxes = getElementsByXPath("//tr[td[5][text()='Canceled']]/td/input");
// check all found checkboxes
checkBoxes.forEach(checkBox => checkBox.checked = true);
"
```

## Randomly select/click <a name="question2"></a>

### Detailed question
```
Is it also possible to randomly select any rows in the selection tables?
```
### What is needed
We need to mark checkboxes to `true` in random order.
### Example data structure
```html
<table>
    <tr>
        <th>Selected</th>
        <th>Order ID</th>
        <th>Products</th>
        <th>Order Date</th>
        <th>Status</th>
    </tr>
    <tr>
        <td><input type="checkbox" /></td>
        <td>Order #1</td>
        <td>Product #1, Product #2</td>
        <td>2022-03-24</td>
        <td>Canceled</td>
    </tr>
    <tr>
        <td><input type="checkbox" /></td>
        <td>Order #2</td>
        <td>Product #3, Product #4</td>
        <td>2022-03-25</td>
        <td>Pending</td>
    </tr>
    <tr>
        <td><input type="checkbox" /></td>
        <td>Order #3</td>
        <td>Product #1, Product #3</td>
        <td>2022-03-26</td>
        <td>Paid</td>
    </tr>
    <tr>
        <td><input type="checkbox" /></td>
        <td>Order #4</td>
        <td>Product #1, Product #2</td>
        <td>2022-03-27</td>
        <td>Canceled</td>
    </tr>
</table>
<button onClick="doSomething();">Do Something</button>
```
### How to solve this problem with co.meta
To solve this problem we can use `Run Javascript function "{function}"` step.
Inside the Javascript code we can create small function to archive what we want, so we'll create small steps to solve the problem.
#### **1. Get a random number between 1 and maximum number of rows in table**

Create a small function that returns a random number between 1 and maximum number of rows.

Code by <a name="credit" href="https://stackoverflow.com/a/1527820/18232031">**@Ionuț G. Stan**</a>:
```javascript
function getRandomInt(min, max) {
    min = Math.ceil(min);
    max = Math.floor(max);
    return Math.floor(Math.random() * (max - min + 1)) + min;
}
```

#### **2. Get a random number using the function above**
```javascript
// get all rows
let rows = document.querySelectorAll("table tr");
// minimum value here is 2 because we don't want to include header
let randomNumber = getRandomInt(2, rows.length);
```

#### **3. Check the checkbox for the order at randomNumber position**
```javascript
// get row
let row = rows[randomNumber];
// check the checkbox
row.querySelector(input).checked = true;
```

### Final Step
This is how the step would look like after all
```
Run Javascript function "
// return a random number between min and max
function getRandomInt(min, max) {
    min = Math.ceil(min);
    max = Math.floor(max);
    return Math.floor(Math.random() * (max - min + 1)) + min;
}
// get all rows
let rows = document.querySelectorAll("table tr");
// minimum value here is 2 because we don't want to include header
let randomNumber = getRandomInt(2, rows.length);
// get row
let row = rows[randomNumber];
// check the checkbox
row.querySelector(input).checked = true;
"
```

