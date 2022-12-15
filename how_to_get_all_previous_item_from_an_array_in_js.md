We can use two array methods to help us get the previous items from an array:

1. Matrix.indexOf()
2. Array.slice()

### Array.indexOf()

We use it to get the index of an item in an array. In our case, we want to get the index of the current item. Returns -1 if the item is not found.

### Array.slice()

We use it to get a part of an array. In our case, we want to get the previous items from the current item. Returns an empty array if the item is not found.

Example:

```js
const cars = ['Ford', 'Chevy', 'Honda', 'Toyota'];
const currentCar = 'Honda';
const index = cars.indexOf(currentCar); // two
const previousCars = cars.slice(0, index); // ['Ford', 'Chevy']
```

You can find more information about slice and indexOf type in the Mdn web docs. - [Mdn Docs - slice](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice#try_it) and [Mdn Docs - indexOf](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf#try_it)

Thanks for reading this article.
If you liked this article, please vote and comment.
Follow me on [Twitter](https://twitter.com/_ianfelix)
