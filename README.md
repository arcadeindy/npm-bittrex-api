This is an asynchronous node js client for the bittrex.com API.

It exposes all the API methods found here: https://www.bittrex.com/Home/Api.
 
```
npm install bittrex-api
```

-or-

```
git clone https://github.com/mwhite73/npm-bittrex-api.git
```


Example Usage:

```javascript
var market = 'BTC-LTC';
var bittrex = require('bittrex-api');
var client = new bittrex('my_public_key', 'my_private_key');

NodeBittrexApi.getbalances(function (err, response, taskcallback) {
    if (err) {
        console.log(JSON.stringify(err));
    } else {
        taskcallback(err, response);
    }
    function taskcallback(error, response) {
       if (error) {
          console.log(JSON.stringify(error) + ' ' + JSON.stringify(response));
       } else {
          console.log(JSON.stringify(response));
       }
    }
});



Note:

As of version 0.2.0, the callback function should conform to node's standard for callbacks:

```javascript
function callback(error, result) {
	// Do stuff...
}
```

Credit:

This package is modeled after the API from nothingisdead/npm-cryptsy-api, converted for use with Bittrex found here: https://github.com/nothingisdead/npm-cryptsy-api.git

This package was first modeled after the mtgox-apiv2 npm package located here: https://github.com/ameen3/node-mtgox-apiv2.

The methods were modeled after the python client located here: https://github.com/ScriptProdigy/CryptsyPythonAPI.



Feeling generous? Send me a fraction of a bitcoin!

1GZ55vWmv1CBe8VB5fRrDcNA5PXyus7g1n
