# **forEach\(\)**

The `forEach()`method executes a provided function once for each array element.

**Example 1:**

```js
colors.forEach(function(color){
  console.log(color);
});
```

---

**Example 2:**

```js
var numbers = [1,2,3,4,5];
var sum = 0;
numbers.forEach(function(number){
  sum += number;
});
sum; //15
```

In forEach we don't need to pass anonymous function, we can pass a function:

**Example 2.1:**

```js
var numbers = [1,2,3,4,5];
var sum = 0;
function adder(number) {
  sum += number;
}
numbers.forEach(adder); 
// Carefull, 'adder' without parenthesis. 
// Otherwise we're calling the function, evaluate it and passing its value.
sum; //15
```

---

### **Exercises**

**Exercise 1:**  
The array below contains an array of objects, each of which is a representation of an image.  
Using the forEach helper, calculate the area of each image and store it in a new array called 'areas'.  
The area of an image can be calculated as 'image.height \* image.width'.

```js
var images = [
  { height: 10, width: 30 },
  { height: 20, width: 90 },
  { height: 54, width: 32 }
];

var areas = [];

function calcArea(image){
    return  image.height * image.width;
}

images.forEach(function(image) {
    areas.push(calcArea(image));
});
```

**Links:**

* [mdn - forEach\(\)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)



