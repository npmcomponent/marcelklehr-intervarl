*This repository is a mirror of the [component](http://component.io) module [marcelklehr/intervarl](http://github.com/marcelklehr/intervarl). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/marcelklehr-intervarl`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*
﻿
# a variable interval
dynamically change your interval period

## Install
`npm install intervarl`
or
`component install marcelklehr/intervarl`

## Usage
```js
var setInterval = require('intervarl').setInterval

var interval = setInterval(function() {
  console.log('ShAZzAmM')
  if(interval.period < 20000) return interval.period = interval.period+1000
  interval.period = interval.period-1000
}, 0)

setTimeout(function() {
  interval.stop()
}, 60000)
```

# License
MIT