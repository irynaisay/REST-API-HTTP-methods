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

----------------------------------

**2. Primary HTTP verbs: GET, PUT, POST, DELETE**

There are several major HTTP verbs (or the so called methods) used to read, update/replace, create, and delete operations, namely: GET, PUT, POST, and DELETE.

Let's see what they go for with [Google Cloud examples](https://cloud.google.com/apis/design/standard_methods):

|Verb       | Utilization           | HTTP Mapping  |
| ------------- |:-------------:| -----:|
| GET      | retrieves information from the server | GET < resource URL > |
| PUT      | replaces representations with new content     |   PUT < resource URL > |
| POST | sends data to the server     | POST < collection URL > |
| DELETE | removes representations      | DELETE < resource URL > |

Based on the [Google Classroom API example](https://developers.google.com/classroom/reference/rest/v1/courses.students/list), let's see how to extract list of students: HTTP request: GET <https://classroom.googleapis.com/v1/courses/{courseId}/students>

JSON representation would be as follows:
```
{
  "students": [
    {
      object(Student)
    }
  ],
  "nextPageToken": string
}
```
where "students" object(Student) means students who match the list request.

We can expand the request and JSON representation would be as follows:

```
{
  "courseId": string,
  "userId": string,
  "profile": {
    object(UserProfile)
  },
  "studentWorkFolder": {
    object(DriveFolder)
  }
}
```
where 
- courseId string means identifier of the course
- userId string means identifier of the user
- profile object(UserProfile) means global user information for the student
- studentWorkFolder	object(DriveFolder) means information about a Drive Folder for this student's work in this course

You can epand the methods with more HTTP verbs.
