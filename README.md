# AjaxPromise

## Description

A very narrowly scoped Ajax library that returns promises instead of using
callbacks.

Return values should be JSON objects with status 200.

If status not 200, then the promise will return an error.
The error should be returned as a JSON object as well.


## Usage

```javascript
var AjaxPromise = require('ajax-promise');

AjaxPromise
  .get('/pages')
  .then(function (response) {
    console.log(response);
  })

AjaxPromise
  .post('/pages', {title: 'Hello', body: 'Hello to the world!'})
  .then(function (response) {
    console.log(response);
  })
  .catch(function (err) {
    console.log('errors in response', err);
  })
```