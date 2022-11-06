# #100DaysOfCode Log - Round 1 

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