# Using ts5-nameof with Jest

1. Setup jest with [ts-jest](https://github.com/kulshekhar/ts-jest)

2. `npm install --save-dev ts5-nameof @types/ts5-nameof`

3. In _package.json_ specify...

```jsonc
{
  // ...
  "jest": {
    "globals": {
      "ts-jest": {
        "astTransformers": ["ts5-nameof"]
      }
    }
  }
}
```

...or in _jest.config.js_...

```ts
module.exports = {
  // ...
  globals: {
    "ts-jest": {
      "astTransformers": ["ts5-nameof"],
    },
  },
};
```
