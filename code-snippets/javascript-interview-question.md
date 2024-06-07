**1. What is the output of this code?**
```
##Question
let a = {};
let b = { key: "b" };
let c = { key: "c" };

a[b] = 123;
a[c] = 456;

console.log(a[b]);
```

Answer: Output code will be 456, the values of the properties are being set to the number 123 and 456. It logs the value of 456 because it uses the latest value.

So the object looks like
```
{
    "[object Object]": 456
}
```

**2.What is the output of this code?**
```
let obj1 = { key: "value" };
let obj2 = obj1;
let obj3 = obj2;

obj1.key = "new value";
obj2 = { key: "another value" };

console.log(obj1.key, obj2.key, obj3.key);
```

Output
```
"new value", "another value", "new value"
```

**Explanation**:
This is because when an object is assigned to a variable, the variable stores a reference to the object in memoryu rather than the object itself.


**3. Guess the output of this code**
```
const arr = [1, 2, 3, 4, 5];

for (var i = 0; i < arr.length; i++) {
  setTimeout(function () {
    console.log(i);
  }, 1000);
}
```

Output
````
5
5
5
5
5
````

**Explanation**
The setTimeout function is called inside of a loop that iterates through element in the arr array. The setTimeout function will execue its callback function after a delay of 1000 millisecond, but at the time the loop will already be completed hence the 5


**4. Guess the output of this code**
```
let a = {
  x: 1,
  y: 2,
};
let b = a;
a.x = 5;
console.log(a);
console.log(b);
```

Output
```
{x:5, y:2} {x:5, y:2}
```
JS objects are passed by reference. So when we assigned a object to b. b is also poining to the same object in memory.

**5, what is the output of this code**
```
let num = 0;
function test(){
    var num = 1;
    return num;
}

console.log(test())
console.log(num)
```

Output
```
1
0
```

**Explanation**: The num inside is a global variable, while the num in test is not.


**6.Write a function in JS that takes an array of strings as input and returns a new array with the strings sorted in Alphabetical Order.**

```
function removeVowels(str){
    const vowels =  ["a", "e", "i", "o", "u", "A", "E", "I", "O", "U"];
    let newStr = "";
    for(let i = 0; i < str.length; i++){
        if(!vowels.includes(str[i])){
            newStr += str[i]
        }
    }

    return newStr
}

console.log(removeVowels(str))
```


**Explanation**: The num inside is a global variable, while the num in test is not.


**7.Write a function in JS that find the second highest number in array of numbers.**

```
function findSecondHighest(arr){
    const sortedArr = arr.sort((a,b) => b - a)

    return sortedArr[1]
    console.log(findSecondHighest(numbers));
}
        
```


**8.Write a function in JS that converts a given string to tile case.**

```
function toTitleCase(str) {
  return str.replace(/\b\w+/g, function (word) {
    return word.charAt(0).toUpperCase() + word.slice(1).toLowerCase();
  });
}

// Example usage:
console.log(toTitleCase("the quick brown fox")); // Output: 'The Quick Brown Fox'
        
```

**9, what is the output of this code**
```
const arr1 = [1, 2, 3];
const arr2 = [4, 5, 6];
const arr3 = [...arr1, ...arr2];
console.log(arr3);
```

Output
```
[1,2,3,4,5,6]
```

**Explanation**: The ... operator can be used to spread the elements of an array or the properties of an object into a new array or object.

**10, what is the output of this code**
```
const arr1 = [1, 2, 3];
const arr3 = [...arr1];
arr3.push(4);


console.log(arr1);
console.log(arr3);

```

Output
```
[1,2,3]
[1,2,3,4]
```

**Explanation**: The code creates an array arr1 with the values [1, 2, 3]. It then creates a new array arr2 using the spread syntax (...) to spread the values of arr1 into a new array.

**11, what is the output of this code**
```
const x = 10;

function foo() {
  console.log(x);
  const x = 20;
}

foo();

```

Output
```
ReferenceError: Cannot access 'x' before initialization
```

**Explanation**: The foo function attempts to log the value of x before it is initialized. This causes a ReferenceError to be thrown, as x is not yet defined in the function scope.

**12, what is the output of this code**
```
const person = {
  name: "John",
  age: 30,
};

Object.freeze(person);
person.age = 40;

console.log(person.age);
```

Output
```
30
```

**Explanation**: Using Object.freeze ensures that the object remains constant and its properties are protected from modification

**14, what is the output of this code**
```
const obj = {
  a: 1,
  b: 2,
  c: {
    a: 3,
    b: 4,
  },
};

const {
  a,
  b,
  c: { a: nestedA },
} = obj;

console.log(a, b, nestedA);
A: 1 2 3
```

Output
```
Answer: A: 1 2 3
```

**Explanation**: This code snippet uses destructuring assignment to extract values from the obj object. It extracts the properties a, b, and the nested property a from the c object and assigns them to the corresponding variables a, b, and nestedA, respectively.

After destructuring, the variables will hold the following values:

a: 1 (value of obj.a)
b: 2 (value of obj.b)
nestedA: 3 (value of obj.c.a)


**15, what is the output of this code**
```
let numbers = [1, 2, 3, 4, 5];
numbers = numbers.map((number) => number * 2);
console.log(numbers.reduce((total, num) => total + num));
```

Output
```
30
```

**Explanation**: The map() method is used to create a new array by applying a function to eache element which in this case is doubling it
- the reudce method is used to reduce the array to a single value by applying a function