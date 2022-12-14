# Authing Tenants Demo

<div align=center>
  <img width="250" src="https://files.authing.co/authing-console/authing-logo-new-20210924.svg" />
</div>

<div align=center>
  <a href="https://forum.authing.cn/" target="_blank"><img src="https://img.shields.io/badge/chat-forum-blue" /></a>
  <a href="https://opensource.org/licenses/MIT" target="_blank"><img src="https://img.shields.io/badge/License-MIT-success" alt="License"></a>
</div>

**English** | [简体中文](./README.zh-CN.md)

## Introduction

This demo will show you how to use Authing to develop a SaaS software called Uthing. Let us take the example software Uthing as an example, Uthing is an advanced enterprise collaboration tool that provides efficient workflow management functions, and it is also a SaaS software on which different companies can manage their own workflows.


## Change Setting

Modify the `/server/config.js` file and modify the following configuration:

```js
module.exports = {
  authing: {
    userPoolId: '<your user pool id>',
    userPoolSecret: '<your user pool secret>',
    appId: '<your app id>',
    appSecret: '<your app secret>',
    host: '<your app host>', // Authing api url, usually https://core.authing.cn
  },
}
```

Modify the `client/src/config.ts` file and modify the following configuration:

```js
export const config = {
  apiBaseUrl: 'http://localhost:3006',
  pageBaseHost: 'localhost:3007',
  authing: {
    appId: '<your app id>',
    appHost: '<your app host>',
  },
}
```

## Start the backend service

Open a terminal and execute

```sh
cd server
yarn install
yarn start
```

## Start the front-end service

Open another terminal and execute

```sh
cd client
yarn install
yarn start
```

## start complete

Visit `http://localhost:3007/login`


## License

[MIT](https://opensource.org/licenses/MIT)

Copyright (c) 2019-present, Authing
