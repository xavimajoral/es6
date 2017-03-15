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



