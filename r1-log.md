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


## R1D4 - *04.11.22*