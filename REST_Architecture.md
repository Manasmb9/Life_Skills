# Rest Architecture
REST stands for Representational State Transfer and API stands for 
Application Program Interface. 

REST is a software architectural style that defines the set of rules to be used for creating web services. Web services which follow the REST architectural style are known as RESTful web services. It allows requesting systems to access and manipulate web resources by using a uniform and predefined set of rules. Interaction in REST based systems happen through Internet’s Hypertext Transfer Protocol (HTTP). 

REST as a network architecture was first documented by Roy Fielding in his doctoral thesis titled Architectural Styles and the Design of Network-based Software Architectures, published in 2000. 

REST allows clients to interact with data stored on a server, without having any prior knowledge of the server or what exists on it.

![rest_api](https://user-images.githubusercontent.com/117135545/200835183-d7018d40-9dad-43ed-817f-6f3bd8427d01.svg)


The web services that follows the REST architectural style is called RESTful Web Services. It differentiates between the computer system and web services. The REST architectural style describes the six barriers.

![what-is-rest](https://user-images.githubusercontent.com/117135545/200836014-da206710-7b74-4898-882f-20454f3abaa5.png)

### 1. Uniform Interface

The Uniform Interface defines the interface between client and server. It simplifies and decomposes the architecture which enables every part to be developed. The Uniform Interface has four guiding principles:

#####  Resource-based: 

Individual resources are identified using the URI as a resource identifier. The resources themselves are different from the representations returned to the customer. For example, the server cannot send the database but represents some database records expressed to HTML, XML or JSON depending on the server request and the implementation details.

#####  Manipulation of resources by representation: 

When a client represents a resource associated with metadata, there is information on the server to modify or delete it.

#####  Self-Descriptive Message: 

Each message contains enough information to describe how the message is processed. For example, the parser can be specified by the Internet media type (known as the MIME type).

#####  As the engine of Hypermedia Application State (HATEOAS): 

Customers provide states by query-string parameters, body content, request headers, and requested URIs. The services provide customers with the state by response codes, response headers and body content. It is called hypermedia (hyperlink within hypertext).

In addition to the above description, HATEOS also means that, where necessary, the object or itself is contained in the linked body (or header) to supply the URI for retrieving the related objects.

The same interface that any REST services provide is fundamental to the design.
### 2. Client-server

A client-server interface separates the client from the server. For Example, the separation of concerns not having an internal relationship with internal storage for each server to improve the portability of customer's data codes. Servers are not connected with the user interface or user status to make the server simpler and scalable. Servers and clients are independently replaced and developed until the interface is changed.

### 3. Stateless

Stateless means the state of the service doesn't persist between subsequent requests and response. It means that the request itself contains the state required to handle the request. It can be a query-string parameter, entity, or header as a part of the URI. The URI identifies the resource and state (or state change) of that resource in the unit. After the server performs the appropriate state or status piece (s) that matters are sent back to the client through the header, status, and response body.
Play Videox

Most of us in the industry have been accustomed to programming with a container, which gives us the concept of "session," which maintains the status among multiple HTTP requests. In REST, the client may include all information to fulfil the server's request and multiple requests in the state. Statelessness enables greater scalability because the server does not maintain, update, or communicate any session state. The resource state is the data that defines a resource representation.
Example, the data stored in a database. Consider the application state of having data that may vary according to client and request. The resource state is constant for every customer who requests it.

### 4. Layered system

It is directly connected to the end server or by any intermediary whether a client cannot tell. Intermediate servers improve the system scalability by enabling load-balancing and providing a shared cache. Layers can enforce security policies.

### 5. Cacheable

On the World Wide Web, customers can cache responses. Therefore, responses clearly define themselves as unacceptable or prevent customers from reusing stale or inappropriate data to further requests. Well-managed caching eliminates some client-server interactions to improving scalability and performance.

### 6. Code on Demand (optional)

The server temporarily moves or optimizes the functionality of a client by logic that it executes. Examples of compiled components are Java applets and client-side scripts.

Compliance with the constraints will enable any distributed hypermedia system with desirable contingency properties such as performance, scalability, variability, visibility, portability, and reliability.

## Rest Architecture Details

REST is an architecture style for designing networked applications. The idea is that, rather than using complex mechanisms such as CORBA, RPC or SOAP to connect between machines, simple HTTP is used to make calls between machines.

### HTTP — HyperText Transfer Protocol

HTTP means HyperText Transfer Protocol. HTTP is the underlying protocol used by the World Wide Web and this protocol defines how messages are formatted and transmitted, and what actions Web servers and browsers should take in response to various commands.

![0_-eISVKVca9dJ-N04](https://user-images.githubusercontent.com/117135545/200839450-8299ff48-4973-493f-92c3-d27bbd99b0d8.jpeg)

HTTP is the protocol that allows for sending documents back and forth on the Web. And, REST is the architecture that uses HTTP protocol to provide functionalities depends the requirements of software applications or Web pages in a very light-weight, simple and effective way!

RESTful applications use HTTP requests to post data (create and/or update), read data (e.g., make queries), and delete data. Thus, REST uses HTTP for all four CRUD (Create/Read/Update/Delete) operations.


![1_tmvBCo4fCH-ms7X8tsOPQg](https://user-images.githubusercontent.com/117135545/200839767-8d8dd677-5d3d-489b-ac3e-2f3f0545fbf5.jpeg)

### Benefits of using REST Architecture
Here are 5 benefits of using REST architecture:

##### RESTful as lightweight Web Services: 

The RESTful architecture was a reaction to the more heavy-weight SOAP-based standards. In REST web services, the emphasis is on simple point-to-point communication over HTTP using plain XML. In addition, RESTful permits many different data formats whereas SOAP only permits XML.

##### The simplicity of RESTful: 

The RESTful architecture is much simpler to develop than SOAP. One of the main reasons for REST popularity is the simplicity and ease of use, as it does an extension of native Web technologies such as HTTP.
##### RESTful architecture is closer in design to the Web:

RESTful is the architectural style of the web itself, so the developer with knowledge in web architecture will naturally develop in the RESTful architecture.

##### Scalability: 
As RESTful forbids conversational state, which means we can scale very wide by adding additional server nodes behind a load balancer.

##### Expose APIs as HTTP Services: 

When developers need the universal presence with minimum efforts, given the fact that RESTful APIs are exposed as HTTP Services, which is virtually present on almost all the platforms.

Client context is never stored on the server between requests. Each request has to contain all the necessary information. A stateless server improves scalability by allowing the server to quickly free resources and simplifies implementation. Reliability eases recovering from partial failures. Visibility, monitoring system does not have to look beyond a single request to determine the nature of the request.

## Advantages and disadvantages of REST

There are several advantages to using REST. They are as follows:

##### Resource-based. 

A primary benefit of using REST, from both a client and server perspective, is that REST interactions are based on constructs which are familiar to anyone accustomed to using HTTP. Employing a resource-based approach, REST defines how developers interact with web services.

##### Communication. 

REST-based interactions communicate their status through numerical HTTP status codes. REST APIs use these HTTP status codes to detect errors and ease the API monitoring process. They include the following:
404 error indicates that a requested resource wasn't found;
401 status response code is triggered by an unauthorized request;
200 status response code indicates that a request was successful; and
500 error signals an unrecoverable application fault on the server.

##### Familiarity. 

Most developers are already familiar with key elements of the REST architecture, such as Secure Sockets Layer (SSL) encryption and Transport Layer Security (TLS).

##### Language-independent. 

When creating RESTful APIs or web services, developers can employ any language that uses HTTP to make web-based requests. This capability makes it easy for programmers to choose the technologies they prefer to work with and that best suit their needs.
##### Pervasive. 

The popularity of REST is due to its widespread use in both server- and client-side implementations. For example, on the server side, developers can employ REST-based frameworks, including Restlet and Apache CXF. On the client side, developers can employ a variety of frameworks (i.e., jQuery, Node.js, Angular, EmberJS, etc.) and invoke RESTful web services using standard libraries built into their APIs.
##### Web APIs. 

When it comes to caching, RESTful services employ effective HTTP mechanisms. For example, by providing many endpoints, a REST API makes it easier for developers to create complex queries that can meet specific deployment needs.

### Disadvantages of REST are as follows:

##### Architecture. 

Developers working with REST frequently encounter limitations due to its architecture design. These include multiplexing multiple requests over a single TCP connection, having different resource requests for each resource file, server request uploads, and long HTTP request headers, which cause delays in webpage loading.
##### Stateless applications. 

Since HTTP does not store state-based information between request-response cycles, the client must perform state management tasks. This makes it difficult for programmers to implement server updates without the use of client-side polling or other types of webhooks that send data and executable commands from one app to another.
##### Definition. 

Developers generally disagree over defining REST-based designs. As an architectural style, REST lacks a clear reference implementation or a definitive standard that designates whether a specific design can be defined as RESTful. This also leads to uncertainty over whether a given web API conforms to REST-based principles.
##### Data overfetching/underfetching. 

RESTful services frequently return large amounts of unusable data combined with relevant information, typically the result of multiple server queries. These inefficiencies also increase the time it takes for a client to return all the required data.

## Alternatives to REST

Alternate technologies for creating SOA-based systems or creating APIs for invoking remote microservices include XML over HTTP (XML-RPC), CORBA, RMI over IIOP and the Simple Object Access Protocol (SOAP).

In general, every technology has benefits and drawbacks. However, a unique feature of REST is that instead of requiring that developers work with custom protocols for client-server message exchanges, REST insists that the best way to implement network-based web services is to use the basic construct of the network protocol itself, which in terms of the internet is HTTP.

This is an important component, as REST is not intended to apply just to the internet; rather, its principles are intended to apply to all protocols, including WebDav and FTP.


## Conclusion
REST is an architectural pattern which is based on HTTP and uses HTTP requests, responses, verbs and status codes to communicate.
The fact that REST services use HTTP means they can be consumed by almost any ‘online’ device or application (including IoT devices such as toasters, cars, pedometers etc) — no proprietary knowledge of the API is required! This is freaking awesome!!!
REST is a cool phenomena of Web Technologies and it always makes us excited to develop light-weight and robust systems that are built on top of REST Architecture to interact using Web!

## References

https://www.geeksforgeeks.org/rest-api-architectural-constraints/

https://restfulapi.net/rest-architectural-constraints/

https://www.javatpoint.com/what-is-rest

https://www.techtarget.com/searchapparchitecture/definition/REST-REpresentational-State-Transfer
