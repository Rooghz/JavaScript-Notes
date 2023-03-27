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


