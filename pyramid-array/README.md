# Pyramid Array

[Code Wars](https://www.codewars.com/kata/515f51d438015969f7000013)

## Problem

Write a function that when given a number >= 0, returns an Array of ascending length subarrays.

```js
pyramid(0) => [ ]
pyramid(1) => [ [1] ]
pyramid(2) => [ [1], [1, 1] ]
pyramid(3) => [ [1], [1, 1], [1, 1, 1] ]
```

Note: the subarrays should be filled with 1s

## Possible Solution

```js
function pyramid(n) {
  const row = [];
  for (let i = 1; i <= n; i++) {
    row.push(Array(i).fill(1));
  }
  return row;
}
```
