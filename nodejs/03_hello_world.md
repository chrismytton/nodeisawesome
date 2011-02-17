!SLIDE

## Obligatory hello world example

!SLIDE smaller

    @@@ javascript

    var http = require('http');

    http.createServer(function (req, res) {

      res.writeHead(200, {'Content-Type': 'text/plain'});

      res.end('Hello World\n');

    }).listen(8124, "127.0.0.1");

!SLIDE smaller

    @@@ javascript
    // CommonJS modules
    var http = require('http');

    http.createServer(function (req, res) {

      res.writeHead(200, {'Content-Type': 'text/plain'});

      res.end('Hello World\n');

    }).listen(8124, "127.0.0.1");

!SLIDE smaller

    @@@ javascript
    // CommonJS modules
    var http = require('http');
    // The callback will be invoked for each request
    http.createServer(function (req, res) {

      res.writeHead(200, {'Content-Type': 'text/plain'});

      res.end('Hello World\n');

    }).listen(8124, "127.0.0.1");

!SLIDE smaller

    @@@ javascript
    // CommonJS modules
    var http = require('http');
    // The callback will be invoked for each request
    http.createServer(function (req, res) {
      // Write out the status, and the headers
      res.writeHead(200, {'Content-Type': 'text/plain'});

      res.end('Hello World\n');

    }).listen(8124, "127.0.0.1");

!SLIDE smaller

    @@@ javascript
    // CommonJS modules
    var http = require('http');
    // The callback will be invoked for each request
    http.createServer(function (req, res) {
      // Write out the status, and the headers
      res.writeHead(200, {'Content-Type': 'text/plain'});
      // Finish the response by writing a body
      res.end('Hello World\n');

    }).listen(8124, "127.0.0.1");

!SLIDE smaller

    @@@ javascript
    // CommonJS modules
    var http = require('http');
    // The callback will be invoked for each request
    http.createServer(function (req, res) {
      // Write out the status, and the headers
      res.writeHead(200, {'Content-Type': 'text/plain'});
      // Finish the response by writing a body
      res.end('Hello World\n');

    }).listen(8124, "127.0.0.1"); // Start listening on port 8124