# JavaScript-Notes

**Output In Javascript:**

````
console.log()

````

**Commenting:**

````
//Single line comment

/*
Multi
Line
Comment
*/
````

**Primitive Data Types:**

* Number - let age = 22;
* String - let firstName = "Ayan";
* Boolean - let adult = true;
* Undefined - Initiated but no value: let hello;
* Null - 'empty value'
* Symbol (ES2015)
* Bigint (ES2020) - Integers that are too big!

**Undefined Variables**

When JavaScript variables are declared, they have an initial value of undefined. If you do a mathematical operation on an undefined variable your result will be NaN which means "Not a Number". If you concatenate a string with an undefined variable, you will get a string of undefined.

**JavaScript Variables**

* Var - Re-declare it and Update the value.
* Let - Only Update the value.
* Const - We cannont redeclare or update the value.

**Template Literal**

````
let username = "Ayan";
let age = 22;

console.log(`Welcome ${username}, your age is ${age}.`);
````
**Output** -  Welcome Ayan, your age is 22.

To Check Data Type - 

````
let age = 22;

console.log(typeof age);

Output - Number
````

**Type Conversion**

* String to Number - Number(x);
* Number to String - String(a);
* Boolean - Boolean(a);


**Nullish Coalescing**

It gives the output when the value is Undefined or NULL.

````
let age = null;

console.log(age ?? "Hi");

Output - Hi
````

**Error Handling**

````
try{
    some lines of code....
 }
catch(error){
    console.log(error);
    console.log(error.name);
    console.log(error.message);
    console.log(error.stack);
    console.log("something else");
````







    
