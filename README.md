# testcafe-browser-provider-browserstack
[![Build Status](https://travis-ci.org/DevExpress/testcafe-browser-provider-browserstack.svg)](https://travis-ci.org/DevExpress/testcafe-browser-provider-browserstack)

This is the [TestCafe](http://devexpress.github.io/testcafe) browser provider plugin for the integration with the [BrowserStack Testing Cloud](https://browserstack.com/).

## Install

```
npm install testcafe-browser-provider-browserstack
```

## Usage
Before using the provider, save the BrowserStack username and access key to environment variables `BROWSERSTACK_USERNAME` and `BROWSERSTACK_ACCESS_KEY`.

You can determine the available browser aliases by running
```
testcafe -b browserstack
```

When you run tests from the command line, use the alias when specifying browsers:

```
testcafe "browserstack:Chrome@53.0:Windows 10" "path/to/test/file.js"
```


When you use API, pass the alias to the `browsers()` method:

```js
testCafe
    .createRunner()
    .src('path/to/test/file.js')
    .browsers('browserstack:Chrome@53.0:Windows 10')
    .run();
```

## Author
Developer Express Inc. (https://devexpress.com)
