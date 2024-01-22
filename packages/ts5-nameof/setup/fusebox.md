# Using ts5-nameof with FuseBox

To use ts5-nameof with [FuseBox](https://github.com/fuse-box/fuse-box), specify it as a custom transformer:

```javascript
const tsNameof = require("ts5-nameof");

FuseBox.init({
  transformers: {
    before: [tsNameof],
  },
});
```
