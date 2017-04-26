# npmdoc-wordpress-rest-api

#### basic api documentation for  [wordpress-rest-api (v0.8.0)](https://github.com/kadamwhite/wordpress-rest-api)  [![npm package](https://img.shields.io/npm/v/npmdoc-wordpress-rest-api.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-wordpress-rest-api) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-wordpress-rest-api.svg)](https://travis-ci.org/npmdoc/node-npmdoc-wordpress-rest-api)

#### A client for interacting with the WordPress REST API

[![NPM](https://nodei.co/npm/wordpress-rest-api.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/wordpress-rest-api)

- [https://npmdoc.github.io/node-npmdoc-wordpress-rest-api/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-wordpress-rest-api/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-wordpress-rest-api/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-wordpress-rest-api/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-wordpress-rest-api/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-wordpress-rest-api/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "K.Adam White",
        "url": "http://www.kadamwhite.com"
    },
    "bugs": {
        "url": "https://github.com/kadamwhite/wordpress-rest-api/issues"
    },
    "dependencies": {
        "bluebird": "^3.4.1",
        "li": "^1.0.1",
        "lodash": "^2.4.2",
        "node.extend": "^1.1.5",
        "parse-link-header": "^0.4.1",
        "qs": "^6.2.0",
        "route-parser": "0.0.4",
        "superagent": "^1.8.3"
    },
    "deprecated": "MODULE RENAMED: This module has been renamed to \"wpapi\"",
    "description": "A client for interacting with the WordPress REST API",
    "devDependencies": {
        "chai": "^3.5.0",
        "chai-as-promised": "^5.3.0",
        "grunt": "^1.0.1",
        "grunt-cli": "^1.2.0",
        "grunt-contrib-jshint": "^1.0.0",
        "grunt-contrib-yuidoc": "^1.0.0",
        "istanbul": "^0.4.4",
        "jscs": "^3.0.5",
        "jscs-stylish": "^0.3.1",
        "jshint": "^2.9.2",
        "jshint-stylish": "^2.2.0",
        "load-grunt-tasks": "^3.5.0",
        "minimist": "^1.2.0",
        "mocha": "^2.5.3",
        "sandboxed-module": "^2.0.3",
        "sinon": "^1.17.4",
        "sinon-chai": "^2.8.0"
    },
    "directories": {},
    "dist": {
        "shasum": "819a0d0999a1253df078b4fc662eb4a22452049f",
        "tarball": "https://registry.npmjs.org/wordpress-rest-api/-/wordpress-rest-api-0.8.0.tgz"
    },
    "engines": {
        "node": ">= 0.10.0"
    },
    "gitHead": "042fa899d0a1ba1d6260b48b2c62758c9d4b9294",
    "homepage": "https://github.com/kadamwhite/wordpress-rest-api",
    "keywords": [
        "api",
        "client",
        "cms",
        "wordpress"
    ],
    "license": "MIT",
    "main": "wp.js",
    "maintainers": [
        {
            "name": "kadamwhite"
        }
    ],
    "name": "wordpress-rest-api",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/kadamwhite/wordpress-rest-api.git"
    },
    "scripts": {
        "docs": "grunt yuidoc",
        "download-endpoint-json": "node ./lib/data/generate-endpoint-response-json",
        "jscs": "jscs Gruntfile.js wp.js lib tests --reporter node_modules/jscs-stylish/jscs-stylish.js",
        "jshint": "jshint --reporter=node_modules/jshint-stylish/index.js Gruntfile.js wp.js lib tests",
        "lint": "npm run jshint && npm run jscs || true",
        "mocha": "_mocha tests --recursive --reporter=nyan",
        "pretest": "npm run lint",
        "test": "istanbul cover _mocha -- tests --recursive --reporter=nyan",
        "test:all": "_mocha tests --recursive --reporter=nyan",
        "test:ci": "npm run lint && istanbul cover _mocha -- tests/unit --recursive --reporter=list",
        "test:integration": "_mocha tests/integration --recursive --reporter=nyan",
        "test:unit": "_mocha tests/unit --recursive --reporter=nyan",
        "watch": "grunt watch"
    },
    "version": "0.8.0",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
