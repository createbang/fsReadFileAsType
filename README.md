fsReadFileAsType
==============

Parse the contents of files as JavaScript objects.

.env file
```sh
VAR1=foobar
VAR2=bazbang
```

.jsonfile file
```json
{
  "foo": "bar",
  "baz": "bang"
}
```

js file
```js
var fsReadFileAsType = require('fsreadfileastype');

var jsonData = fsReadFileAsType.sync(__dirname + '/.jsonfile', 'json');
// returns {foo: "bar", baz: "bang"}
var shellVarData = fsReadFileAsType.sync(__dirname + '/.env', 'shell');
// returns {VAR1: "foo", VAR2: "bar"}
```
