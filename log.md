# #100DaysOfCode Log 

The log of my #100DaysOfCode challenge. Starting on [November, 1st, 2022].

# Log

## R1D1 - *01.11.22*

Started a GitHub log for the 100DaysOfCode challenge - I'm thinking this counts. Planned some resources and learning for the challenge. Completed a CodeWars challenge. 

### CodeWars
Complete the square sum function so that it squares each number passed into it and then sums the results together.

```
function squareSum(numbers){
  return numbers.reduce((sum,num) => sum + (num * num), 0);
}
```

## R1D2 - *02.11.22*

Wanting to sharpen my fundamentals so starting with beginners guides to ReactJS, vanilla JavaScript and the react beta docs, which will be my focus for this round of the challenge.

https://beta.reactjs.org/learn read through and noted the quick start guide in the beta reactjs documentation. 

### CodeWars
Alex just got a new hula hoop, he loves it but feels discouraged because his little brother is better than him

Write a program where Alex can input (n) how many times the hoop goes round and it will return him an encouraging message 

If Alex gets 10 or more hoops, return the string "Great, now move on to tricks".
If he doesn't get 10 hoops, return the string "Keep at it until you get it".

```
function hoopCount (n) {
  return n >= 10 ? "Great, now move on to tricks" : "Keep at it until you get it";
}
```

## R1D3 - *03.11.22*

Continuing with React beta docs, read over and made notes about the Thinking in React section.

### CodeWars
Trolls are attacking your comment section!

A common way to deal with this situation is to remove all of the vowels from the trolls' comments, neutralizing the threat.

Your task is to write a function that takes a string and return a new string with all vowels removed.

For example, the string "This website is for losers LOL!" would become "Ths wbst s fr lsrs LL!".

Note: for this kata y isn't considered a vowel.

```
function disemvowel(str) {
  
  let disemvowelledStr = "";
 
  str.split("").filter((letter) => {
    if (!"aeiou".includes(letter.toLowerCase())) {
      disemvowelledStr += letter; 
    }
  })
  
  return disemvowelledStr
}
```

Refactored with regex

```
function disemvowel(str) {
  return str.replace(/[aeiou]/gi, '');
}
```

## R1D4 - *04.11.22*

Lazy day, just plodded along with a codewars

### CodeWars

Your start-up's BA has told marketing that your website has a large audience in Scandinavia and surrounding countries. Marketing thinks it would be great to welcome visitors to the site in their own language. Luckily you already use an API that detects the user's location, so this is an easy win.

The Task
Think of a way to store the languages as a database (eg an object). The languages are listed below so you can copy and paste!
Write a 'welcome' function that takes a parameter 'language' (always a string), and returns a greeting - if you have it in your database. It should default to English if the language is not in the database, or in the event of an invalid input.

Possible invalid inputs include:
```
IP_ADDRESS_INVALID - not a valid ipv4 or ipv6 ip address
IP_ADDRESS_NOT_FOUND - ip address not in the database
IP_ADDRESS_REQUIRED - no ip address was supplied
```

```
const database = {
english: 'Welcome',
czech: 'Vitejte',
danish: 'Velkomst',
dutch: 'Welkom',
estonian: 'Tere tulemast',
finnish: 'Tervetuloa',
flemish: 'Welgekomen',
french: 'Bienvenue',
german: 'Willkommen',
irish: 'Failte',
italian: 'Benvenuto',
latvian: 'Gaidits',
lithuanian: 'Laukiamas',
polish: 'Witamy',
spanish: 'Bienvenido',
swedish: 'Valkommen',
welsh: 'Croeso'
}

function greet(language) {
return database[language] || "Welcome";
}
```

## R1D5 - *05.11.22*

Another lazy day plodding along with a codewars

### CodeWars

When provided with a number between 0-9, return it in words.

Input :: 1

Output :: "One".

```
function switchItUp(number){
  const dictionary = { 0: "Zero", 1: "One", 2: "Two", 3: "Three", 4:"Four", 5: "Five", 6: "Six", 7: "Seven", 8: "Eight", 9:"Nine" }
  return dictionary[number];
}
```
refactored
```
function switchItUp(n){
  return ["Zero","One","Two","Three","Four","Five","Six","Seven","Eight","Nine"][n]
}
```

## R1D6 - *06.11.22*

Started note taking on Describing the UI section of beta docs. Completed 2 codewars challenges. 

### CodeWars

Count the number of divisors of a positive integer n.

Random tests go up to n = 500000.

Examples (input --> output)
4 --> 3 (1, 2, 4)
5 --> 2 (1, 5)
12 --> 6 (1, 2, 3, 4, 6, 12)
30 --> 8 (1, 2, 3, 5, 6, 10, 15, 30)
Note you should only return a number, the count of divisors. The numbers between parentheses are shown only for you to see which numbers are counted in each case.

```
function getDivisorsCnt(n){
  let divisors =0
  
  for (let i=1; i<=n; i++) {
    if (n % i == 0) {
      divisors += 1
    }
  }
  return divisors
}
```

Deoxyribonucleic acid, DNA is the primary information storage molecule in biological systems. It is composed of four nucleic acid bases Guanine ('G'), Cytosine ('C'), Adenine ('A'), and Thymine ('T').

Ribonucleic acid, RNA, is the primary messenger molecule in cells. RNA differs slightly from DNA its chemical structure and contains no Thymine. In RNA Thymine is replaced by another nucleic acid Uracil ('U').

Create a function which translates a given DNA string into RNA.

For example:

"GCAT"  =>  "GCAU"
The input string can be of arbitrary length - in particular, it may be empty. All input is guaranteed to be valid, i.e. each input string will only ever consist of 'G', 'C', 'A' and/or 'T'.

```
function DNAtoRNA(dna) {
  let rna =""
  dna.split("").forEach((letter) => {
    if(letter === "T") {
      letter = "U"
    }
    rna += letter
  })
  return rna
}
```

Refactored with regex

```
function DNAtoRNA(dna){
  return dna.replace(/T/g, 'U');
}
```

## R1D7 - *07.11.22*

Read up on exports and imports from the react beta docs, completed some codewars, brushed up on some interview questions https://github.com/sudheerj/reactjs-interview-questions#what-is-react 

### CodeWars

In this Kata we are passing a number (n) into a function.

Your code will determine if the number passed is even (or not).

The function needs to return either a true or false.

Numbers may be positive or negative, integers or floats.

Floats with decimal part non equal to zero are considered UNeven for this kata.

```
function testEven(n) {
  return n % 2 == 0
}
```

Bob needs a fast way to calculate the volume of a cuboid with three values: the length, width and height of the cuboid. Write a function to help Bob with this calculation.

```
class Kata {
  static getVolumeOfCuboid(length, width, height) {
   return length * width * height;
  }
}
```

## R1D8 - *08.11.22*

Code wars task, also article on alternative way https://medium.com/@matthewvondanger/simple-encryption-alternating-split-5d10af44df57 

### CodeWars

Implement a pseudo-encryption algorithm which given a string S and an integer N concatenates all the odd-indexed characters of S with all the even-indexed characters of S, this process should be repeated N times.

Examples:

encrypt("012345", 1)  =>  "135024"
encrypt("012345", 2)  =>  "135024"  ->  "304152"
encrypt("012345", 3)  =>  "135024"  ->  "304152"  ->  "012345"

encrypt("01234", 1)  =>  "13024"
encrypt("01234", 2)  =>  "13024"  ->  "32104"
encrypt("01234", 3)  =>  "13024"  ->  "32104"  ->  "20314"
Together with the encryption function, you should also implement a decryption function which reverses the process.

If the string S is an empty value or the integer N is not positive, return the first argument without changes.

```
function encrypt(text, n) {
  if (!text || n <= 0) return text; 
  while (n--) {
    let ans = '';
    for (let i = 1; i < text.length; i += 2) {
      ans += text[i];
    }
    for (let i = 0; i < text.length; i += 2) {
      ans += text[i];
    }
    text = ans;
  }
  return text;
}

function decrypt(encryptedText, n) {
  if (!encryptedText || n <= 0) return encryptedText;
  const ans = new Array(encryptedText.length);
  while (n--) {
    let j = 0;
    for (let i = 1; i < ans.length; i += 2) {
      ans[i] = encryptedText[j++];
    }
    for (let i = 0; i < ans.length; i += 2) {
      ans[i] = encryptedText[j++];
    }
    encryptedText = ans.join('');
  }
  return encryptedText;
}
```

## R1D9 - *09.11.22*

Code wars task

### CodeWars

Write function bmi that calculates body mass index (bmi = weight / height2).

if bmi <= 18.5 return "Underweight"

if bmi <= 25.0 return "Normal"

if bmi <= 30.0 return "Overweight"

if bmi > 30 return "Obese"

```
function bmi(weight, height) {
  const bmiAmount = weight / (height**2)
  if (bmiAmount <=18.5) {
    return "Underweight"
  } else if (bmiAmount <=25) {
    return "Normal"
  } else if (bmiAmount <=30) {
    return "Overweight"
  } else {
    return "Obese"
  }
}
```
switch case method:
```
function bmi(weight, height) {
 let bmiAmount = weight / (height * height);
 switch(true){
   case bmiAmount <= 18.5:
     return "Underweight";
   case bmiAmount <= 25.0:
     return "Normal";
   case bmiAmount <= 30.0:
     return "Overweight";
   case bmiAmount > 30:
     return "Obese";
  }
}
```

## R1D10 - *10.11.22*

Lots of react reading 

## R2D11 - *11.11.22*
Time to start a course of learning - React - The Complete Guide (incl Hooks, React Router, Redux) Course on Udemy.

Completed half of Section 3

## Weekend off

## R2D12 - *14.11.22*

Just some codewars today

### CodeWars

Write a function named setAlarm which receives two parameters. The first parameter, employed, is true whenever you are employed and the second parameter, vacation is true whenever you are on vacation.

The function should return true if you are employed and not on vacation (because these are the circumstances under which you need to set an alarm). It should return false otherwise. Examples:

setAlarm(true, true) -> false
setAlarm(false, true) -> false
setAlarm(false, false) -> false
setAlarm(true, false) -> true

```
function setAlarm(employed, vacation){
  return employed && !vacation
}
```

You get an array of numbers, return the sum of all of the positives ones.

Example [1,-4,7,12] => 1 + 7 + 12 = 20

Note: if there is nothing to sum, the sum is default to 0.

```
function positiveSum(arr) {
  let sum = 0
  arr.forEach((item) => { if (item > 0) {sum+=item} })
  return sum
}
```

alternative

```
function positiveSum(arr) {
  return arr.filter(x => x > 0).reduce((a, b) => a+b, 0);
}
```

## R2D13 - *15.11.22*

More codewars today & reading of react beta docs - writing markup in jsx

### CodeWars

Given two numbers and an arithmetic operator (the name of it, as a string), return the result of the two numbers having that operator used on them.

a and b will both be positive integers, and a will always be the first number in the operation, and b always the second.

The four operators are "add", "subtract", "divide", "multiply".

A few examples:(Input1, Input2, Input3 --> Output)

5, 2, "add"      --> 7
5, 2, "subtract" --> 3
5, 2, "multiply" --> 10
5, 2, "divide"   --> 2.5
Try to do it without using if statements!

```
function arithmetic(a, b, operator){
  const operations = {"add": "+", "subtract": "-", "multiply": "*", "divide": "/"}
  return eval(a + operations[operator] + b)
}
```

Alternative:
```
const arithmetic = (a, b, operator) => ({
  'add'     : a + b,
  'subtract': a - b,
  'multiply': a * b,
  'divide'  : a / b
}[operator]);
```

## R2D14 - *16.11.22*

More codewars today & read react docs JavaScript in JSX with Curly Braces section

### CodeWars

Complete the function that takes two integers (a, b, where a < b) and return an array of all integers between the input parameters, including them.

For example:

a = 1
b = 4
--> [1, 2, 3, 4]

```
function between(a, b) {
  let arr = []
  for(let i=a; i<=b; i++) {
    arr.push(i)
  }
  return arr
}
```