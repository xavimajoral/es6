# every\(\), some\(\)

![](/assets/every.png)

**Example 1:    
**Want to find the computers with greater than 16gb of ram:

```js
var computers = [
  { name: 'Apple', ram: 24},
  { name: 'Compaq', ram: 4},
  { name: 'Acer', ram: 32}
];
```

I want a boolean, value. Can they run the program? Yes or No?

```js
var allComputersCanRunProgram = true;
var onlySomeComputersCanRunProgram = false;
```

### ES5

```js
for (var i = 0; i < computers.length; i++) {
  var computers = computers[i];

  if (computers.ram < 16) {
    allComputersCanRunProgram = false;
  } else {
    onlySomeComputersCanRunProgram = true;
  }
}

allComputersCanRunProgram;
onlySomeComputersCanRunProgram;
```

### ES6

with **every\(\)** =&gt;  && opeartor

```js
computers.every(function(computer) {
  return computer.ram > 16;
});
```

return false, as not all the the computers can run the program.

with **some** =&gt; do any records satisfy the function =&gt; \|\| operator

```js
computers.some(function(computer) {
  return computer.ram > 16;
});
```

---

**Example 2:    
**Check that the length of name is greater than 4 charac.

```js
var names = [
  "Alexandria",
  "Matthew",
  "Joe"
];
names.every(function(name) {
  return name.length > 4;
});
names.some(function(name) {
  return name.length > 4;
});
```

---

**Example 3:    
**Form validation

```js
function Field(value) {
  this.value = value;
}

Field.prototype.validate = function() {
    return this.value.length > 0;
}

var username = new Field('Xavi');
var password = new Field('alalalalong');
var birthday = new Field('10/10/2017');

var fields = [username, password, birthday];

var formIsValid = fields.every(function(field) {
    return field.validate();
});

if (formIsValid) {
    //allow user to Submit
} else {
  // show error messages
}
```



