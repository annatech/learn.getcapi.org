---
title: 'Event-Driven  Non-blocking I/O with PHP'
taxonomy:
    category:
        - docs
process:
    markdown: true
    twig: true
content:
    items:
        '@page': /libraries/services-libraries/react-php
    order:
        by: title
        dir: asc
    limit: 99
    pagination: false
---

[![React PHP](reactphp.png?cropResize=250)](http://reactphp.org)

#### [<span class="fa fa-github"> Github</span>](https://github.com/reactphp) [<span class="fa fa-twitter"> Twitter</span>](https://twitter.com/reactphp) [<span class="fa fa-slack"> IRC</span>](irc://irc.freenode.net/reactphp)


> ReactPHP is a low-level library for event-driven programming in PHP. At its core is an event loop, on top of which it provides low-level utilities, such as: Streams abstraction, async dns resolver, network client/server, http client/server, interaction with processes. Third-party libraries can use these components to create async network clients/servers and more.

React PHP libraries were introduced into cAPI release v1.3.2 to open the door for event-based application development.

* Keep an eye on these pages for additional information as we update our documentation to include new API methods to generate and interact with asynchronous event handlers, timers, promises and more!


### Additional Resources

#### React PHP Libraries Included with cAPI

[https://learn.getcapi.org/advanced/event-driven-application-development](/libraries/services-libraries/react-php)

{% for p in page.collection %}
##### [{{ p.title }}]({{p.link}})
{% endfor %}

#### By Developer Sergey Zhuk

[http://seregazhuk.github.io](http://seregazhuk.github.io)

- [Event-Driven PHP with ReactPHP: Event Loop And Timers](http://seregazhuk.github.io/2017/06/06/phpreact-event-loop/)
- [Event-Driven PHP with ReactPHP: Streams](http://seregazhuk.github.io/2017/06/12/phpreact-streams/)
- [Event-Driven PHP with ReactPHP: Promises](http://seregazhuk.github.io/2017/06/16/phpreact-promises/)
- [Build A Simple Chat With ReactPHP Socket: Server](http://seregazhuk.github.io/2017/06/22/reactphp-chat-server/)
- [Build A Simple Chat With ReactPHP Socket: Client](http://seregazhuk.github.io/2017/06/24/reactphp-chat-client/)
- [UDP/Datagram Sockets with ReactPHP](http://seregazhuk.github.io/2017/07/05/reactphp-udp/)
- [Building Video Streaming Server with ReactPHP](http://seregazhuk.github.io/2017/07/17/reatcphp-http-server/)
- [Making Asynchronous HTTP Requests With ReactPHP](http://seregazhuk.github.io/2017/07/26/reactphp-http-client/)
- [Managing Child Processes With ReactPHP](http://seregazhuk.github.io/2017/08/07/reactphp-child-process/)
