# Yarn v2

[Yarn v2](http://yarnpkg.com/) is a major break away from [classic yarn](https://classic.yarnpkg.com/). Along with a number of other changes, it now relies entirely on PnP (plug and play) compatibility, which not all libraries or SDKs support.

This project attempts to demonstrate how someone would go about adding support for many of those packages, including support for webpack v4, Typescript, and VS Code.

## Steps to add support:

```sh
yarn set version latest
yarn
yarn plugin import interactive-tools # Adds a plugin to the repository to allow interactive package updates
yarn upgrade-interactive # Optional - updates all dependencies
yarn add -D pnp-webpack-plugin # Adds support for webpack 4 (also needs to be added to webpack.config.js)
yarn add -D @yarnpkg/pnpify # Adds support for packages that don't use require()
yarn add pnpify --sdk vscode # Adds support for VSCode's various language servers to use pnp compatible variants
```
