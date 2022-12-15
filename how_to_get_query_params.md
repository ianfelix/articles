Use the property searchParams from URL interface to get the query params from a URL.

## Examples:

In the following example, we have a URL with name and lastname as query params.

```js
const url = new URL('https://example.com/path?name=Ian&lastname=Felix');

// using method get from searchParams

const name = url.searchParams.get('name');
const lastName = url.searchParams.get('lastname');

console.log(name); // 'Ian'
console.log(lastName); // 'Felix'

const myName = `${name} ${lastName}`;

console.log(myName); // 'Ian Felix' - this is my name :)
```

We can use some methods from the searchParams to help us to handle with the query params.

## Methods:

Below is a list of some methods from the searchParams property.

```ts
URL.searchParams.get();
// returns the value of the first query parameter with the given name

URL.searchParams.getAll();
// returns an array of all query parameters with the given name

URL.searchParams.has();
// returns true if the given query parameter exists

URL.searchParams.set();
// sets the value of the first query parameter with the given name
```

You can find more information about interfaces and type aliases in the official TypeScript documentation. - [MDN Docs](https://developer.mozilla.org/en-US/docs/Web/API/URLSearchParams#methods)

Thank you for reading this article.
If you enjoy this article, please upvote and comment.
Follow me on [Twitter](https://twitter.com/_ianfelix)
