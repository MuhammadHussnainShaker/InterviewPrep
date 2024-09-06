# InterviewPrep

A repository to store resource to prepare for JS interviews.

## React Topics
### useEffect
useEffect aik React ka hook hai jo jab bhi kisi component ka render hota hai ya uska koi data ya state change hota hai, us waqt kuch kaam karne ke liye use hota hai. Yeh aik tareeqa hai kisi bhi function ko chalane ka jab bhi koi zaroori cheez tabdeel hoti hai ya jab component pehli dafa load hota hai.

## JavaScript Topics

### Closures in JS

[Redo] The concept that enables inner function to have access to variables and function of outer function is known as closure in JavaScript.

### Hoisting in JS
JavaScript Hoisting refers to the process whereby the interpreter appears to move the declaration of functions, variables, classes, or imports to the top of their scope, prior to execution of the code.

### Why do we use state variable instead of simple variable in React.js
Because changes in state variable initiates re-render which would not have possible with simple variable.

### Higher Order Functions
The function that can accept functions as parameters or return functions as a result.

## HTML

## CSS

## OOP

## DSA

### Linked List

#### Singly

#### Doubly

Time complexity between array and linked list.

### Stack vs Queue or LIFI vs FIFO or DFS vs BFS

## SQL

SELECT \* FROM Student WHERE student_name = 'ahmed'

## PS

### How do you reverse a string?

```js
let str1 = "abcef"
let revStr1 = str1.split("").reverse().join("")
console.log(revStr1)
```

### How do you determine if a string is a palindrome?

```js
if (str1 === revStr1) {
  console.log("Palindrom")
} else {
  console.log("Not Palindrom")
}
```

### Find the number of occurrences of a character in a String?

```js
let str = "abcdcc"
let char = "c"

let count = 0
let position = str.indexOf(char)

while (position !== -1) {
  count++
  position = str.indexOf(char, position + 1)
}

console.log(count) // count = 2
```

### How to find out if the given two strings are anagrams or not?

```js
let str1 = "silent"
let str2 = "listen"

let sortedStr1 = str1.split("").sort().join("")
let sortedStr2 = str2.split("").sort().join("")

if (str1.length !== str2.length) {
  console.log("Not Anagrams!")
} else {
  if (sortedStr1 === sortedStr2) {
    console.log("Anagrams")
  } else {
    console.log("Not Anagrams")
  }
}
```

### How do you calculate the number of vowels and consonants in a String?

```js
let string = "aeioucd"

let vowels = 0
let consonants = 0
string = string.toLowerCase()

for (let index = 0; index < string.length; index++) {
  let char = string[index]
  if (char >= "a" && char <= "z") {
    if (
      string[index] === "a" ||
      string[index] === "e" ||
      string[index] === "i" ||
      string[index] === "o" ||
      string[index] === "u"
    ) {
      vowels++
    } else {
      consonants++
    }
  }
}
console.log(`No. of Vowels: ${vowels}. No. of Consonants ${consonants}`) // logs: No. of Vowels: 5. No. of Consonants 2
```

### How would you swap two numbers without using a third variable?

```js
let b = 10
let a = 20
a = a + b //30
b = a - b //10
a = a - b //20
console.log(`a: ${a}, b: ${b}`)
// OR
b = b + a //70
a = b - a //40
b = b - a //30
console.log(`a: ${a}, b: ${b}`)
```

### How do you find the factorial of an integer?

```js
function factorial (n) {
   return n === 0 || n === 1 ? 1 : n * factorial(n - 1)
}
console.log(factorial(4));
```

### Write a function to calculate factorial of a number without recursion?

```js
let n = 4
let fact = 1

while (n > 0) {
  fact = fact * n
  n--
}

console.log("Factorial of the number is: ", fact)
```

### How do you remove all occurrences of a given character from the input string?

```js
let str = 'abcd'
let newStr = str.replace("b", "")
console.log(newStr)
```

### How do you get the matching elements in an integer array?

```js
function matchingElements (arr) {
  for (let i = 0; i < arr.length; i++) {
    for (let j = i + 1; j < arr.length; j++) {
      if (arr[i] === arr[j]) {
        console.log(arr[i]);
      }
    }
  }
}
(matchingElements([1, 2, 3, 5, 3])) // 3
```

### How do you check if a number is prime or not?
```js
function isPrime(n) {
  if (n === 0 || n === 1) {
    return false // 0 and 1 are not prime numbers
  }
  if (n === 2) {
    return true // 2 is a prime number
  }
  
  for (let i = 2; i <= Math.sqrt(n); i++) {
    if (n % i === 0) {
      return false
    }
  }
  return true
}
console.log(isPrime(13))
```

### Write a fuction that takes an array of numbers and returns duplicate elements in new array
```js
function findDuplicate (inputArray) {
  let finalArray = []

  for (let i = 0; i < inputArray.length; i++) {

    for(let j = i + 1; j < inputArray.length; j++) {
      if (inputArray[i] === inputArray[j]) {
        finalArray.push(inputArray[i])
      }
    }
  }
  return finalArray
}

console.log(findDuplicate([1, 3, 2, 4, 4, 5, 6, 6]))

// unbelieveable
```

### Write a function that takes an array of numbers and return sum of unique number
```js
function sumOfUniqueNumbers(inputArray) {
  let sum = 0
  for (let i = 0; i < inputArray.length; i++) {
    if (inputArray[i] === 0) continue
    for (let j = i + 1; j < inputArray.length; j++) {
      if (inputArray[i] === inputArray[j]) {
        inputArray[i]=0
        inputArray[j]=0
      }
    }
  }
  let finalArray = inputArray.map((value)=>sum+=value)

  return sum
}
console.log(sumOfUniqueNumbers([1, 2, 3, 4, 3,4]))

// unbelieveable
```
