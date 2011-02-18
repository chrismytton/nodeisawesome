!SLIDE bullets incremental

# Use cases

* Realtime applications
* Web crawlers/scrapers
* Proxy servers
* Bridging the client/server gap

!SLIDE center

# Code please!

![Enigma](code.jpg)

!SLIDE smaller

## webhooks.js

    @@@javascript
    // Require module from node-core
    var http = require("http");

    // Attach function to the exports object
    exports.deliver = function(options, payload, callback) {

      // Create a new http request
      var req = http.request(options, function(res) {
        var body = '';
        res.setEncoding('utf8');

        // Capture the response body
        res.on('data', function (chunk) {
          body += chunk;
        });

        res.on('end', function() {
          // Return the result to the caller
          callback(body);
        });
      });

      // Send the payload to the endpoint
      req.write(payload);
      req.end();
    };

!SLIDE smaller

## application.js

    @@@javascript
    // Use a relative require to load the module
    var webhooks = require("./webhooks");

    // Create a payload and options
    var payload = {
      name: "hecticjeff",
      webscale: true
    },
    options = {
      host: "hecticjeff.net",
      port: 80,
      path: "/notify",
      method: 'POST'
    };

    // Use the deliver method that we exported
    webhooks.deliver(options, payload, function(response) {
      console.log("Webhook responded with %s", response);
    });

!SLIDE bullets incremental

# It sounds perfect!

## but beware...

* Quite a low level API
* Still evolving, changes quite frequently
* Not good for CPU intensive tasks
