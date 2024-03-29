---
title: Bitwise XOR assignment (^=)
slug: Web/JavaScript/Reference/Operators/Bitwise_XOR_assignment
page-type: javascript-operator
tags:
  - Assignment operator
  - JavaScript
  - Language feature
  - Operator
  - Reference
browser-compat: javascript.operators.bitwise_xor_assignment
---

{{jsSidebar("Operators")}}

The **bitwise XOR assignment (`^=`)** operator uses the binary representation of
both operands, does a bitwise XOR operation on them and assigns the result to the
variable.

{{EmbedInteractiveExample("pages/js/expressions-bitwise-xor-assignment.html", "shorter")}}

## Syntax

```js-nolint
x ^= y // x = x ^ y
```

## Examples

### Using bitwise XOR assignment

```js
let a = 5; // (00000000000000000000000000000101)
a ^= 3; // (00000000000000000000000000000011)

console.log(a); // 6 (00000000000000000000000000000110)

let b = 5; // (00000000000000000000000000000101)
b ^= 0; // (00000000000000000000000000000000)

console.log(b); // 5 (00000000000000000000000000000101)
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- [Assignment operators in the JS guide](/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#assignment_operators)
- [Bitwise XOR operator](/en-US/docs/Web/JavaScript/Reference/Operators/Bitwise_XOR)
