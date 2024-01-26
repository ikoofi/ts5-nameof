# ts5-nameof.macro


## Setup

1. Install dependencies:

```
npm install --save-dev babel-plugin-macros ts5-nameof.macro
```

2. Ensure `babel-plugin-macros` is properly setup ([Instructions](https://github.com/kentcdodds/babel-plugin-macros/blob/master/other/docs/user.md)).

3. Import and use the default export. For example:

```ts
import nameof from "ts5-nameof.macro";

nameof(window.alert);
```

Transforms to:

```ts
"alert";
```

## Transforms

[Read here](https://github.com/dsherret/ts5-nameof/blob/master/README.md)

## Other

- [Contributing](https://github.com/dsherret/ts5-nameof/blob/master/CONTRIBUTING.md)
- [Development](https://github.com/dsherret/ts5-nameof/blob/master/DEVELOPMENT.md)
