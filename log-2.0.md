# #100DaysOfCode Log 2.0

The log of my #100DaysOfCode challenge attempt 2. Starting on [January, 2nd, 2023]

# Log

First 30 days or so will focused around foundations of JS, React, HTML, CSS, inclusive of watching videos, reading docs, and completing small challenges

## R1D1 - *08.01.23*

* Watched Kent C. Dodds's Beginners Guide to React from egghead.io 
https://www.youtube.com/watch?v=7_x4AuqHxlg 

## R1D2 - *09.01.23*

* Completed JavaScript refresher of React - The Complete Guide (incl Hooks, React Router, Redux)

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

