# Yarn v2

[Yarn v2](http://yarnpkg.com/) is a major break away from [classic yarn](https://classic.yarnpkg.com/). Along with a number of other changes, it now relies entirely on PnP (plug and play) compatibility, which not all libraries or SDKs support.

This project attempts to demonstrate how someone would go about adding support for many of those packages, including support for webpack v4, Typescript, and VS Code.

## Steps to add support:

```sh
yarn set version latest
yarn
```

Optional - enables updating dependencies

```sh
yarn plugin import interactive-tools
yarn upgrade-interactive
```

Add support for various things that don't support pnp natively

```sh
yarn add -D pnp-webpack-plugin # Not needed in webpack v5
yarn add -D @yarnpkg/pnpify
yarn pnpify --sdk vscode
```
