LocalBitcoins Node API
===========

NodeJS Client Library for the LocalBitcoins API

This is an asynchronous node js client for the localbitcoins.com API.

It exposes all the API methods found here: https://localbitcoins.com/api-docs/ through the 'api' method:

Example Usage:

`npm install localbitcoins-client`

```javascript
var methods = {
    public: [],
    private: [],
    get: [
        'contact_info/', 'recent_messages'
    ],
    post: []
}
var LBCClient = require('localbitcoins-client');
var lbc = new LBCClient(api_key, api_secret, {methods: methods});

var ad_id; //set to value when applicable
var params = {};


// Display user's info
lbc.api('myself', ad_id, params, function(error, data) {
    if(error) {
        console.log(error);
    }
    else {
        console.log(data);
    }
});

```
