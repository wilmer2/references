# Javascripot

## functors
```js
const Functor = value => ({
  map: fn => Functor(fn(value)),
  valueOf: () => value, // used for arithmetic operators
  toString: () => `Functor(${value})`
});
```
