# Development

## Building

Open the root directory of the repo and run:

```bash
# install dependencies
yarn install
# build
yarn build
```

## Packages

- [packages/babel-plugin-ts5-nameof](packages/babel-plugin-ts5-nameof) - Transform plugin for Babel.
- [packages/common](packages/common) - Common code used by almost everything.
- [packages/scripts-common](packages/scripts-common) - Common scripts used by other packages.
- [packages/tests-common](packages/tests-common) - Tests used by some packages. Write all your transform tests here.
- [packages/transforms-babel](packages/transforms-babel) - Transforms from the Babel AST to the Common AST.
- [packages/transforms-common](packages/transforms-common) - Nameof transforms done in the Common AST.
- [packages/transforms-ts5](packages/transforms-ts5) - Transforms from the TypeScript AST to the Common AST.
- [packages/ts5-nameof](packages/ts5-nameof) - ts5-nameof library for the TypeScript compiler.
- [packages/ts5-nameof.macro](packages/ts5-nameof) - ts5-nameof.macro library for Babel macros.

## Standard Commands

```bash
# build (run in root dir)
yarn build
# run tests (run in root dir)
yarn test
# format the code (download dprint from dprint.dev)
dprint fmt
```

### Clean Rebuild

```
yarn clean && yarn build
```

## Declaration File

### Global Definitions

The global definitions are stored in [lib/global.d.ts](lib/global.d.ts). To make changes:

1. Add a failing test in [lib/global.tests.ts](lib/global.tests.ts) (failing test means you get a compile error)
2. Update [lib/global.d.ts](lib/global.d.ts).
3. Run `yarn create-declaration-file` in the root directory

### ts5-nameof - Updating API

1. Update [packages/ts5-nameof/lib/declarationFileTests.ts](packages/ts5-nameof/lib/declarationFileTests.ts) with a failing test.
2. Update the API in [packages/ts5-nameof/src/main.ts](packages/ts5-nameof/src/main.ts).
3. Run `yarn create-declaration-file` in the root directory

## After Development

Run the following command in the root directory, which will check that everything is good:

```bash
yarn verify
```
