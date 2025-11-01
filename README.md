# zrgs

Tiny cli args module.

--------

## Installation

`npm i zrgs`

## Usage

`zrgs` does the bare minimum. It's just a couple of helper functions. If you
want an interactive CLI library, automatic help/usage, configurable aliases,
complex arguments, or any other nice features, you should probably use a
different library.

`zrgs` assumes you want short, long, and GNU-style long flags. `hasFlag('foo')`
will return true if the first argument is `-f`, `-foo`, or `--foo`. `args` is
`process.argv.slice(2)`. And that's it.

```javascript
const { hasFlag, args } = require('zrgs')

if (hasFlag('help')) {
  // display help
} else if (hasFlag('something')) {
  handleSomething(args)
}
```

[LICENSE](./LICENSE.md)
