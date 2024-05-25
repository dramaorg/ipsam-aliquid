# @dramaorg/ipsam-aliquid <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Validate an object in the "exports" field.

## Example

```js
const assert = require('assert');
const validateExportsObject = require('@dramaorg/ipsam-aliquid');
const pkg = require('./package.json');

const results = validateExportsObject(pkg.exports);

assert.deepEqual(
    results,
    {
        __proto__: null,
        normalized: {
            __proto__: null,
            '.': './index.js',
            './package.json': './package.json'
        },
        problems: [],
        status: 'files'
    }
);
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

## Security

Please email [@ljharb](https://github.com/ljharb) or see https://tidelift.com/security if you have a potential security vulnerability to report.

[package-url]: https://npmjs.org/package/@dramaorg/ipsam-aliquid
[npm-version-svg]: https://versionbadg.es/ljharb/@dramaorg/ipsam-aliquid.svg
[deps-svg]: https://david-dm.org/ljharb/@dramaorg/ipsam-aliquid.svg
[deps-url]: https://david-dm.org/ljharb/@dramaorg/ipsam-aliquid
[dev-deps-svg]: https://david-dm.org/ljharb/@dramaorg/ipsam-aliquid/dev-status.svg
[dev-deps-url]: https://david-dm.org/ljharb/@dramaorg/ipsam-aliquid#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@dramaorg/ipsam-aliquid.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@dramaorg/ipsam-aliquid.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@dramaorg/ipsam-aliquid.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@dramaorg/ipsam-aliquid
[codecov-image]: https://codecov.io/gh/ljharb/@dramaorg/ipsam-aliquid/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/ljharb/@dramaorg/ipsam-aliquid/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/ljharb/@dramaorg/ipsam-aliquid
[actions-url]: https://github.com/dramaorg/ipsam-aliquid/actions
