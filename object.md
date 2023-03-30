## Object in JavaScript

````
let obj = {
    name : "Ayan",
    age : 22,
    work : "Software Engineer",
    skills : ["react", "node"],
    "is admin" : true
};

console.log(obj.name);
console.log(obj.skills[1]);
console.log(obj["is admin"]);
````

Ayan
node
true

**Functions as Property**

````
let obj = {
    name : "Ayan",
    greetMessage : function(){
        console.log("Welcome!")
    },
    bye(){
        console.log("Bye bye!!")
    }
};

obj.greetMessage();
obj.bye();
````

Welcome!
Bye bye!!

**For In**

```
const obj = {
  name: "Ayan",
  age: 22,
};

for (let item in obj) {
  console.log(item, obj[item]);
}

```

> name Ayan\
age 22

**Deal With Copy**

It's also a shallow copy and does not work with nested object.

````
const p1 = {
  name: "Ayan",
  age: 22,
};

let p2 = Object.assign({},p1);

p2.name = "Sample";
p1.age = 99;

console.log(p1);
console.log(p2);
````

> { name: 'Ayan', age: 99 }\
{ name: 'Sample', age: 22 }

**Spread Operator**

It will do Deep Copy. But it wont work with nested objects.

````
const p1 = {
  name: "Ayan",
  age: 22,
  city:{
    name: "kOL",
    state: "WB",
  }
};

let p2 = {...p1};

console.log(p1);
console.log(p2);
````
> { name: 'Ayan', age: 22, city: { name: 'kOL', state: 'WB' } }\
{ name: 'Ayan', age: 22, city: { name: 'kOL', state: 'WB' } }

**Copy nested objects**

````
const p1 = {
  name: "Ayan",
  age: 22,
  city:{
    name: "kOL",
    state: "WB",
  }
};

let p2 = {...p1, city: {...p1.city}};

p2.name = "Ashish";
p2.city.name = "Delhi";

console.log(p1);
console.log(p2);
````

> { name: 'Ayan', age: 22, city: { name: 'kOL', state: 'WB' } }\
{ name: 'Ashish', age: 22, city: { name: 'Delhi', state: 'WB' } }

**Optional Chaining**

?.

*Syntax:*

````
 

obj?.prop
obj?.[expr]
arr?.[index]
func?.(args)
````

````
const p1 = {
  name: "Ayan",
  age: 22,
  city:{
    name: "kOL",
    state: "WB",
  }
};

let p2 = {...p1, city: {...p1.city}};

p2.name = "Ashish";
p2.city.name = "Delhi";

console.log(p1);
console.log(p2);
console.log(p1.city?.no);
````

> { name: 'Ayan', age: 22, city: { name: 'kOL', state: 'WB' } }\
{ name: 'Ashish', age: 22, city: { name: 'Delhi', state: 'WB' } }\
undefined

**Destructuring Object**

````
const num = {
a: 1, 
b: 2
};  
const {a, b} = num;  
  
console.log(a); // 1  
console.log(b); // 2  
````

> Output\
1\
2

````
const student = {name: 'Prabal', rollno: '5'};  
const {name, rollno} = student;  
console.log(name); 
console.log(rollno); 
````
> Output:\
Prabal\
5

*We can assign a variable with a different name than the property of the object. You can see the illustration for the same as follows:*

````
const num = {x: 1, y: 2};  
const {x: a, y: b} = num;  
   
console.log(a);   
console.log(b); 
````
> Output:\
1\
2

**Call Method**

````
let user1 = {
  name: "John",
  age: 30,
};

let user2 = {
  name: "ayan",
  age: 99,
};

let user3 = {
  name: "hi",
  age: 999,
};

function sayHi() {
  console.log(this.name);
}

sayHi.call(user1);
sayHi.call(user2);
````

> John\
ayan

**Passing Multilple Arguements with Call**

````
let user1 = {
  name: "John",
  age: 30,
};

let user2 = {
  name: "ayan",
  age: 99,
};

let user3 = {
  name: "hi",
  age: 999,
};

function sayHi(degree, year) {
  console.log(this.name, degree, year);
}

sayHi.call(user1, "B.Tech-EE", 2021);
sayHi.call(user2);
````

> John B.Tech-EE 2021\
ayan undefined undefined

**Apply Method**

*You have to send arguements as an array so just Use [] while providing aruegements*

````
let user1 = {
  name: "John",
  age: 30,
};

let user2 = {
  name: "ayan",
  age: 99,
};

let user3 = {
  name: "hi",
  age: 999,
};

function sayHi(degree, year) {
  console.log(this.name, degree, year);
}

sayHi.apply(user1, ["B.Tech-EE", 2021]);
sayHi.apply(user2, ["B.Tech"]);
````

> John B.Tech-EE 2021\
ayan B.Tech undefined
