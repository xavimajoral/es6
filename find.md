# find\(\)

**Purpose**: to search to an Array and look for a particular element in the Array

As soon it's find the helper will return that record

**Example 1:**

```js
var users = [
  { name: 'Jill' },
  { name: 'Alex' },
  { name: 'Bill' }
];
users.find(function(user){
    return user.name === 'Alex';
});
// returns {"name":"Alex"}
// Only returns the first ocurrency that founds in case there are more than 1
```

---

**Example 2:      
**Try to find the car with some particular criteria

```js
function Car(model) {
    this.model = model;
}

var cars = [
    new Car('Buick'),
    new Car('Camaro'),
    new Car('Focus')
];

cars.find(function(car){
  return car.model === 'Focus';
});
```

---

**Example 3:      
**Find the posts where belongs the comment.

```js
var posts = [
  { id: 1, title: 'Old post' },
  { id: 2, title: 'New post' }
];

var comment = { postId: 1, content: 'Great Post' };

function postForComment(posts, comment) {
  return posts.find(function(post) {
    return post.id === comment.postId;
  });
}

postForComment(posts, comment);
```

---

---

**Example 4:      
**Find the user in the users's array who is an admin.  Assign this user to the variable 'admin'.

```js
var users = [
  { id: 1, admin: false },
  { id: 2, admin: false },
  { id: 3, admin: true }
];

var admin;

users.find(function(user){
    if (user.admin) {
        admin = user;
        return admin;
    }
});
```

---

**Example 5:    
**Find the account with a balance of 12 and assign it to the variable 'account'.

```js
var accounts = [
  { balance: -10 },
  { balance: 12 },
  { balance: 0 }
];

var account;

accounts.find(function(acc){
    if (acc.balance === 12) {
        account = acc;
        return account;
    }
});
```

---

**Example 6:**  
This is a tough one!  The most common find operation is to an object that has a given property.  
Rather than writing out a full function every time, it would be great if we has a shorthand syntax to find an object like this:

`findWhere(ladders, { height: '20 feet' });`

The object { ladders: '20 feet' } should be used as the search criteria - we would want to find a ladder whose 'height' property is '20 feet';

**Your goal**: Write a 'findWhere' function that achieves this shorthand approach.  'findWhere' should return the found object.

**In summary:**

```js
var ladders = [
  { id: 1, height: 20 },
  { id: 3, height: 25 }
];
findWhere(ladders, { height: 25 }); // result: { id:3, height: 25 }
```

Hint: the hard part of this is figuring out the name of the proeprty on the criteria.

You can use Object.keys\(criteria\)\[0\] to figure out the name of the property on the object.

For example, Object.keys\({ height: '20 feet' }\) would return 'height'.  You could then check to see if a given element in the array had a property equal to the criteria's value with something like element\[property\] === criteria\[property\].

