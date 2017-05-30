# stylelint-config-zicht

> Shareable stylelint configuration for Zicht projects.

Use this configuration for [stylelint](https://stylelint.io/) when you're writing CSS for a project by Zicht.

To see the rules that this config uses, please read the [config itself](./index.js).

## Installing

```bash
npm install stylelint-config-zicht --save-dev
```

## Usage

After installing, add a `stylelint` property to your package.json. Stylelint will automatically find the config in your `node_modules` directory.

```
{
    "stylelint": {
        "extends": "stylelint-config-zicht"
    }
}
```

### Linting with an NPM script

Add a script to your package.json.

```
"scripts": {
    "lint-css": "./node_modules/.bin/stylelint 'sass/**/*.scss' --verbose"
}
```

Then run it:

```
npm run lint-css
```

### Linting in your Webpack build

First, install the [stylelint Webpack plugin](https://github.com/JaKXz/stylelint-webpack-plugin).

```
npm install stylelint-webpack-plugin --save-dev
```

Then, load the plugin in your build configuration.

```
const StyleLintPlugin = require('stylelint-webpack-plugin');
   
...
   
   plugins: [
        new StyleLintPlugin({
            files: 'sass/**/*.scss',
            quiet: false
        })
   ]

```

## [License](LICENSE)
