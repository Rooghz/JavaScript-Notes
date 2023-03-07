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

Spread Operator 

````
let arr1 = [1,2,3];
let arr2 = [...arr1];

console.log(arr1);
console.log(arr2);

arr2.push(4);

console.log('updated arr1-',arr1);
console.log('updated arr2-',arr2);

````

[ 1, 2, 3 ]
[ 1, 2, 3 ]
updated arr1- [ 1, 2, 3 ]
updated arr2- [ 1, 2, 3, 4 ]
