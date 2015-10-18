serialport-1
============

A re-export of `serialport@1`.

Use
-----

Instead of `require('serialport')`, use `require('serialport-1')`

This allows you to depend on either serialport@1 or serialport@2 depending on which installs successfully:

```
var serialport
try {
    serialport = require('serialport-2');
} catch (e) {
    if (e.code != 'MODULE_NOT_FOUND') throw e;

    serialport = require('serialport-1');
}
```
