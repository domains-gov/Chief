---
title: BigUint64Array() constructor
slug: Web/JavaScript/Reference/Global_Objects/BigUint64Array/BigUint64Array
page-type: javascript-constructor
tags:
  - BigInt
  - Constructor
  - JavaScript
  - Reference
  - TypedArrays
browser-compat: javascript.builtins.BigUint64Array.BigUint64Array
---

{{JSRef}}

The **`BigUint64Array()`** typed array constructor creates a
new {{jsxref("BigUint64Array")}} object, which is, an array of 64-bit unsigned integers
in the platform byte order. If control over byte order is needed, use
{{jsxref("DataView")}} instead. The contents are initialized to `0n`. Once
established, you can reference elements in the array using the object's methods, or by
using standard array index syntax (that is, using bracket notation).

## Syntax

```js-nolint
new BigUint64Array()
new BigUint64Array(length)
new BigUint64Array(typedArray)
new BigUint64Array(object)

new BigUint64Array(buffer)
new BigUint64Array(buffer, byteOffset)
new BigUint64Array(buffer, byteOffset, length)
```

> **Note:** `BigUint64Array()` can only be constructed with [`new`](/en-US/docs/Web/JavaScript/Reference/Operators/new). Attempting to call it without `new` throws a {{jsxref("TypeError")}}.

### Parameters

See [`TypedArray`](/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray#parameters).

### Exceptions

See [`TypedArray`](/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray#exceptions).

## Examples

### Different ways to create a BigUint64Array

```js
// From a length
const biguint64 = new BigUint64Array(2);
biguint64[0] = 42n;
console.log(biguint64[0]); // 42n
console.log(biguint64.length); // 2
console.log(biguint64.BYTES_PER_ELEMENT); // 8

// From an array
const x = new BigUint64Array([21n, 31n]);
console.log(x[1]); // 31n

// From another TypedArray
const y = new BigUint64Array(x);
console.log(y[0]); // 21n

// From an ArrayBuffer
const buffer = new ArrayBuffer(64);
const z = new BigUint64Array(buffer, 8, 4);
console.log(z.byteOffset); // 8

// From an iterable
const iterable = function*() { yield* [1n, 2n, 3n]; }();
const biguint64FromIterable = new BigUint64Array(iterable);
console.log(biguint64FromIterable);
// BigUint64Array [1n, 2n, 3n]
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- [JavaScript typed arrays](/en-US/docs/Web/JavaScript/Typed_arrays)
- {{jsxref("BigInt64Array")}}
- {{jsxref("DataView")}}