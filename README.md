# node-regex-files

```js
var regexfiles = require('./regexfiles.js')

var rIncludes = [/\.html$/i];
var rExcludes = [/\/node_modules\//, /\/\.git\//, /\/\.tmp\//];

var st = new Date();
regexfiles('./', rIncludes, rExcludes, function (err, subfiles) {
  if (err) {
    console.log(chalk.red(err.message));
    return;
  }
  console.log(subfiles);
  var end = st.getTime() - (new Date()).getTime()
  console.log(end)
});

var st2 = new Date();
regexfiles('./', _regIncludes, [], function (err, subfiles) {
  if (err) {
    console.log(chalk.red(err.message));
    return;
  }
  console.log(subfiles);
  var end = st2.getTime() - (new Date()).getTime()
  console.log(end)
});
```