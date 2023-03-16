# shortid2

_ShortId_ (https://www.npmjs.com/package/shortid) has been an amazing module to generate short non-sequential url-friendly unique ids.
However it is no longer maintained and suggests using _NanoId_ (https://www.npmjs.com/package/nanoid) as replacement.

_NanoId_ is simple and straight forward. However, it is not a drop-in replacement. Specially places where _ShortId_ is a transient dependency.

This project uses _NanoId_ and provides same interface as _ShortId_ so that it can be used as drop-in resolution for transient dependencies.


### Usage

```js
const shortid = require('shortid2');

console.log(shortid.generate());
```

Mongoose Unique Id
```js
_id: {
  'type': String,
  'default': shortid.generate
},
```

### API

```js
const shortid = require('shortid2');
```

---------------------------------------

#### `shortid.generate()`

__Returns__ `string` non-sequential unique id.

__Example__

```js
users.insert({
  _id: shortid.generate(),
  name: '...',
  email: '...'
});
```

---------------------------------------