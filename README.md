# npmtest-cuid

#### test coverage for  [cuid (v1.3.8)](https://github.com/ericelliott/cuid#readme)  [![npm package](https://img.shields.io/npm/v/npmtest-cuid.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-cuid) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-cuid.svg)](https://travis-ci.org/npmtest/node-npmtest-cuid)

#### Collision-resistant ids optimized for horizontal scaling and performance. For node and browsers.

[![NPM](https://nodei.co/npm/cuid.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/cuid)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-cuid/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-cuid/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-cuid/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-cuid/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-cuid/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-cuid/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-cuid/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-cuid/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-cuid/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-cuid/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-cuid/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-cuid/build/test-report.html](https://npmtest.github.io/node-npmtest-cuid/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-cuid/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-cuid/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-cuid/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-cuid/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-cuid/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-cuid/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-cuid/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-cuid/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Eric Elliott",
        "url": "https://ericelliottjs.com"
    },
    "browser": "./dist/browser-cuid.js",
    "bugs": {
        "url": "https://github.com/ericelliott/cuid/issues"
    },
    "dependencies": {
        "browser-fingerprint": "0.0.1",
        "core-js": "^1.1.1",
        "node-fingerprint": "0.0.2"
    },
    "description": "Collision-resistant ids optimized for horizontal scaling and performance. For node and browsers.",
    "devDependencies": {
        "babel": "5.6.14",
        "babel-eslint": "^4.0.10",
        "babel-loader": "5.3.0",
        "babelify": "^6.2.0",
        "ecstatic": "^0.8.0",
        "eslint": "0.24.0",
        "faucet": "0.0.1",
        "node-libs-browser": "0.5.2",
        "rimraf": "2.4.1",
        "sauce-connect-launcher": "^0.12.0",
        "saucelabs": "0.1.1",
        "tape": "4.2.0",
        "wd": "^0.3.12",
        "webpack": "1.10.1",
        "zuul": "^3.3.0"
    },
    "directories": {},
    "dist": {
        "shasum": "4b875e0969bad764f7ec0706cf44f5fb0831f6b7",
        "tarball": "https://registry.npmjs.org/cuid/-/cuid-1.3.8.tgz"
    },
    "gitHead": "9fcb9e85316d0eec9a4a596a82432149f1950f81",
    "homepage": "https://github.com/ericelliott/cuid#readme",
    "keywords": [
        "id",
        "guid",
        "uid",
        "unique id",
        "uuid"
    ],
    "license": "MIT",
    "main": "./dist/node-cuid.js",
    "maintainers": [
        {
            "name": "ericelliott"
        }
    ],
    "name": "cuid",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/ericelliott/cuid.git"
    },
    "scripts": {
        "build": "npm run build:server && npm run build:client && npm run build:test",
        "build:client": "NODE_ENV=production WEBPACK_TARGET=client webpack -p",
        "build:server": "NODE_ENV=production WEBPACK_TARGET=server webpack",
        "build:test": "browserify ./test/client/index.js -s testcuid -t babelify --outfile test/client/test-cuid.js",
        "clean": "rimraf build && rimraf test/client/test-cuid.js",
        "comment:build:test": "NODE_ENV=production WEBPACK_TARGET=test webpack -p",
        "lint": "eslint source test",
        "prebuild": "npm run clean",
        "prepublish": "npm run validate",
        "prevalidate": "npm run clean",
        "test": "npm run test:server && npm run test:client",
        "test:client": "#zuul -- test/client/test-cuid",
        "test:server": "babel-node test/server",
        "validate": "npm run lint && npm run build && npm run test",
        "validate-dev": "npm run lint && npm run build && npm run test | faucet"
    },
    "version": "1.3.8"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
