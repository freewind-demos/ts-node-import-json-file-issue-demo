Ts-node Import Json File Issue Demo
===================================

### It works without `ts-node`:

```
npm install
npx tsc
node hello.js
```

It will print `{ name: 'ts-node' }`

### It doesn't work with `ts-node`

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

If we use typescript 2.9+, we can add `"resolveJsonModule": true` to `tsconfig.json` to fix the problem.

But with older versions of typescript, the issue is still unresolved.

Resources
---------

- issue discussion: https://github.com/TypeStrong/ts-node/issues/455