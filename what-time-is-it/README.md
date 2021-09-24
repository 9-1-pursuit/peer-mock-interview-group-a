# What Time is It?

[Code Wars](https://www.codewars.com/kata/57729a09914da60e17000329/)

[Code Wars](https://www.codewars.com/kata/57729a09914da60e17000329)

## Problem

Given a time in AM/PM format as a string, convert it to military (24-hour) time as a string.

Midnight is 12:00:00AM on a 12-hour clock, and 00:00:00 on a 24-hour clock. Noon is 12:00:00PM on a 12-hour clock, and 12:00:00 on a 24-hour clock

Sample Input: 07:05:45PM Sample Output: 19:05:45

Try not to use built in DateTime libraries.

For more information on military time, check the wiki https://en.wikipedia.org/wiki/24-hour_clock#Military_time

## Possible Solution

```js
var getMilitaryTime = function (input) {
  const hour = input.substr(0, 2);
  const mins = input.substr(3, 2);
  const secs = input.substr(6, 2);
  const ampm = input.substr(-2, 2);

  if (hour === "12" && ampm === "AM") return `00:${mins}:${secs}`;
  else if (hour !== "12" && ampm === "PM")
    return `${parseInt(hour) + 12}:${mins}:${secs}`;
  else return `${hour}:${mins}:${secs}`;
};
```
