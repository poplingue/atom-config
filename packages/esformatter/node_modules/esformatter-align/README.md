# esformatter-align

[esformatter](https://github.com/millermedeiros/esformatter) plugin for alignment.



## Usage

install it:

```sh
npm install esformatter-align
```

and add to your esformatter config file:

```json
{
  "plugins": [
    "esformatter-align"
  ]
}
```

## Alignments

### VariableDeclarations

input:

```js
var longer = require('hello');
var small = require('hello');
var muchlonger = require('hello');
```

output:

```js
var longer     = require('hello');
var small      = require('hello');
var muchlonger = require('hello');
```

### ObjectExpressions

input:

```js
var x = {
  a: 5,
  bla: ''
};
```

output:

```js
var x = {
  a:   5,
  bla: ''
};
```

### AssignmentExpressions

input:

```js
foo = 'bar';
fooooooo = 'baz';
```

output:

```js
foo      = 'bar';
fooooooo = 'baz';
```

### TernaryExpression

input:

```js
foo ? x : 'bar';
fooooooo ? y : 'baz';
```

output:

```js
foo      ? x : 'bar';
fooooooo ? y : 'baz';
```

### OrExpression

input:

```js
foo || x || 'bar';
fooooooo || yy || 'baz';
```

output:

```js
foo      || x  || 'bar';
fooooooo || yy || 'baz';
```

## Config

Optionally disable alignment of specific expressions

```js
{
  "esformatter": {
    // ...
  },
  "indent": {
    // ...
  },
  "align": {
    "ObjectExpression":     1,
    "VariableDeclaration":  1,
    "AssignmentExpression": 1,
    "TernaryExpression":    0,
    "OrExpression":         0
  },
  // ...
}
```

## License

Released under the [MIT License](http://opensource.org/licenses/MIT).

