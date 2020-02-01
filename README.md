# rdlevel - rdlevel parser

This is a parser for the .rdlevel format, which is just JSON.

It does a two stage process:

 - first, it tries to parse with the normal `JSON.parse`. Modern RD levels are JSON-compliant.
 - if that doesn't work, it uses a modified JSON5 parser. Older RD levels are JSON-ish but have some weirdness.

# how to use

```
const RDLevel = require('rdlevel');
RDLevel.parse(...);
```