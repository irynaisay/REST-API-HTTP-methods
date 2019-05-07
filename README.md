## REST API

**CONTENT**

**1. REST API essentials and principles**

**2. Primary HTTP verbs: GET, PUT, POST, DELETE**

-----------------------------

**1. REST API essentials and principles**

First, let's see what the REST acronym means. It goes for *REpresentational State Transfer*, which means a software architectural style with characteristics that governs behavior of servers and clients.

An API is “RESTful”, if the following requirements are met (the list is inexhaustive):

- *Client–server.* A client and a server both maintain the frontend and the backend respectively; these two can be interchanged independently

- *Stateless* means no client data is stored on the server between the requests, while the session state is stored on the client

- *Cacheable.* Clients can easily cache responses (the same as browsers cache statics of a web page). This allows improving performance.

Because REST APIs use HTTP, they can be used by any programming language. In addition, they can be easily tested.

To show how it works, we'll make a real-life example. Let's take a look at Twitter: if you need to get the latest tweets, you can easily query it as shown below:

<http://search.twitter.com/search.json?q=jQuery&result_type=recent&rpp=3>

This example returns results in JSON format with the 3 latest tweets matching "jQuery" wording.


**2. Primary HTTP verbs: GET, PUT, POST, DELETE**

There are several major HTTP verbs (or the so called methods) used to read, update/replace, create, and delete operations, namely: GET, PUT, POST, and DELETE.

Let's see what they go for:

|Verb       | Utilization           | Description  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |
