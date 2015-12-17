# inoreader
A nodejs wrapper for unread counter checking in Inoreader


### Example

```js
var inoreader = require('./index');

inoreader
    .config({
        appId: 0000000000,
        appKey: 'aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa',
        appName: 'unread-counter',
        login: 'email@email.com',
        pass: 'mysecretpassword'
    })
    .then(inoreader.getTotalCount)
    .then(function (resp) {
        console.log('Unread: ' + resp);
    })
    .catch(function (err) { 
        console.error('' + err); 
    })

```