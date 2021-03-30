global-npm
======
Require global npm as a local node module.

[![NPM version](https://badge.fury.io/js/global-npm.svg)](https://www.npmjs.com/package/global-npm)
[![Deps](https://david-dm.org/dracupid/global-npm.svg?style=flat)](https://david-dm.org/dracupid/global-npm)
[![Build Status](https://travis-ci.org/dracupid/global-npm.svg)](https://travis-ci.org/dracupid/global-npm)
[![Build status](https://ci.appveyor.com/api/projects/status/github/dracupid/global-npm?svg=true)](https://ci.appveyor.com/project/dracupid/global-npm)

[![js-standard-style](https://cdn.rawgit.com/feross/standard/master/badge.svg)](https://github.com/feross/standard)

Npm is about 25MB in size now, which is quite a heavy dependency for most modules. Luckily, nearly every node.js user has a npm installed globally.

However, normally, you can't require a global module directly, unless:

0. [set `NODE_PATH` environment variable](https://nodejs.org/api/modules.html#modules_loading_from_the_global_folders) to the folder where global modules are installed.
0. [link](https://docs.npmjs.com/cli/link) the local project with global module to use.
0. [require a file path](https://nodejs.org/api/modules.html#modules_file_modules) instead of a module name.

The last one should be the best way for a third-party module.

If your module needs to depend on `npm`, why not just use the global one?

## Usage
```javascript
var npm = require('global-npm')
```

**If the version of npm counts, please use [semver](https://github.com/npm/node-semver) to check `npm.version` by yourself.**

## License
MIT@Dracupid
