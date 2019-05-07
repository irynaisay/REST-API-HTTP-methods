## REST API

**CONTENT**

**1. REST API essentials and principles**

**2. Primary HTTP verbs: GET, PUT, POST, DELETE**


#1. REST API essentials and principles

First, let's see what the REST acronym means. It goes for *REpresentational State Transfer*, which means a software architectural style with characteristics that governs behavior of servers and clients.

An API is “RESTful”, if the following requirements are met (the list is inexhaustive):

*Client–server.* A client and a server both maintain the frontend and the backend respectively; these two can be interchanged independently

*Stateless* means no client data is stored on the server between the requests, while the session state is stored on the client

*Cacheable.* Clients can easily cache responses (the same as browsers cach statics of a web page). This allows improving performance.

Because REST APIs use HTTP, they can be used by any programing language. In addition, they can be easily tested.

To make a real-life example, let's take a look at Twitter: if you need to get the latest tweets, query it (see nelow):

```http://search.twitter.com/search.json?q=jQuery&result_type=recent&rpp=3```

#2. Primary HTTP verbs: GET, PUT, POST, DELETE

