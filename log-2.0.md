# #100DaysOfCode Log 2.0

The log of my #100DaysOfCode challenge attempt 2. Starting on [January, 2nd, 2023]

# Log

First 30 days or so will focused around foundations of JS, React, HTML, CSS, inclusive of watching videos, reading docs, and completing small challenges

## R1D1 - *08.01.23*

* Watched Kent C. Dodds's Beginners Guide to React from egghead.io 
https://www.youtube.com/watch?v=7_x4AuqHxlg 

## R1D2 - *09.01.23*

* Completed JavaScript refresher module of React - The Complete Guide (incl Hooks, React Router, Redux)

* Challenges 1 and 2 of https://github.com/lydiahallie/javascript-questions?ref=java5cript.com

### CodeWars

Given a string of digits, you should replace any digit below 5 with '0' and any digit 5 and above with '1'. Return the resulting string.

Note: input will never be an empty string

```
function fakeBin(x){
  
  let str = ""
  
   x.split("").forEach((num) => 
      { parseInt(num) < 5 ?
     str += "0" :
     str  += "1"
   })
   
   return str
   
}
```
Refactored

```
function fakeBin(x) {
    return x.split('').map(n => n < 5 ? 0 : 1).join('');
}
```

## R1D2 - *10.01.23*

* Completed 80% of the React BAsics & Working with Components section of React - The Complete Guide (incl Hooks, React Router, Redux)
  
* Challenges 3 and 4 of https://github.com/lydiahallie/javascript-questions?ref=java5cript.com


### CodeWars

Make a program that filters a list of strings and returns a list with only your friends name in it.

If a name has exactly 4 letters in it, you can be sure that it has to be a friend of yours! Otherwise, you can be sure he's not...

Ex: Input = ["Ryan", "Kieran", "Jason", "Yous"], Output = ["Ryan", "Yous"]

i.e.

friend ["Ryan", "Kieran", "Mark"] `shouldBe` ["Ryan", "Mark"]
Note: keep the original order of the names in the output.


```
function friend(friends){
  return friends.filter(friend => friend.length === 4 )
}

```

## R1D3 - *11.01.23*