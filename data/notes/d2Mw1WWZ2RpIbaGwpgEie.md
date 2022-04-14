
Super test is used in conjunction with JEST or on it's own to test http requests.

- once installed, it can be used and referenced by calling `require('supertest')`

### Installation

`npm install supertest`

### Setup

- create normal expres app
- be sure to create `__tests__` folder, this seems to be what JEST needs to run testing. (You can run supertest without jest but issues are reported in normal error messages as opposed to jest style message).
- create a file with the convention `(FILENAME).test.js`
- if testing expres, export the app component
  `export const app = express();`
- import app object into test.js file `const { app } = require('../../dist/src/index.js');`
- sample app using supertest with no test suites

```const request = require('supertest');
const assert = require('assert');
const express = require('express');

const app = express();

app.get('/user', function(req, res) {
  res.status(200).json({ name: 'john' });
});

request(app)
  .get('/user')
  .expect('Content-Type', /json/)
  .expect('Content-Length', '15')
  .expect(200)
  .end(function(err, res) {
    if (err) throw err;
  });
```

### API Guide

API
You may use any superagent methods, including .write(), .pipe() etc and perform assertions in the .end() callback for lower-level needs.

- **.expect(status[, fn])**
  Assert response status code.

- **.expect(status, body[, fn])**
  Assert response status code and body.

- **.expect(body[, fn])**
  Assert response body text with a string, regular expression, or parsed body object.

- **.expect(field, value[, fn])**
  Assert header field value with a string or regular expression.

- **.expect(function(res) {})**
  Pass a custom assertion function. It'll be given the response object to check. If the check fails, throw an error.

```
request(app)
  .get('/')
  .expect(hasPreviousAndNextKeys)
  .end(done);

function hasPreviousAndNextKeys(res) {
  if (!('next' in res.body)) throw new Error("missing next key");
  if (!('prev' in res.body)) throw new Error("missing prev key");
}
```

- **.end(fn)**
  Perform the request and invoke fn(err, res).

[[Back|Testing]]
