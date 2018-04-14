# create-ava [![Build Status: Linux](https://travis-ci.org/avajs/ava-init.svg?branch=master)](https://travis-ci.org/avajs/ava-init) [![Build status: Windows](https://ci.appveyor.com/api/projects/status/abj17qsw0j1rts7l/branch/master?svg=true)](https://ci.appveyor.com/project/ava/ava-init/branch/master)

> Add [AVA](https://ava.li) to your project


## CLI

```
$ npx create-ava [<options>]
```


## Install

```
$ npm install create-ava
```


## Usage

```js
const createAva = require('create-ava');

createAva().then(() => {
	console.log('done');
});
```


## API

### createAva([options])

Returns a `Promise`.

#### options

#### cwd

Type: `string`<br>
Default: `process.cwd()`

Current working directory.

#### args

Type: `Array`<br>
Default: CLI arguments *(`process.argv.slice(2)`)*

For instance, with the arguments `['--foo', '--bar']`, the following will be put in package.json:

```json
{
	"name": "awesome-package",
	"scripts": {
		"test": "ava --foo --bar"
	}
}
```

#### next

Type: `boolean`<br>
Default: `false`

Install `ava@next` instead of `ava`.


## License

MIT © [Sindre Sorhus](https://sindresorhus.com)
