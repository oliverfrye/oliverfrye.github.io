---
layout: post
title: "Day Two: RESTful"
---

Welcome to another daily check-in. I've been working on a few things.

Firstly, learning about the REST architecture. It seems to be a commonly abused term for API's that use HTTP methods (GET, POST, PUT, DELETE, etc.) when in reality it was originally intended that REST could be used even if the client (browser) had no idea what the API looked like or how to use it. A concept called HATEOAS (Hypermedia as the Engine of Application State) is essential to this - it specifies that every response to a request must include 'hypermedia' links to related requests. It looks something like this:

~~~
GET /account/12345 HTTP/1.1
Host: yourbank.com
Accept: applcation/json
~~~

~~~
HTTP/1.1 200 OK
Content-Type application/json

{
    "accountNumber": "12345",
    "balance": "100.00,
    "links": [ {
        "rel": "deposit",
        "href": "https://yourbank.com/account/12345/deposit"
    },
    {
        "rel": "withdraw",
        "href": "https://yourbank.com/account/12345/withdraw"
    } ]
}
~~~

HATEOAS was an essential part of RESTful architecture as defined by [Roy Fielding](https://en.wikipedia.org/wiki/Roy_Fielding), whose doctoral dissertation formalized the concepts behind REST (among many other extremely important contributions to the web).

Practically, this system has never been used. The reasons are fairly obvious - [Jeff Knup explains](https://jeffknupp.com/blog/2014/06/03/why-i-hate-hateoas/) in his aptly named blog post "Why I Hate HATEOAS" that:

> When designing a hypermedia API, you're really designing for a client that does not, and will never, exist.

The rest of REST is pretty universal - statelessness fits in with established web conventions and is important for scalability. Every request from the client includes the important bits of the client's application state, hence the name Representational **State Transfer**.

The (semi-)RESTful API is going to be the first step in getting my Lyon project off the ground. Lyon will be a line-of-business web app for our family business, [Mary Street Wellness](http://marystreetwellness.com.au). It will handle appointments, patient data, billing and much more. It's going to replace a centuries old VB6 (!) application ironically named Capable.

At the moment I'm working on developing a model of the system in an awesome program called [StarUML](http://staruml.io/) - here's a sneak preview:

![Lyon UML diagram]({{ site.url }}/assets/img/2016-12-14-day-two-restful-1.png)

For the API I will be using [Django](https://www.djangoproject.com/) and [django-rest-framework](http://www.django-rest-framework.org/).

Anyway - I'd best get on with it and stop writing this.
