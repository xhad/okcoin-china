# OKCoin China API Wrapper


A node.js wrapper for the [REST APIs](https://www.okcoin.cn/about/rest_api.do) exposed by bitcoin exchange [OKCoin](https://www.okcoin.cn).
You will need to have a registered account with [OKCoin](https://www.okcoin.cn) and generated API keys to access the private methods.

Please contact support@okcoin.com if you are having trouble opening an account or generating an API key.

This module is forked from [okcoin](https://www.npmjs.com/~naddison36).

forked from [naddison36](https://github.com/naddison36/okcoin)

A node.js wrapper for the [REST APIs](https://www.okcoin.cn/about/rest_api.do) exposed by bitcoin exchange [OKCoin](https://www.okcoin.cn).
You will need to have a registered account with [OKCoin](https://www.okcoin.cn) and generated API keys to access the private methods.

Please contact support@okcoin.com if you are having trouble opening and account or generating an API key.

### Install

`npm install okcoin-china`

```js
var OKCoin = require('okcoin-china');

// Test public data APIs
var publicClient = new OKCoin();

// get BTCCNY ticker
publicClient.getTicker(console.log, 'btc_cny');

// get BTCCNY order book
publicClient.getDepth(console.log, 'btc_cny');

// get trades defaulting to BTCCNY
publicClient.getTrades(console.log);

// replace the parameters with your API key and secret
var privateClient = new OKCoin('your-api-key', 'your-api-secret');

privateClient.getUserInfo(console.log);

// buy limit order for 0.01 BTC at price 4000 CNY
privateClient.addTrade(console.log, 'btc_cny', 'buy', '0.01', '4000');

```
