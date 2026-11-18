Shuup Static Build Tools
------------------------

This package uses [Parcel](https://parceljs.org/) to compile JavaScript and LESS entry points for [Shuup](https://github.com/shuup/shuup) add-ons.

## Installation

```shell
$ npm i --save shuup-static-build-tools
```

## Usage

Create a Node.js build script named `build_resources.js`.

```js
const { getParcelBuildCommand, runBuildCommands } = require("shuup-static-build-tools");

runBuildCommands([
    getParcelBuildCommand({
        cacheDir: "myapp",
        outputDir: "static/myapp/",
        entryFile: "static_src/myapp.js"
    }),
    getParcelBuildCommand({
        cacheDir: "myapp",
        outputDir: "static/myapp/",
        entryFile: "static_src/myapp.less"
    })
]);
```

Add these properties to your `package.json`.

```json
{
  "scripts": {
    "watch": "node build_resources.js --watch",
    "build": "node build_resources.js"
  },
  "shuup": {
    "static_build": true
  }
}
```

Run the package's build script with `npm run build`, or build resources for all Shuup apps from the Shuup repository root.

```
python setup.py build_resources
```

Install the [Parcel](https://parceljs.org/) transformers your entry points require.

## License

OSL-3.0
