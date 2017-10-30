isomorphic-fetch
================

Fork of [isomorphic-fetch]: https://github.com/matthew-andrews/isomorphic-fetch with added support for Electron. Currently, isomorphic-fetch builds Electron with node's fetch implementation as isomorphic-fetch does not provide a seperate build target for this deployment mode. As a result, fetch requests are not visible in Chromium's developer tools. This fork of isomorphic-fetch enables Chromium inspection by adding in the explicit Electron build target. See original isomorphic-fetch project for more details.

## Installation

### NPM

```sh
npm install --save isomorphic-fetch-extended es6-promise
```

## Usage

```js
require('es6-promise').polyfill();
require('isomorphic-fetch-extended');

fetch('//offline-news-api.herokuapp.com/stories')
	.then(function(response) {
		if (response.status >= 400) {
			throw new Error("Bad response from server");
		}
		return response.json();
	})
	.then(function(stories) {
		console.log(stories);
	});
```
