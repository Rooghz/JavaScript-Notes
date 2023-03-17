# JavaScript-Notes

**Output In Javascript:**

```
console.log()

```

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

**Function**

````
function greet(){
    console.log("Welcome!");
}
greet();

````
Welcome!
````
function greet(name){
    console.log(`Welcome, ${name}!`);
}
greet("Ayan");
````
Welcome, Ayan!

**Anonymous Function**

Anonymous Function is a function that does not have any name associated with it. Normally we use the function keyword before the function name to define a function in JavaScript. However, for anonymous functions in JavaScript, we use only the function keyword without the function name.

An anonymous function is not accessible after its initial creation, it can only be accessed by a variable it is stored in as a function as a value. An anonymous function can also have multiple arguments, but only one expression.

The syntax below illustrates the declaration of anonymous function using normal declaration:

````
function() {
    // Function Body
 }
````
We may also declare anonymous function using arrow function technique which is shown below:

````
( () => {
    // Function Body...
} )();
````
````
var greet = function () {
    console.log("Welcome!");
};
 
greet();
````
Welcome!



**Arrow Function**

**How to create arrow function**: To write the arrow function, simply create any variable it can be const, let, or var but always do prefer with const to avoid unnecessary problems. And then assign the function code to the variable it. So from now, you can call that function by writing the parenthesis in front of that variable! With arrow function syntax, we consider function as an object and assign the definition to some variable. Following are the syntax of the arrow function:

````
const myFunction = (param1, param2,
    .... paramN) => { // function code }
const myFunction = (param) => { // function code }
                      or 
const myFunction = param => { // function code }  
const myFunction = param => { return param*param }
                      or 
const myFunction = param => param*param

````
We can omit the {} parenthesis when there is only one statement and the JavaScript considers that statement as return value, also there is no need to write parenthesis () when there is only one parameter. The arrow function cannot contain the line break between the (params) and the arrow =>, Also there should not be any space between the = and > characters.  

````
const calculateSum = (x,y) => x + y;

console.log(calculateSum(2,3));
````
5







    
