# `stratic-extract-header`

[![Greenkeeper badge](https://badges.greenkeeper.io/straticjs/stratic-strip-header.svg)](https://greenkeeper.io/)

[remark][1] plugin to strip out a standard [Stratic][2] header

## Installation

    npm install stratic-strip-header

## Usage

```js
var remark = require('remark');
var stripHeader = require('stratic-strip-header');

var processor = remark().use(stripHeader);

var doc = processor.process([
    '# Post information',
    '"Title", "0 UTC-0","Jane Doe", "some, categories"',
	'# Post text',
	'Some arbitrary Markdown content'
].join('\n'));

console.log(doc);
```

Outputs:

```
Some arbitrary Markdown content

```

## License

LGPL 3.0+

## Author

Alex Jordan <alex@strugee.net>

 [1]: https://github.com/wooorm/remark
 [2]: https://github.com/strugee/generator-stratic
