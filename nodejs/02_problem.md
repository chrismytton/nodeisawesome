!SLIDE bullets incremental

# WTF is node.js? #

* "Evented I/O for V8 JavaScript"
* Concurrent, scalable network programs
* Speaks HTTP natively
* Asynchronous, non-blocking by design

!SLIDE center

# How is it better than *x*? #

![Error](500.jpeg)

!SLIDE incremental

    @@@ javascript
    var result = posts.findAll();



    doSomethingElse();

!SLIDE

    @@@ javascript
    var result = posts.findAll();

    // Waiting for results

    doSomethingElse();

!SLIDE center

# The node way! #

![Hovercar](hovercar.jpg)

!SLIDE

    @@@ javascript
    posts.findAll(function(result) {

    });



    doSomethingElse();

!SLIDE

    @@@ javascript
    posts.findAll(function(result) {
      // Do something with result
    });



    doSomethingElse();

!SLIDE

    @@@ javascript
    posts.findAll(function(result) {
      // Do something with result
    });

    // No waiting!

    doSomethingElse();
