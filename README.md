Ts-node Import Json File Issue Demo
===================================

### It works without `ts-node`:

```
npm install
npx tsc
node hello.js
```

It will print `{ name: 'ts-node' }`

### <s>It doesn't work with `ts-node`</s>

```
npm install
npx ts-node hello.ts
```

Error:

```
⨯ Unable to compile TypeScript:
hello.ts(1,23): error TS2307: Cannot find module './data.json'.
```

Update
------

Fix: add `"resolveJsonModule": true` to `tsconfig.json`, `ts-node` will work fine.

`resolveJsonModule` is supported from typescript 2.9.

Resources
---------

- issue discussion: https://github.com/TypeStrong/ts-node/issues/455