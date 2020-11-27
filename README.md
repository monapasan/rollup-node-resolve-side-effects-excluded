# Based on rollup-starter-app

This repo reproduces the problem where a file defined in `sideEffects` of `package.json` gets excluded from the bundle when using `@rollup/plugin-node-resolve`.
The file `polyfill/sideEffect.js` will be present in the bundle in case:

1. `sideEffects` is removed from package.json or set to `true`
2. Omit the use of plugin `@rollup/plugin-node-resolve` from the rollup build

