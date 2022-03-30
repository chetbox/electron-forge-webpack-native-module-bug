## Electron Forge Typescript + Webpack native modules bug

This repo contains was creating using the Electron Forge Typescript + Webpack template:

```
yarn create electron-app my-new-app --template=typescript-webpack
```

and also includes the `lzma-native` library which should be available with `nodeIntegration: true`

### Reproduce the error

- Clone this repo
- `yarn`
- `yarn package`
- `./out/my-new-app-*/my-new-app`

#### Expected behavior

A log message appears in the Electron window with an object containing the `lzma-native` imported library

#### Actual behavior

Console error message:

```
Uncaught Error: Cannot find module '/native_modules/prebuilds/linux-x64/node.napi.node'
```

### Other info:

Note that running with `yarn start` shows the log message as expected.
