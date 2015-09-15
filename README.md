
quaint-javascript
=================

Allows inline JavaScript code in Quaint markup.

Expressions in curly brackets will be evaluated in JavaScript.

Usage:

```javascript
var quaint = require("quaint");
var qjs = require("quaint-javascript");

var q = quaint(qjs);

q.toHTML("2 + 3 = {2 + 3}")
// ==> "2 + 3 = 5"
```

In the JavaScript code, you can use the `h` function to create HTML
elements programmatically:

```javascript
q.toHTML("{h('a.cls#id', {href: 'there'}, 'A', 'B')}")
'<a href="there" id="id" class="cls">AB</a>'

q.toHTML("{[1, 2, 3].map(function (x) { return h('b', x); })}")
// ==> "<b>1</b><b>4</b><b>9</b>"
```

