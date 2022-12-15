# How to invert a string

First, we need to transform the string into a list of characters. We can use the split() method to do that.

```js
const str = 'Hello World';
const chars = str.split('');
console.log(chars); // ['H', 'e', 'l', 'l', 'o', ' ', 'W', 'o', 'r', 'l', 'd']
```

Then, we need to reverse the list of characters. We can use the reverse() method to do that.

```js
const chars = ['H', 'e', 'l', 'l', 'o', ' ', 'W', 'o', 'r', 'l', 'd'];
const reversedChars = chars.reverse();
console.log(reversedChars); // ['d', 'r', 'l', 'o', ' ', 'W', 'o', 'r', 'l', 'o', 'e', 'l', 'l', 'H']
```

Finally, we need to join the list of characters back into a string. We can use the join() method to do that.

```js
const reversedChars = [
  'd',
  'r',
  'l',
  'o',
  ' ',
  'W',
  'o',
  'r',
  'l',
  'o',
  'e',
  'l',
  'l',
  'H',
];
const reversedStr = reversedChars.join('');
console.log(reversedStr); // 'dlrow olleH'
```

So, we have a string that is the reverse of the original string.

```js
const str = 'Hello World';
const reversedStr = str.split('').reverse().join('');
console.log(reversedStr); // 'dlrow olleH'
```
