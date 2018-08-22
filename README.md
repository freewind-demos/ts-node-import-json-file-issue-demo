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

Resources
---------

