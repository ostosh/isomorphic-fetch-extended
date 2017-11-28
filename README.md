isomorphic-fetch-extended
================

Fork of https://github.com/matthew-andrews/isomorphic-fetch with added support for Electron. Currently, isomorphic-fetch builds Electron with node's fetch implementation as isomorphic-fetch does not provide a separate build target for this deployment mode. As a result, fetch requests are not visible in Chromium's developer tools. This fork of isomorphic-fetch enables Chromium inspection by adding in the explicit Electron build target. See original isomorphic-fetch project for more details.

## Installation

### NPM

```sh
npm install --save isomorphic-fetch-extended es6-promise
```
