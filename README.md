# npmdoc-happypack

#### api documentation for  [happypack (v3.0.3)](https://github.com/amireh/happypack#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-happypack.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-happypack) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-happypack.svg)](https://travis-ci.org/npmdoc/node-npmdoc-happypack)

#### webpack speed booster, makes you happy!

[![NPM](https://nodei.co/npm/happypack.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/happypack)

- [https://npmdoc.github.io/node-npmdoc-happypack/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-happypack/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-happypack/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-happypack/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-happypack/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-happypack/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Ahmad Amireh"
    },
    "bugs": {
        "url": "https://github.com/amireh/happypack/issues"
    },
    "dependencies": {
        "async": "1.5.0",
        "json-stringify-safe": "5.0.1",
        "loader-utils": "0.2.16",
        "mkdirp": "0.5.1"
    },
    "description": "webpack speed booster, makes you happy!",
    "devDependencies": {
        "chai": "3.5.0",
        "codecov": "1.0.1",
        "eslint": "2.13.1",
        "fs-extra": "0.30.0",
        "mocha": "3.0.1",
        "multiline-slash": "2.0.0",
        "nyc": "7.1.0",
        "sinon": "1.17.5",
        "webpack": "1.13.1",
        "webpack-dev-server": "1.14.1"
    },
    "directories": {},
    "dist": {
        "shasum": "22f78c87a325cdb798c958cf4ec383fcd4d6fdc7",
        "tarball": "https://registry.npmjs.org/happypack/-/happypack-3.0.3.tgz"
    },
    "gitHead": "17410b95b8e21fcb51ea4de43d091e178ea843f5",
    "homepage": "https://github.com/amireh/happypack#readme",
    "keywords": [
        "webpack",
        "plugin",
        "fast",
        "speed",
        "performance",
        "compilation",
        "transformer",
        "loader",
        "happiness",
        "happy"
    ],
    "license": "MIT",
    "main": "./lib/HappyPlugin.js",
    "maintainers": [
        {
            "name": "amireh"
        }
    ],
    "name": "happypack",
    "nyc": {
        "include": [
            "lib/*.js"
        ],
        "exclude": [
            "lib/**/*.test.js",
            "lib/HappyTestUtils.js"
        ]
    },
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/amireh/happypack.git"
    },
    "scripts": {
        "coverage": "nyc report",
        "coverage:ci": "nyc report --reporter=text-lcov > tmp/coverage.lcov && codecov --disable search -f tmp/coverage.lcov",
        "coverage:html": "nyc report --reporter html",
        "lint": "eslint lib",
        "prepublish": "npm run lint && npm run test && npm run test-examples",
        "test": "mocha 'lib/**/*.test.js'",
        "test-examples": "./examples/build-all.sh",
        "test:coverage": "nyc npm test"
    },
    "version": "3.0.3"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
