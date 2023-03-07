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


