---
title: Bitwise AND (&)
slug: Web/JavaScript/Reference/Operators/Bitwise_AND
page-type: javascript-operator
tags:
  - Bitwise operator
  - JavaScript
  - Language feature
  - Operator
  - Reference
browser-compat: javascript.operators.bitwise_and
---

{{jsSidebar("Operators")}}

The **bitwise AND (`&`)** operator returns a `1` in each bit
position for which the corresponding bits of both operands are `1`s.

{{EmbedInteractiveExample("pages/js/expressions-bitwise-and.html", "shorter")}}

## Syntax

```js-nolint
a & b
```

## Description

The operands are converted to 32-bit integers and expressed by a series of bits (zeroes
and ones). Numbers with more than 32 bits get their most significant bits discarded. For
example, the following integer with more than 32 bits will be converted to a 32-bit
integer:

```plain
Before: 11100110111110100000000000000110000000000001
After:              10100000000000000110000000000001
```

Each bit in the first operand is paired with the corresponding bit in the second
operand: _first bit_ to _first bit_, _second bit_ to _second
bit_, and so on.

The operator is applied to each pair of bits, and the result is constructed bitwise.

The truth table for the AND operation is:

| a   | b   | a AND b |
| --- | --- | ------- |
| 0   | 0   | 0       |
| 0   | 1   | 0       |
| 1   | 0   | 0       |
| 1   | 1   | 1       |

```plain
     9 (base 10) = 00000000000000000000000000001001 (base 2)
    14 (base 10) = 00000000000000000000000000001110 (base 2)
                   --------------------------------
14 & 9 (base 10) = 00000000000000000000000000001000 (base 2) = 8 (base 10)
```

Bitwise ANDing any number `x` with `-1` returns `x` converted to a 32-bit integer. Do not use `& -1` to truncate numbers to integers; use [`Math.trunc()`](/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/trunc#using_bitwise_no-ops_to_truncate_numbers) instead.

## Examples

### Using bitwise AND

```js
// 5: 00000000000000000000000000000101
// 2: 00000000000000000000000000000010
5 & 2; // 0
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- [Bitwise operators in the JS guide](/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#bitwise_operators)
- [Bitwise AND assignment operator](/en-US/docs/Web/JavaScript/Reference/Operators/Bitwise_AND_assignment)
