# npmtest-sitespeed.io

#### basic test coverage for  [sitespeed.io (v4.7.0)](https://www.sitespeed.io)  [![npm package](https://img.shields.io/npm/v/npmtest-sitespeed.io.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-sitespeed.io) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-sitespeed.io.svg)](https://travis-ci.org/npmtest/node-npmtest-sitespeed.io)

#### Analyze the web performance of your site

[![NPM](https://nodei.co/npm/sitespeed.io.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/sitespeed.io)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-sitespeed.io/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-sitespeed.io/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-sitespeed.io/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-sitespeed.io/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-sitespeed.io/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-sitespeed.io/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-sitespeed.io/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-sitespeed.io/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-sitespeed.io/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-sitespeed.io/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-sitespeed.io/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-sitespeed.io/build/test-report.html](https://npmtest.github.io/node-npmtest-sitespeed.io/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-sitespeed.io/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-sitespeed.io/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-sitespeed.io/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-sitespeed.io/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-sitespeed.io/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-sitespeed.io/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-sitespeed.io/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-sitespeed.io/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "sitespeed.io",
    "bin": "./bin/sitespeed.js",
    "version": "4.7.0",
    "description": "Analyze the web performance of your site",
    "keywords": [
        "performance",
        "web",
        "rules",
        "har",
        "webperf",
        "perfmatters",
        "navigation-timing",
        "browser"
    ],
    "homepage": "https://www.sitespeed.io",
    "license": "MIT",
    "author": {
        "name": "Peter Hedenskog",
        "url": "https://www.peterhedenskog.com"
    },
    "contributors": [
        {
            "name": "Tobias Lidskog"
        },
        {
            "name": "Jonathan Lee"
        }
    ],
    "repository": {
        "type": "git",
        "url": "git://github.com/sitespeedio/sitespeed.io.git"
    },
    "bugs": {
        "url": "https://github.com/sitespeedio/sitespeed.io/issues"
    },
    "scripts": {
        "lint": "npm run eslint && npm run pug-lint",
        "eslint": "eslint .",
        "eclint": "eclint check * lib/**/* bin/**/* tools/**/* !*.iml",
        "eclint:fix": "eclint fix * lib/**/* bin/**/* tools/**/* !*.iml",
        "pug-lint": "pug-lint lib/plugins/html/templates",
        "test": "mocha",
        "check-licenses": "tools/check-licenses.js",
        "travis": "npm run lint && npm run test",
        "build:css": "node-sass lib/plugins/html/src/sass/main.scss > lib/plugins/html/assets/css/index.css && cleancss -o lib/plugins/html/assets/css/index.min.css lib/plugins/html/assets/css/index.css"
    },
    "engines": {
        "node": ">=6.9.1"
    },
    "devDependencies": {
        "chai": "^3.5.0",
        "chai-as-promised": "^6.0.0",
        "clean-css-cli": "^4.0.7",
        "eclint": "^1.1.5",
        "eslint": "^3.10.2",
        "jsdoc": "^3.3.3",
        "license-checker": "^5.1.2",
        "mocha": "^3.1.2",
        "node-sass": "^3.8.0",
        "pug-lint": "^2.3.0",
        "pug-lint-config-clock": "^2.0.0"
    },
    "main": "./lib/sitespeed.js",
    "dependencies": {
        "bluebird": "3.5.0",
        "browsertime": "1.0.0-beta.31",
        "cli-color": "1.1.0",
        "concurrent-queue": "7.0.1",
        "fast-stats": "0.0.3",
        "fs-extra": "2.0.0",
        "gpagespeed": "3.0.0",
        "influx": "5.0.4",
        "intel": "1.1.2",
        "junit-report-builder": "1.1.1",
        "lodash.chunk": "4.2.0",
        "lodash.clonedeep": "4.5.0",
        "lodash.difference": "4.5.0",
        "lodash.flatten": "4.4.0",
        "lodash.foreach": "4.5.0",
        "lodash.get": "4.4.2",
        "lodash.isempty": "4.4.0",
        "lodash.merge": "4.6.0",
        "lodash.pullall": "4.2.0",
        "lodash.reduce": "4.6.0",
        "lodash.set": "4.3.2",
        "lodash.union": "4.6.0",
        "longjohn": "0.2.12",
        "mkdirp": "0.5.1",
        "moment": "2.17.1",
        "node-slack": "0.0.7",
        "pagexray": "0.14.1",
        "pug": "2.0.0-beta11",
        "s3": "4.4.0",
        "simplecrawler": "1.1.0",
        "tape": "4.6.3",
        "text-table": "0.2.0",
        "uuid": "^3.0.0",
        "webcoach": "0.31.0",
        "webpagetest": "0.3.4",
        "yargs": "6.6.0"
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
