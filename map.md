# map\(\)

Write a loop that iterates over a list of numbers, doubles the value of it and pushes the value to a new Array

**Example 1:**

```js
var numbers = [1, 2, 3];
var doubled = numbers.map(function(number){
  return number * 2; //Important to remember to add the return keyword. Otherwise it returns undefined
});
doubled;
```

Used when we want to modify records in some lists of data

**Example 2:**

```js
var cars = [
  { model: 'Ibiza', price: 'Cheap'},
  { model: 'RS6', price: 'Expensive'}
];
var prices = cars.map(function(car) {
  return car.price;
});
prices;
```

**Example 3:**  
Using map, create a new array that contains the 'height' property of each object.  
Assign this new array to the variable 'heights'.  
Don't forget to use the 'return' keyword in the function!

```js
var images = [
  { height: '34px', width: '39px' },
  { height: '54px', width: '19px' },
  { height: '83px', width: '75px' },
];

var heights = images.map(function(image) {
    return image.height;
});
```

**Example 4:**  
Using map, create a new array that contains the distance / time value from each trip.  
In other words, the new array should contain the \(distance / time\) value.  
Assign the result to the variable 'speeds'.

```js
var trips = [
  { distance: 34, time: 10 },
  { distance: 90, time: 50 },
  { distance: 59, time: 25 }
];

var speeds = trips.map(function(trip) {
    return (trip.distance/trip.time);
});
```

**Example 5:**  
Implement a 'pluck' function.  
Pluck should accept an array and a string representing a property name and return an  array containing that property from each object.

```js
var paints = [ { color: 'red' }, { color: 'blue' }, { color: 'yellow' }];
pluck(paints, 'color'); // returns ['red', 'yellow', 'blue'];
// Hint: Remember that you can access a property on an object by using square bracket notation. For example...
var person = { name: 'Bill' };
person['name'] // returns 'Bill'
//
function pluck(array, property) {
    var result = array.map(function(elem) {
       return elem[property];
    });
    return result;
}
```



