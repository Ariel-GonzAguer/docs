---
Title: 'normalize'
Description: 'Its a instance method of String that returns the Unicode Normalization Form of this string.'
Subjects:
  - 'Web Development'
Tags:
  - 'Strings'
  - 'JavaScript'
  - 'Methods'
CatalogContent:
  - 'paths/front-end-engineer-career-path'
---

Among the various instance methods that JavaScript has for String, we have **normalize**, which can take a Unicode Normalization Form as a parameter.

## Syntax

```javascript
normalize();
normalize(form);
```

### Parameters

One of _"NFC"_, _"NFD"_, _"NFKC"_, or _"NFKD"_, specifying the Unicode Normalization Form. If the parameter is omitted (or undefined), "NFC" is used.

Meaning of the parameters:

- NFC → Canonical Decomposition, followed by Canonical Composition.
- NFD → Canonical Decomposition.
- NFKC → Compatibility Decomposition, followed by Canonical Composition.
- NFKD → Compatibility Decomposition.

## Example

```javascript
const a = 'café';
const b = 'café'; // It looks the same, but the "é" is made up of two characters

console.log(a === b); // false

// solution with normalize
console.log(a.normalize() === b.normalize()); // true
```
