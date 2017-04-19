# npmdoc-node-uglifier

#### api documentation for  [node-uglifier (v0.5.41)](https://github.com/zsoltszabo/node-uglifier)  [![npm package](https://img.shields.io/npm/v/npmdoc-node-uglifier.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-node-uglifier) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-node-uglifier.svg)](https://travis-ci.org/npmdoc/node-npmdoc-node-uglifier)

#### Fully auto merging and uglifying a whole NodeJs project into one file with external files option. Thieves lose the module name and structure information, code runs faster. Makes deployement super easy!
Also now you can separate your dependencies!

[![NPM](https://nodei.co/npm/node-uglifier.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/node-uglifier)

- [https://npmdoc.github.io/node-npmdoc-node-uglifier/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-node-uglifier/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-node-uglifier/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-node-uglifier/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-node-uglifier/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-node-uglifier/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Zsolt Istvan Szabo"
    },
    "bugs": {
        "url": "https://github.com/zsoltszabo/node-uglifier/issues"
    },
    "contributors": [],
    "dependencies": {
        "fs-extra": "=2.0",
        "optparse": ">=0.x",
        "seedrandom": ">=0.x",
        "sugar": "=2.0.4",
        "uglify-js-harmony": "=2.6.2",
        "underscore": ">=1.5.2"
    },
    "description": "Fully auto merging and uglifying a whole NodeJs project into one file with external files option. Thieves lose the module name and structure information, code runs faster. Makes deployement super easy!\nAlso now you can separate your dependencies!",
    "devDependencies": {
        "express": "4.14.0",
        "nodeunit": "=0.10.2"
    },
    "directories": {},
    "dist": {
        "shasum": "2bdd0699eddcc417689f042439ce6dd614317b8f",
        "tarball": "https://registry.npmjs.org/node-uglifier/-/node-uglifier-0.5.41.tgz"
    },
    "engines": {
        "node": "> 0.6.0"
    },
    "gitHead": "f60dabe36ca86257b9b13ac5cf3d281d57cdce2f",
    "homepage": "https://github.com/zsoltszabo/node-uglifier",
    "keywords": [
        "obfuscate",
        "total",
        "whole",
        "project",
        "protect",
        "minify",
        "code protect",
        "uglify",
        "mangle",
        "compress",
        "automatic",
        "code separation",
        "separate dependencies",
        "sub project extraction"
    ],
    "main": "./index.js",
    "maintainers": [
        {
            "name": "arbitrager"
        }
    ],
    "name": "node-uglifier",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/zsoltszabo/node-uglifier.git"
    },
    "scripts": {
        "test": "node nodeunit.js ./lib_compiled/test/unitTest.js"
    },
    "url": "https://github.com/zsoltszabo/node-uglifier",
    "version": "0.5.41"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
