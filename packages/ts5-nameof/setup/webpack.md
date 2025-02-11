# Using ts5-nameof with Webpack

## ts-loader / awesome-typescript-loader

If using [ts-loader](https://github.com/TypeStrong/ts-loader) or [awesome-typescript-loader](https://github.com/s-panferov/awesome-typescript-loader), specify ts5-nameof as a custom transformation like so in _webpack.config.js_:

```ts
const tsNameof = require("ts5-nameof");

module.exports = {
  // ...etc...
  module: {
    rules: [{
      test: /\.tsx?$/,
      use: [{
        loader: "ts-loader", // or awesome-typescript-loader
        options: {
          getCustomTransformers: () => ({ before: [tsNameof] }),
        },
      }],
    }],
  },
};
```
