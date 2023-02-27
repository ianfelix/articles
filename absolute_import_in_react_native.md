# Absolute imports in Read Native

This is a short guide on how to use absolute imports in React Native.

## Absolute imports

The absolute imports are a feature that was introduced in ES2020. It allows you to import modules using an absolute path instead of a relative path.

For example, if you have a file called `App.js` in the `src` folder, you can import a module called `utils.js` using the following code:

```javascript
import { sum } from 'src/utils';
```

This is a simple example, but it can be very useful when you have a complex project with many files and folders.

## How to use absolute imports in React Native

To use absolute imports in React Native, you need to install the `babel-plugin-module-resolver` package.

```bash
yarn add -D babel-plugin-module-resolver
```

After installing the package, you need to configure it in the `babel.config.js` file.

```javascript
module.exports = {
  presets: ['babel-preset-expo'],
  plugins: [
    [
      'module-resolver',
      {
        root: ['./src'],
        alias: {
          '~/assets': './src/assets',
          '~/contexts': './src/contexts',
          '~/screens': './src/screens',
          '~/styles': './src/styles',
          '~/routes': './src/routes',
          '~/services': './src/services',
          '~/hooks': './src/hooks',
          '~/shared': './src/shared',
        },
      },
    ],
  ],
};
```

The `root` property is used to define the root folder of the project. In this case, it is the `src` folder.

The `alias` property is used to define the aliases that will be used in the imports. In this case, I defined the following aliases:

- `~/assets`: `./src/assets`
- `~/contexts`: `./src/contexts`
- `~/screens`: `./src/screens`
  ...

The aliases are used to import modules using the `~` character. For example, if you want to import the `App.js` file in the `screens` folder, you can use the following code:

```javascript
import App from '~/screens/App';
```

If you are using Typescript you will need to add the following code to the `tsconfig.json` file:

```json
{
  "compilerOptions": {
    "baseUrl": "./src",
    "paths": {
      "~/*": ["*"]
    }
  }
}
```

It is important to note that the `baseUrl` property must be the same as the `root` property in the `babel.config.js` file.

Now you will be able to use absolute imports in your React Native project.

Thank you for reading this article.
If you enjoy this article, please up vote and comment.

Follow me on:

- [Twitter](https://twitter.com/_ianfelix)
- [Github](https://github.com/ianfelix)
- [LinkedIn](https://www.linkedin.com/in/ian-felix)
