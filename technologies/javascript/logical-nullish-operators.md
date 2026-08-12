# Logical and Nullish Coalescing Operators

## Logical Operators

### &&

If `a` is truthy, `b` is returned.
If `a` is falsy, `a` is returned.

#### Truthy Values / Falsy Values

Truthy values include:

- `[]`
- `{}`

Falsy values include:

- `false`
- `0`
- `""`
- `null`
- `undefined`
- `NaN`

### ||

If `a` is truthy, `a` is returned.
If `a` is falsy, `b` is returned.

#### Truthy Values / Falsy Values

Truthy and falsy values are the same as those for `&&`.

## Nullish Coalescing Operator

### ??

`??` returns `b` only when `a` is `null` or `undefined`.
Otherwise, `a` is returned.

#### Nullish Values

Nullish values include only:

- `null`
- `undefined`