# cache-api-experiment

Testing Cache API

[1. About](#1-about)  
[2. Dev + Build](#2-dev--build)  
&nbsp; &nbsp; [2-1. Dev](#2-1-dev)  
&nbsp; &nbsp; [2-2. Build](#2-2-build)  
[3. What I Did](#3-what-i-did)  
[4. Installed NPM Packages](#4-installed-npm-packages)  
&nbsp; &nbsp; [4-1. All](#4-1-all)  
&nbsp; &nbsp; [4-2. Babel](#4-2-babel)  
&nbsp; &nbsp; [4-3. ESLint + Prettier](#4-3-eslint--prettier)  
&nbsp; &nbsp; [4-4. TypeScript](#4-4-typescript)  
&nbsp; &nbsp; [4-5. Jest](#4-5-jest)  
&nbsp; &nbsp; [4-6. Vue](#4-6-vue)  
&nbsp; &nbsp; [4-7. Webpack](#4-7-webpack)  
&nbsp; &nbsp; [4-8. Other Build Tools](#4-8-other-build-tools)  
&nbsp; &nbsp; [4-9. Other Packages](#4-9-other-packages)  
[5. LICENSE](#5-license)

## 1. About

Testing Cache API.

- Vue 2 (Vue 3 is still not ready for some libraries)
- Babel 7 for TypeScript compilation
- Webpack 5
- Vuex
- Vue Router
- Jest (using `babel-jest` instead of `ts-jest`)

## 2. Dev + Build

### 2-1. Dev

```
yarn start
```

### 2-2. Build

```
yarn prod
```

## 3. What I Did

xxxx

## 4. Installed NPM Packages

### 4-1. All

```
yarn add vue vue-router vuex register-service-worker

yarn add --dev @babel/core babel-core@bridge @babel/cli @babel/preset-env core-js@3 @babel/runtime-corejs3 babel-loader eslint eslint-config-prettier eslint-plugin-vue typescript ts-loader @typescript-eslint/eslint-plugin @typescript-eslint/parser @vue/eslint-config-typescript jest babel-jest vue-jest @types/jest @vue/test-utils vue-loader vue-template-compiler vue-style-loader webpack webpack-cli webpack-dev-server file-loader css-loader style-loader postcss-loader autoprefixer webpack-merge clean-webpack-plugin html-webpack-plugin copy-webpack-plugin mini-css-extract-plugin license-webpack-plugin @types/webpack-env prettier
```

### 4-2. Babel

For `@babel/polyfill` has been deprecated, we use `core-js`.  
Notice we are using
[babel-preset-vue](https://github.com/vuejs/babel-preset-vue)

- @babel/core
- <strike>babel-core@^7.0.0-bridge.0</strike>
- babel-core@bridge
  - Allowing `vue-jest` to find Babel.
- @babel/cli
- @babel/preset-env
- core-js@3
- @babel/runtime-corejs3
- babel-loader
- <strike>babel-plugin-bundled-import-meta</strike>

yarn remove babel-plugin-bundled-import-meta

```
yarn add --dev @babel/core babel-core@bridge @babel/cli @babel/preset-env core-js@3 @babel/runtime-corejs3 babel-loader
```

### 4-3. ESLint + Prettier

Just like in React setup, we use
[eslint-config-prettier](https://github.com/prettier/eslint-config-prettier)
to filter out the ESLint rules which conflict with Prettier.  
While we use
[eslint-plugin-prettier](https://github.com/prettier/eslint-plugin-prettier)
for orchestration, for Vue, we will use
[eslint-plugin-vue](https://github.com/vuejs/eslint-plugin-vue).

- eslint
- eslint-config-prettier
- eslint-plugin-vue

```
yarn add --dev eslint eslint-config-prettier eslint-plugin-vue
```

Note:  
Vue CLI uses `eslint-plugin-prettier`.

TODO:  
Investigate `@vue/eslint-config-prettier`.

### 4-4. TypeScript

Several other packages such as `@types/jest`, `@types/webpack-env`, and so on, are needed.

- typescript
- ts-loader
- @typescript-eslint/eslint-plugin
- @typescript-eslint/parser
- @vue/eslint-config-typescript

```
yarn add --dev typescript ts-loader @typescript-eslint/eslint-plugin @typescript-eslint/parser @vue/eslint-config-typescript
```

### 4-5. Jest

Using
[babel-jest](https://github.com/babel/babel-jest)
instead of
[ts-jest](https://github.com/kulshekhar/ts-jest).

- jest
- babel-jest
- vue-jest
- @types/jest
- @vue/test-utils

```
yarn add --dev jest babel-jest vue-jest @types/jest @vue/test-utils
```

### 4-6. Vue

Since some modules are not ready for Vue 3, installing Vue 2.

- vue
- vue-router
- vuex
- vue-loader
- vue-template-compiler
- vue-style-loader

```
yarn add vue vue-router vuex

yarn add --dev vue-loader vue-template-compiler vue-style-loader
```

Note:  
When using Vue CLI, the following modules are installed:

```
@vue/cli-service
@vue/cli-plugin-babel
@vue/cli-plugin-eslint
@vue/cli-plugin-pwa
@vue/cli-plugin-router
@vue/cli-plugin-typescript
@vue/cli-plugin-unit-jest
@vue/cli-plugin-vuex
@vue/compiler-sfc
```

### 4-7. Webpack

- webpack
- webpack-cli
- webpack-dev-server
- file-loader
- css-loader
- style-loader
- postcss-loader
- autoprefixer
- webpack-merge
- clean-webpack-plugin
- html-webpack-plugin
- copy-webpack-plugin
- mini-css-extract-plugin
- license-webpack-plugin
- @types/webpack-env

```
yarn add --dev webpack webpack-cli webpack-dev-server file-loader css-loader style-loader postcss-loader autoprefixer webpack-merge clean-webpack-plugin html-webpack-plugin copy-webpack-plugin mini-css-extract-plugin license-webpack-plugin
```

### 4-8. Other Build Tools

- prettier

```
yarn add --dev prettier
```

### 4-9. Other Packages

- register-service-worker

```
yarn add register-service-worker
```

## 5. License

Dual-licensed under either of the followings.  
Choose at your option.

- The UNLICENSE ([LICENSE.UNLICENSE](LICENSE.UNLICENSE))
- MIT license ([LICENSE.MIT](LICENSE.MIT))
