# JavaScript Array

**Iterating over Array**

````
let arr = ['apple', 'banana', 'tomato', 'potato'];

for(let i=0; i<arr.length; i++){
    console.log(arr[i]);
}
````
apple <br/>
banana <br/>
tomato <br/>
potato <br/>

````
let arr = ['apple', 'banana', 'tomato', 'potato'];

for(let char of arr){
    console.log(char);
}
````

**Copy by Reference**

Shallow copy: In the case of shallow copy when we copy the original object into the clone object then the clone object has the copy of the memory address of the original object i.e. both point to the same memory address.

Both original object and cloned object internally point to the same referenced object. Since they point to the same memory address so if we changed the cloned object then changes would be reflected back to the original object.

Spread Operator -

Spread operator allows an iterable to expand in places where 0+ arguments are expected. It is mostly used in the variable array where there is more than 1 values are expected. It allows us the privilege to obtain a list of parameters from an array. Syntax of Spread operator is same as Rest parameter but it works completely opposite of it.

Syntax:

var variablename1 = [...value]; 

````
let arr1 = [1,2,3];
let arr2 = [...arr1];

console.log(arr1);
console.log(arr2);

arr2.push(4);

console.log('updated arr1-',arr1);
console.log('updated arr2-',arr2);

````

[ 1, 2, 3 ] <br/>
[ 1, 2, 3 ] <br/>
updated arr1- [ 1, 2, 3 ] <br/>
updated arr2- [ 1, 2, 3, 4 ] <br/>

**push()**

Add an element/multiple elements at the end of an array.

````
let arr1 = [1,2,3];
arr1.push(4);

console.log(arr1);

arr1.push(5,6,7,8);

console.log(arr1);

````

[ 1, 2, 3, 4 ] <br/>
[ 1, 2, 3, 4, 5, 6, 7, 8] <br/>

**concat()**

Add two/multiple arrays.

````
let arr1 = [1,2,3];
let arr2 = [4,5,6];

let arr3 = arr1.concat(arr2);

console.log(arr3);
````
[ 1, 2, 3, 4, 5, 6 ]

````
let arr1 = [1,2,3];
let arr2 = [4,5,6];
let arr3 = [7,8,9];

let arr4 = arr1.concat(arr2,arr3);

console.log(arr4);
````
[1, 2, 3, 4, 5,6, 7, 8, 9]


**pop()**

Removes the last element.

````
let arr = ['html', 'css', 'js', 'react', 'angular'];

let removedIteam = arr.pop();

console.log(arr);
console.log(removedIteam);

removedIteam = arr.pop();

console.log(arr);
console.log(removedIteam);
````

[ 'html', 'css', 'js', 'react' ] <br/>
angular <br/>
[ 'html', 'css', 'js' ] <br/>
react <br/>

**slice()**

Syntax:

arr.slice(begin, end)

It's like cutting a big cake and taking a slice but it creates a shallow copy and returns it. Nothing happens with the original array.

````
let arr = ['html', 'css', 'js', 'react', 'angular'];

let removedIteam = arr.slice(1,4);

console.log(arr);
console.log(removedIteam);
````

[ 'html', 'css', 'js', 'react', 'angular' ] <br/>
[ 'css', 'js', 'react' ] <br/>


**splice()**

It works like slice but it does with the original array.

````
let arr = ['html', 'css', 'js', 'react', 'angular'];

let removedIteam = arr.splice(1,4);

console.log(arr);
console.log(removedIteam);
````

[ 'html' ] <br/>
[ 'css', 'js', 'react', 'angular' ] <br/>


**Add elements using Splice()**

I have used 3 for specifying where it should start from, 0 for delete nothing and 'node' for add node. This will add 'node' before 'react'.

````
let arr = ['html', 'css', 'js', 'react', 'angular'];

arr.splice(3,0, 'node');

console.log(arr);
````

[ 'html', 'css', 'js', 'node', 'react', 'angular' ]

**includes()**

````
let arr = ['html', 'css', 'js', 'react', 'angular'];

let user = 'node';

console.log(arr.includes(user));
````

false


**sort()**

````
let arr = ['a', 'c', 's', 'r', 'b'];

arr.sort();

console.log(arr);
````
[ 'a', 'b', 'c', 'r', 's' ]



