# backpackjs
useful js resources
<h1>1-Reverse a String</h1>


The following one-liner will reverse a string in JavaScript:

<pre><code>const reversedString = str.split('').reverse().join('');</code></pre>
<p>This code first splits the string into an array of characters, then reverses the order of the characters, and finally joins them back together into a string.</p>

<h1>2-Sum of Array Elements</h1>
<p>To find the sum of an array in JavaScript, you can use the reduce() method. The reduce() method iterates over each element in the array and reduces it to a single value, which in this case is the sum of all the elements.</p>
<pre><code>const numbers = [1, 2, 3, 4, 5];
const sum = numbers.reduce((total, number) => total + number, 0);
console.log(sum); // 15</code></pre>

<p>The first argument of the reduce() method is a callback function that takes two parameters: total and number. The total parameter is the running total of the array, and number is the current element being processed. The second argument of the reduce() method is the initial value of the total parameter. In this case, it’s set to 0.</p>

<h1>3-Largest and Smallest Number in Array</h1>
<p>To find the largest and smallest number in an array using JavaScript, you can use the following one-liner:</p>
<pre><code>
const numbers = [11, 2, 9, 6, 19];
console.log(Math.max(...numbers)); // 19
console.log(Math.min(...numbers)); // 2
This code uses the spread operator (…) to pass each value in the array as an argument to the Math.max() and Math.min()methods. These methods in turn return the largest and smallest numbers in the array, respectively.
</code></pre>
<h1>4-Remove Duplicates from Array</h1>
<pre><code>
const numbers = [2, 3, 7, 7, 2];
const uniqueNumbers = [...new Set(numbers)];
console.log(uniqueNumbers); // [2, 3, 7]
</code></pre>
By creating a new Set object and passing the array as its parameter, you can ensure that only unique values are kept. Then, using the spread operator, you can convert the set back into an array.
<h1>5-Looping Objects</h1>
<p>The Object.entries() method is used to return an array of an object’s key-value pairs. </p>
<pre><code>
const person = {
  name: 'person one',
  age: 25,
  city: 'city now'
};
for (const [key, value] of Object.entries(person)) {
  console.log(`${key}: ${value}`);
}
</code></pre>
<p>In this code, we have an object person with three properties: name, age, and city. We use the Object.entries() method to create an array of the key-value pairs of the person object. Then, we use a for...of loop to iterate over the array and destructure each key-value pair into variables key and value. Finally, we log the key and value to the console using a template literal.
</p>
<h1>6-Copy to ClipBoard</h1>
The Clipboard API provides a simple and efficient way to copy text to the clipboard in JavaScript.</p>
<pre><code>
function copyToClipboard(text) {
    navigator.clipboard.writeText(text);
}
</code></pre>

<h1>7-Offline/Online Status</h1>
To check the user’s online/offline status in a web application using JavaScript, you can use the navigator.onLine property.</p>
<pre><code>
if (navigator.onLine) {
  console.log('User is online');
} else {
  console.log('User is offline');
}
</code></pre>

<h1>8-Remove Falsy Values</h1>
In JavaScript, you can remove falsy values from an array using the filter() method. Falsy values include false, 0, '', null, undefined, and NaN.</p>
<pre><code>
const arr = [1, 2, 0, '', undefined, null, 3, NaN, false];

const filteredArr = arr.filter(Boolean);

console.log(filteredArr); // [1, 2, 3]
</code></pre>
In this code, Boolean is passed as the callback function to filter(). The Boolean() function is a built-in function in JavaScript that returns true for truthy values and false for falsy values. By passing Boolean as the callback function, filter() will remove all falsy values from the array arr and return a new array filteredArr with only truthy values.

<h1>9-Flattening an Array</h1>
To flatten a multi-dimensional array in JavaScript, you can use the flat() method. The flat() method creates a new array with all sub-array elements concatenated into it recursively up to the specified depth.</p>
<pre><code>
const multiDimensionalArray = [[1, 2], [3, 4, [5, 6]]];
const flattenedArray = multiDimensionalArray.flat(2);

console.log(flattenedArray); // Output: [1, 2, 3, 4, 5, 6]
</code></pre>
In this code, multiDimensionalArray is a two-dimensional array with two nested arrays. By calling the flat() method with a depth of 2, all sub-array elements are concatenated into a single flat array. The resulting flattenedArray contains all the elements of the original multi-dimensional array in a single dimension.

<h1>10-Accessing Custom Attributes</h1>
In HTML, data attributes provide a way to store additional data in an element. To access these data attributes in JavaScript, you can use the dataset property of the element.

For example, consider the following HTML element:

<div id="myDiv" data-name="jull" data-age="41"></div>
To access the data-name and data-age attributes of the div element using the dataset property, you can use the following JavaScript code:

const myDiv = document.getElementById('myDiv');
const name = myDiv.dataset.name;
const age = myDiv.dataset.age;

console.log(name); // "jull"
console.log(age);  // "41"
In this code, myDiv.dataset returns an object that contains the values of all the custom data attributes on the div element. We can access a specific data attribute by using its name as a property of the dataset object.

<h1>11-Create Array from Iterables</h1>
Array.from() is a built-in method in JavaScript that creates a new array from an iterable object or an array-like object.
<pre><code>
// Converting String to an array
const str = "jull";
const arr = Array.from(str);
console.log(arr); // Output: ["j", "u", "l", "l"]

// Converting Set to an array
const set = new Set([1, 2, 3, 3, 4, 5]);
const arr = Array.from(set);
console.log(arr); // Output: [1, 2, 3, 4, 5]
</code></pre>


<h1>12-Destructuring Arrays</h1>
Destructuring assignment is a way to extract values from arrays or objects and assign them to variables in a more concise and readable way. For example, consider the following array:
<pre><code>
const numbers = [1, 2, 3, 4, 5];
</pre></code>
Instead of accessing each element using index notation, we can use destructuring assignment to extract specific values:
<pre><code>
const [first, second, , fourth] = numbers;

console.log(first); // 1
console.log(second); // 2
console.log(fourth); // 4
</pre></code>
In this code, we use square brackets to create a pattern that matches the shape of the array. The commas in the pattern allow us to skip over elements that we’re not interested in. We can then assign the extracted values to new variables (first, second, and fourth) in a single line.

<h1>13-Destructuring Objects</h1>
We can also use destructuring assignments with objects:
<pre><code>
const {name, age, email} = person;
</pre></code>
<h1>14-Promise.all()</h1>
Promise.all() allows multiple promises to be executed in parallel. It takes an array of promises as input, and returns a new promise that resolves when all the input promises have resolved.
<pre><code>
const promise1 = fetch('https://api.example.com/data1');
const promise2 = fetch('https://api.example.com/data2');

Promise.all([promise1, promise2])
  .then(responses => {
    // handle responses from both requests here
    const response1 = responses[0];
    const response2 = responses[1];
    // do something with the responses
  })
  .catch(error => {
    // handle errors from either request here
    console.error(error);
  });
  </pre></code>
In this code, we create two promises using the fetch() method to fetch data from two different endpoints. We then pass an array of promises to Promise.all() which returns a new promise that resolves when all of the promises in the array have resolved.

We can then use the responses array in the then() block to handle the responses from both requests. If either promise rejects, the catch() block will handle the error.

<h1>15-Remove numbers from a string</h1>
This function removes the numbers from a string
<pre><code>
const removeNumbers = word => word.replace(/\d/g, "")
</code></pre>

<h1>16-Remove whitespace from a string</h1>
This function remove whitespace from a string
<pre><code>
const fruits = "Hola mundo";
let text = fruits.split(/\s+/).join(''); //Holamundo
</code></pre>
