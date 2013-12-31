# rivets-server

Render [Rivets.js][rivets] templates on the server.

## Installation

  $ npm install rivets-server

## Usage

```javascript
var rivetsServer = require('rivets-server');
var template = '&lt;span rv-text="name"&gt;&lt;/span&gt;'
var data = {
  name: 'Anders'
};
rivetsServer.render(template, data, function (err, html) {
  // now, html == '&lt;span rv-text="name"&gt;Anders&lt;/span&gt;'
});
```

## Details

Conforms to the [Consolidate.js][consolidate] API.

Uses [jsdom] as a context for Rivets to bind.

By default, it currently uses [my fork of Rivets][my-rivets], which supports
restoring `if` and `each` bindings from Rivets on the client-side.
Vanilla Rivets can't currently persist or restore this information.


[my-rivets]: https://github.com/adjohnson916/rivets/tree/revival
[rivets]: http://www.rivetsjs.com/docs/ "Rivets.js"
[jsdom]: https://github.com/tmpvar/jsdom
[consolidate]: https://github.com/visionmedia/consolidate.js/
