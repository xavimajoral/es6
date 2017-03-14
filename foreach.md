# **forEach\(\)**

**Example 1:**

```js
colors.forEach(function(color){
  console.log(color);
});
```

**Example 2:**

```js
var numbers = [1,2,3,4,5];
var sum = 0;
numbers.forEach(function(number){
  sum += number;
});
sum; //15
```

In forEach we don't need to pass anonymous function, we$$x = y$$ can pass a function:

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



