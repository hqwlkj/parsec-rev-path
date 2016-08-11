# parsec-rev-path [![Build Status](https://travis-ci.org/hqwlkj/parsec-rev-path.svg?branch=master)](https://travis-ci.org/hqwlkj/parsec-rev-path)

> Create a [revved file path](http://blog.risingstack.com/automatic-cache-busting-for-your-css/)


## Install

```
$ npm install --save parsec-rev-path
```


## Usage

```js
var revPath = require('parsec-rev-path');
var hash = 'bb9d8fe615'

var path = revPath('src/unicorn.png', hash);
//=> 'src/unicorn.png?v=bb9d8fe615'

revPath('src/unicorn.png', Date.now());
//=> 'src/unicorn.png?v=1432309925925'

// you can also revert an already hashed path
revPath.revert(path, hash);
//=> 'src/unicorn.png'
```



## License

MIT © [Yanghc](https://github.com/hqwlkj)
