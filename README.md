### jsfmt
---
https://github.com/rdio/jsfmt

http://rdio.github.io/jsfmt/
```js
var jfmt = require('jsfmt');
var fs = require('fs');
var js = fs.readFileSync('each.js');
var errors = jsfmt.validate(js);
for(var i = 0; i < errors.length; i++){
  console.error(error[i]);
}

jsfmt.validate(<javascript_string>)
jsfmt.validateJSON(<JSON_string>)

varjsfmt = require('jsfmt');
var fs = require('fs');
var js = fs.readFileSync('unformatted.js');
var config = jsfmt.getConfig();
js = jsfmt.format(js, config);

jsfmt.rewrite(<javasript_string>, <rewrite_rule>)

var jsfmt = require('jsfmt');
var fs = require('fs');
var js = fs.readFileSync('each.js');
js = jsfmt.rewrite(js, "_.each(a, b) -> a.forEach(b)");

jsfmt.search(<javascript_string>, <search_expression>)

jsfmt.format(<javascript_string>, <config_object>)
jsfmt.formatJSON(<JSON_string>, <config_object>)
var config = jsfmt.getConfig();
```

```
npm install -g jsfmt
jsfmt --help

jsfmt --rewrite "_.reduce(a, b, c) -> a.reduce(b, c)" reduce.js
jsfmt --search "_.reduce(a, b, c)" reduce.js
jsfmt --validate bad.js

pattern -> replacement
```

```
```


