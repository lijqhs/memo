# REST API

REST (Representational State Transfer) is an architectural style for building web services that has become widely adopted in recent years. A RESTful API is a web service that adheres to the principles of the REST architecture and provides a standard way for clients to interact with server-side resources.

At its core, a RESTful API is a collection of resources that are identified by a unique URI. Each resource can be represented in multiple formats, such as JSON or XML, and can be manipulated using a set of standard HTTP methods, such as GET, POST, PUT, DELETE, and PATCH. These methods correspond to the basic CRUD (Create, Read, Update, Delete) operations that are typically performed on resources.

RESTful APIs are designed to be stateless, meaning that each request contains all the information necessary to complete the request, and that the server does not maintain any client state between requests. This can help to simplify server-side processing and improve scalability.

Additionally, RESTful APIs often use hypermedia, such as links and forms, to allow clients to discover and navigate the resources available in the API. This can help to make the API more discoverable and self-describing, and can allow clients to adapt to changes in the API more easily.

RESTful APIs should support the following HTTP methods (HTTP verbs). Operation idempotency MUST be respected.

Method  | Description                                                                                                                | Is Idempotent
------- | -------------------------------------------------------------------------------------------------------------------------- | -------------
GET     | Return the current value of an object                                                                                      | True
PUT     | Replace an object, or create a named object, when applicable                                                               | True
DELETE  | Delete an object                                                                                                           | True
POST    | Create a new object based on the data provided, or submit a command                                                        | False
HEAD    | Return metadata of an object for a GET response. Resources that support the GET method MAY support the HEAD method as well | True
PATCH   | Apply a partial update to an object                                                                                        | False
OPTIONS | Get information about a request; see below for details.                                                                    | True

These HTTP methods correspond to the basic CRUD (Create, Read, Update, Delete) operations that are typically performed on resources in a RESTful API. By using these standard HTTP methods, RESTful APIs can provide a simple, consistent, and predictable interface for accessing and manipulating resources.

Note that not all resources will support all of these methods, and some resources may support additional methods that are specific to their functionality. It is also important to ensure that the use of these methods is consistent with the semantics of the resources being manipulated.

For API Guidelines, refer to [Microsoft REST API Guidelines](https://github.com/microsoft/api-guidelines/blob/vNext/Guidelines.md).
