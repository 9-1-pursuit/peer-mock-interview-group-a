# Century from Year

[Code Wars](https://www.codewars.com/kata/56efc695740d30f963000557/)

## Problem

The first century spans from the year 1 up to and including the year 100, The second - from the year 101 up to and including the year 200, etc.

Task :

Given a year, return the century it is in.

Input , Output Examples :

```js
1705 --> 18
1900 --> 19
1601 --> 17
2000 --> 20
```

## Possible Solution

```js
const century = (year) => Math.ceil(year / 100);
```
