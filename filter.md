# **filter\(\)**

**Example:**  
Filter out or sort some products.  
Classic Use Case --&gt; Only show me some specific type, **i.e:** vegetable

```js
var products = [
  { name: 'cucumber', type: 'vegetable' },
  { name: 'banana', type: 'fruit' },
  { name: 'celery', type: 'vegetable' },
  { name: 'orange', type: 'fruit' }
];

products.filter(function(product) {
    return product.type === 'vegetable';
});
```

We create a new subset, don't want to modify the original array

> Don't forget to include the return!



**Another example with more conditions:**  
Type is vegetable, quantity is greater than 0, prices is less than 10

```js
products.filter(function(product) {
  return product.type === 'vegetable'
      && product.quantity > 0
      && product.price < 15
});
```

**Another example:** Give me the list of comments that belong to a particular post.

```js
var post = { id: 4, title: 'New Post' };
var comments = [
  { postId: 4, content: 'awesome post' },
  { postId: 3, content: 'it was ok' },
  { postId: 4, content: 'neat' }
];

function commentsForPost(post, comments) {
    return comments.filter(function(comment) {
      return comment.postId === post.id;
  });
}

commentsForPost(post, comments);
```

**Exercise: Filtering Values    
**Filter the array of numbers using the filter helper, creating a new array that only contains numbers greater than 50.  
Assign this new array to a variable called 'filteredNumbers'. Don't forget to use the 'return' keyword in the function!

```js
var numbers = [15, 25, 35, 45, 55, 65, 75, 85, 95];
// number > 50
var filteredNumbers =[];

function filterOne(numbers) {
  return numbers.filter(function(number) {
        if (number > 50) {
              return filteredNumbers.push(number);
        }
    });
}

filterOne(numbers);
```

**Exercise: Handling Permissions with Filter    
**Filter the array of users, only returning users who have admin level access.  
Assign the result to the variable 'filteredUsers'. Don't forget to use the 'return' keyword in the function!

```js
var users = [
 { id: 1, admin: true },
 { id: 2, admin: false },
 { id: 3, admin: false },
 { id: 4, admin: false },
 { id: 5, admin: true },
];

var filteredUsers = [];

function filterUsers(users) {
    return users.filter(function(user) {
        if (user.admin === true) {
            return filteredUsers.push(user);
        }
    });
}

filterUsers(users);
```

**Exercise: Challenging! Implementing 'reject'.    
**This is a hard one!  Create a function called 'reject'.  
Reject should work in the opposite way of 'filter' - if a function returns 'true', the item should \*not\* be included in the new array. **Hint**: you can reuse filter.

```js
// For example:
var numbers = [10, 20, 30];

var lessThanFifteen = reject(numbers, function(number){
  return number > 15;
});

lessThanFifteen // [ 10 ];

function reject(array, iteratorFunction) {

}
```



