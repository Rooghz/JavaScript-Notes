# JavaScript String

**Iterating over String**

````
let message = "hello";

for(let char of message){
    console.log(char);
}

````
````
let message = "name";

for(let i=0; i<message.length; i++){
    console.log(message[i]);
}

````
h <br/>
e <br/>
l <br/>
l <br/>
o <br/>

**String Methods**

**charAt()**

````
let message = "hello";

console.log(message.charAt(1));
````
e

**charCodeAt()**
````
let message = "hello";

console.log(message.charCodeAt(1));
````
101


**indexOf()**

indexOf() function finds the index of the first occurrence of the argument string in the given string. The value returned is 0-based. The syntax of the function is as follows: 

str.indexOf(searchValue , index)

````
let message = "hello";

console.log(message.indexOf("e"));
````
1

If the search value is not present, it returns -1.

**includes()**

In JavaScript, includes() method determines whether a string contains the given characters within it or not. This method returns true if the string contains the characters, otherwise, it returns false. 

string.includes(searchvalue, start)

````
var str = "Welcome.";
var check = str.includes("Welcome");
if(check){
	console.log("present");
}
else{
	console.log("not present");
}
````

Output - 
present

````
var str = "Welcome to Github.";
var check = str.includes("o",11);
console.log(check);
````

Output
false

In this case the second parameter is 11, so the search will take place from index 11, and since there is no 'o' after index 11, it returns false.

If the computed index(starting index) i.e the position from which the search will begin is less than 0, the entire array will be searched. 

**toUpperCase() and toLowerCase()**

````
function func() {
    var str = 'ayan';
    var string = str.toUpperCase();
    console.log(string);
}
func();
````
AYAN

````

function func() {
    var str = 'HELLO';
    var string = str.toLowerCase();
    console.log(string);
}
func();
````
hello

**substring()**

The substring() is an inbuilt function in JavaScript which is used to return the part of the given string from start index to end index. Indexing start from zero (0). 

Syntax: 

string.substring(Startindex, Endindex)

````
// Taking a string as variable
var string = "HiHowAreYou?";
a = string.substring(0, 5)
b = string.substring(2, 5)
c = string.substring(5)
d = string.substring(0)

// Printing new string which are
// the part of the given string
console.log(a);
console.log(b);
console.log(c);
console.log(d);
````
HiHow <br/>
How <br/>
AreYou? <br/>
HiHowAreYou? <br/>

