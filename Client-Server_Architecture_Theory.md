
## Content
### [Types of Client-Server Architecture](https://github.com/DariaMartinovskaya/Client-Server/blob/main/Client-Server_Architecture_Theory.md#types-of-client-server-architectures)
### [OSI Model and TCP/IP Model](https://github.com/DariaMartinovskaya/Client-Server/blob/main/Client-Server_Architecture_Theory.md#osi-model-and-tcpip-model-1)
### [HTTP Protocol](https://github.com/DariaMartinovskaya/Client-Server/blob/main/Client-Server_Architecture_Theory.md#http-protocol-1)
### [API](https://github.com/DariaMartinovskaya/Client-Server/blob/main/Client-Server_Architecture_Theory.md#api-1)
### [Proxy](https://github.com/DariaMartinovskaya/Client-Server/blob/main/Client-Server_Architecture_Theory.md#proxy-1)

# Client-Server Architecture
A Client (=user agent) is either a person or an organization using as a service. In the IT context, the client is a computer/device that actually uses the service or accepts the information (Browser, Postman, SOAP UI, JMeter, Java app may act as a client).

A Server (=web server=Host)  is a remote computer that provides access to data and services. Servers are usually physical devices such as rack servers, though the rise of cloud computing has brought virtual servers into the equation. The server handles processes like e-mail, application hosting, Internet connections, printing, and more.

Client-server architecture, alternatively called a client-server model, is a network application that breaks down tasks and workloads between clients and servers that reside on the same system or are linked by a computer network.

Client-server architecture typically features multiple users’ workstations, PCs, or other devices, connected to a central server via an Internet connection or other network. The client sends a request for data, and the server accepts and accommodates the request, sending the data packets back to the user who needs them.

To sum it up briefly:

- First, the client sends their request via a network-enabled device

- Then, the network server accepts and processes the user request

- Finally, the server delivers the reply to the client

## Types of Client Server Architectures
Client server architecture consists of the following four types:
#### 1-Tier Structure
In a 1-tier architecture, the user interface, business logic, and data logic are all on the same system. Because the client and server are on the same system, the environment is straightforward and inexpensive, but the variation in the data necessitates repetitive effort. These systems keep their data in a shared driver or a local file. 

Examples: MP3 player and MS Office files.
#### 2-Tier Structure
In a two-tier architecture, also known as the client-server model, there are two main layers: the client and the server. The client communicates directly with the server to request services or data. This model is straightforward and often used in client-server database systems, where the client application sends queries or requests directly to the database server. 

Example: online ticket reservation systems, 1C.
![1](https://img-16.ccm2.net/A8zTYwwaE2vMgVyzhYezDn6mXtU=/377x/32e66bb2e13a4c0988f0c5656499c599/ccm-encyclopedia/cs-images-2-tier.gif)

While the database is on the server side, the user interface is client-side. Both the client and server end can store the database and business logic. The design is known as a fat client-thin server architecture if both sit at the client end. On the other hand, the design is known as a thin client-fat server architecture if both sit at the server end. 


Example of thin client-fat server architecture: Google Docs.

Examples of fat client-thin server architecture: Yahoo Messenger, Office 365, Microsoft Outlook, 1C.
#### Load balancer
![11](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*tEaZGz-p1-E2ytNjl5RPJg.jpeg)

A typical load balancing system consists of three main components: clients, servers, and load balancers. Clients are the devices or applications that initiate requests for services or resources from the servers. Servers are the machines or programs that provide the services or resources to the clients. Load balancers are the devices or software that act as intermediaries between the clients and the servers, receiving the requests from the clients and forwarding them to the appropriate servers. Load balancers can be either hardware or software-based, and can be deployed at different levels of the network, such as the application layer, the transport layer, or the network layer.

####  3-Tier Structure
Three-tier architecture builds upon the two-tier model by introducing an additional layer, known as the middle tier (middleware) or application server, between the client and the server. This architecture separates the user interface, application logic, and data management functionalities into three distinct layers:

Presentation Layer (Client): The client interface where users interact with the application.

Application Layer (Middle Tier): This layer contains the application logic responsible for processing client requests and coordinating interactions between the client and the data management layer.

Data Management Layer (Server): The server layer responsible for storing, retrieving, and managing data.

![2](https://img-16.ccm2.net/8LPyCnrv7QKfHC_6kxfD_qzWeH0=/500x/d83dfb440bb64db3a1d9f7b3f66b985b/ccm-encyclopedia/cs-images-3-tier.gif)

Three-tier architecture enhances modularity and scalability by separating concerns and allowing each layer to evolve independently. It improves performance and simplifies maintenance by distributing tasks across different layers, making it easier to manage and update the system.

Examples: online applications (in almost all cases).

#### N-Tier or Multi-Tiered Architecture

In 3-tier architecture, each server (tier 2 and 3) performs a specialized task or service. A server can, therefore, use services from other servers in order to provide its own service. As a result, 3-tier architecture is potentially an n-tiered architecture:
![3](https://img-16.ccm2.net/B3HmYlRDwgHHMHO2MGh44lmHvYY=/344x/15b16c05450b4a7abd77bdf6715fb418/ccm-encyclopedia/cs-images-n-tier.gif)

Examples: MakeMyTrip.com, Sales Force enterprise application, Indian Railways – IRCTC, Amazon.com.


## OSI Model and TCP/IP Model

Data communication is a process or act in which we can send or receive data. For data communication two models are available:

OSI Model

TCP/IP Model

### OSI Model
OSI stands for Open Systems Interconnection. It has 7 layers. Each layer performs its task independently. It was the first standard model for network communications, adopted by all major computer and telecommunication companies in the early 1980s.
The modern Internet is not based on OSI, but on the simpler TCP/IP model. However, the OSI 7-layer model is still widely used, as it helps visualize and communicate how networks operate, and helps isolate and troubleshoot networking problems.

![4](https://www.imperva.com/learn/wp-content/uploads/sites/13/2020/02/OSI-7-layers.jpg)

##### Advantages

- Both connection-oriented services and connectionless services are supported.
- It is quite flexible.
- All the layers work independently.

##### Disadvantages

- Setting up a model is a challenging task.
- Sometimes, it becomes difficult to fit a new protocol into this model.
- It is only used as a reference model.
  
### TCP/IP Model
TCP/IP is a data link protocol used on the internet to let computers and other devices send and receive data. TCP/IP stands for Transmission Control Protocol/Internet Protocol and makes it possible for devices connected to the internet to communicate with one another across networks.
It has 4 layers named as Physical layer, Network layer, Transport layer, and Application layer.  It also can be used as a communications protocol in a private computer network. 

![10](https://www.guru99.com/images/1/093019_0615_TCPIPModelW2.png)

##### Advantages

- Many Routing protocols are supported.
- It is highly scalable and uses a client-server architecture.
- It is lightweight.
  
##### Disadvantages
- Little difficult to set up.
- Delivery of packets is not guaranteed by the transport layer.
- Vulnerable to a synchronization attack.
  
#### IP Address
An IP address is a collection of numbers assigned to devices that facilitate communication and exchange of information over the internet.
For example, if you want to collect information regarding whales, you send a request to the website that contains the relevant information. The request goes from your computer, which has a unique IP address, to the server containing the relevant information, with its unique IP address. Once the server gets the request, it processes the request and sends back the relevant information. This to-and-fro communication is possible through the use of IP addresses.

An IP address has two parts: the network ID, comprising the first three numbers of the address, and a host ID, the fourth number in the address. So on your home network — 192.168.1.1, for example – 192.168.1 is the network ID, and the final number is the host ID.

The different versions of IP addresses include:

IPV4: The IPV4 address contains four numerals, each being one to three digits separated by a dot. Some examples are 192.168.0.1 and 10.2.3.4.

IPV6: The newly introduced IPV6 address contains a 128-bit alphanumeric value, divided into eight 16-bit blocks, to identify devices on the Internet. An example includes 2000:0db9:84a4:0000:0000:9a3e::7125.

## OSI Model vs. TCP/IP Model
![5](https://www.imperva.com/learn/wp-content/uploads/sites/13/2020/02/OSI-vs.-TCPIP-models.jpg)



TCP/IP is older than the OSI model. A key difference between the models is that TCP/IP is simpler, collapsing several OSI layers into one:

OSI layers 5, 6, 7 are combined into one Application Layer in TCP/IP

OSI layers 1, 2 are combined into one Network Access Layer in TCP/IP – however TCP/IP does not take responsibility for sequencing and acknowledgement functions, leaving these to the underlying transport layer.

Other important differences:

TCP/IP is a functional model designed to solve specific communication problems, and which is based on specific, standard protocols. OSI is a generic, protocol-independent model intended to describe all forms of network communication.

In TCP/IP, most applications use all the layers, while in OSI simple applications do not use all seven layers. Only layers 1, 2 and 3 are mandatory to enable any data communication.

Similarities between OSI Model and TCP/IP Model 

OSI and TCP/IP both are logical models. 

One of the main similarities between the OSI and TCP/IP models is that they both describe how information is transmitted between two devices across a network. Both models define a set of layers. Each layer performs a specific set of functions to enable the transmission of data.

Another similarity between the two models is that they both use the concept of encapsulation, in which data is packaged into a series of headers and trailers that contain information about the data being transmitted and how it should be handled by the network.

## HTTP Protocol
The Hypertext Transfer Protocol (HTTP) is the foundation of the World Wide Web, and is used to load webpages using hypertext links. HTTP is an application layer protocol designed to transfer information between networked devices and runs on top of other layers of the network protocol stack. A typical flow over HTTP involves a client machine making a request to a server, which then sends a response message.

![8](https://developer.mozilla.org/en-US/docs/Learn/Server-side/First_steps/Client-Server_overview/web_application_with_html_and_steps.png)

### HTTP Request

HTTP request includes:
- A URL identifying the target server and resource (e.g. an HTML file, a particular data point on the server, or a tool to run).

- A method that defines the required action (for example, to get a file or to save or update some data). The different methods/verbs and their associated actions are listed below:

-- GET: Get a specific resource (e.g. an HTML file containing information about a product, or a list of products).

-- POST: Create a new resource (e.g. add a new article to a wiki, add a new contact to a database).

-- HEAD: Get the metadata information about a specific resource without getting the body like GET would. You might for example use a HEAD request to find out the last time a resource was updated, and then only use the (more "expensive") GET request to download the resource if it has changed.

-- PUT: Update an existing resource (or create a new one if it doesn't exist).

-- DELETE: Delete the specified resource.

-- TRACE, OPTIONS, CONNECT, PATCH: These verbs are for less common/advanced tasks, so we won't cover them here.

- Additional information can be encoded with the request (for example, HTML form data). Information can be encoded as:

-- URL parameters: GET requests encode data in the URL sent to the server by adding name/value pairs onto the end of it — for example http://example.com?name=Fred&age=11. You always have a question mark (?) separating the rest of the URL from the URL parameters, an equals sign (=) separating each name from its associated value, and an ampersand (&) separating each pair. URL parameters are inherently "insecure" as they can be changed by users and then resubmitted. As a result URL parameters/GET requests are not used for requests that update data on the server.

-- POST data. POST requests add new resources, the data for which is encoded within the request body.

-- Client-side cookies. Cookies contain session data about the client, including keys that the server can use to determine their login status and permissions/accesses to resources.

The most popular methods can be grouped to:

![CRUD](https://www.atatus.com/blog/content/images/2022/12/crud-operations.png)

Web servers wait for client request messages, process them when they arrive, and reply to the web browser with an HTTP Response message. The response contains an HTTP Response status codeindicating whether or not the request succeeded (e.g. "200 OK" for success, "404 Not Found" if the resource cannot be found, "403 Forbidden" if the user isn't authorized to see the resource, etc.). The body of a successful response to a GET request would contain the requested resource.

When an HTML page is returned it is rendered by the web browser. As part of processing, the browser may discover links to other resources (e.g. an HTML page usually references JavaScript and CSS files), and will send separate HTTP Requests to download these files.

Both static and dynamic websites (discussed in the following sections) use exactly the same communication protocol/patterns.

### HTTP Request Structure
![HTTPRequestStructure](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*oy4-WDRk2mYmbNv7.jpg)

​​Queries have the following structure:

- The start line. It is used to describe the request or the status of the request. Indicates the protocol version and other information. Contains the requested resource or a response code (eg error). It is exactly one line in length.
- HTTP header. Looks like a few lines of text specifying the request or describing the content of the message body.
- An empty string. This is necessary as an indication that the metadata for a particular request has been successfully sent.
- The request body. This contains information about the request or the document sent in response to the request.

A request method is considered idempotent if the intended effect on the server of multiple identical requests with that method is the same as the effect for a single such request. And it's worthwhile to mention that idempotency is about the effect produced on the state of the resource on the server and not about the response status code received by the client.  Idempotent methods are GET, PUT, DELETE, HEAD.


### HTTP response: most common status codes
HTTP response status codes (or simply status codes) are three-digit codes issued by a server in response to a browser-side request from a client. 

There are five different categories of HTTP status codes, and they are classified based on the type of response the server communicates to the client:

- 1XX – Informational code: This category indicates that the request was received and understood. It is issued on a provisional basis while request processing continues. It alerts the client to wait for a final response. The message consists only of the status line and optional header fields, and is terminated by an empty line.

- 2XX – Success code: This category indicates the action requested by the client was received, understood, and accepted. 

- 3XX – Redirection code: This category indicates that the client may take additional action to complete the request. Usually that additional action is to redirect the user to another URL. Many of the status codes in this category are used in URL redirection.

- 4XX – Client error code: This category indicates that request cannot be fulfilled because there is an error coming from the client. 

- 5XX – Server error code:This category indicates that the server has encountered an error or is incapable of performing a valid request. 

Listed below are the most common HTTP response status codes for each category.

A. Informational codes

100 Continue

This status code indicates that everything is fine, and that the browser should continue with the request or ignore it if it is already finished. 

101 Switching Protocols

This status code indicates the server is willing to switch the application protocol used in the connection as requested by a browser via the Upgrade request header. The server will also include in the response an Upgrade response header to indicate the protocol it switched to.

103 Early Hints

This status code is used together with the Link header to allow the user-agent (e.g. browser) to start preloading resources while the server is still preparing a response.

B. Success codes

200 OK

This status code indicates that the request has succeeded. The meaning of a success depends on the HTTP request method:

GET: The requested resource has been transmitted in the response together with the message body.

HEAD: The representation headers are transmitted in the response without any message body.

POST: The resource describing the result of the action is transmitted in the response.

TRACE: The response contains the request message as received by the server.

The status code for successful result of PUT or DELETE is often not a 200 OK, but a 204 No Content, or a 201 Created if the resource is uploaded for the first time. A 200 response is cacheable by default.

201 Created

This status code indicates that the request has succeeded and has resulted in the creation of a new resource. 

202 Accepted

This status code indicates that the request has been accepted for processing, and the processing has not been completed or started. 

203 Non-Authoritative Information

This status code indicates that the request was successful but the enclosed payload has been modified by a transforming proxy from the origin server’s 200 OK response. 

204 No Content

This status code indicates that a request has succeeded, but does not need to return a body, so that the client doesn’t need to navigate away from its current page. The 204 response doesn’t include a body, and thus is always terminated by the first empty line after the header field.

C. Redirection codes

300 Multiple Choices

This status code indicates that the request has more than one possible response. The user-agent or the user should choose one of them. Unless it was a HEAD request, the response will include a list of resource characteristics and location(s) from which the user can choose from. 

301 Moved Permanently

This status code indicates that the resource requested has been definitively moved to the new permanent URI. 

302 Found

This status code indicates that the resource requested has been temporarily moved to the URI. 

303 See Other

This status code indicates that the redirects don’t link to the newly uploaded resources, but to a custom page (e.g. confirmation page or upload progress page). This status code is usually sent back as a result of PUT or POST. The method used to display this redirected page is always GET.

304 Not Modified

This status code indicates that there is no need to retransmit the requested resources. It is an implicit redirection to a cached resource. 

307 Temporary Redirect

This status code indicates that the resource requested has been temporarily moved to the URI. 

308 Permanent Redirect

This status code indicates that the resource requested has been definitively moved to the URI. 

D. Client error codes

400 Bad Request

This status code indicates that the server cannot process the request due to an error on the client side, e.g. malformed request syntax, invalid request message framing, or deceptive request routing. The client is advised to not repeat the request unless modifications are made.

401 Unauthorized

This status code indicates that the request has not been applied because it lacks valid authentication credentials for the target resource. 

402 Payment Required

This status code is a nonstandard client error and is reserved for future use. Originally it was created to enable digital cash or payment systems and would indicate that the request can not be processed until the client makes a payment. However, no standard use convention exists and different entities use it in different contexts.

403 Forbidden

This status code indicates that the server understood the request but refuses to authorize it.

This status is similar to 401 Unauthorized, but in this case, re-authenticating will make no difference, so there is no need to repeat the request. The access is permanently forbidden and tied to the application logic, such as insufficient rights to a resource. 

404 Not Found

This status code indicates that the server can’t find anything matching the Request-URI. Links that lead to a 404 page are often called broken or dead links and can be subject to link rot. 

405 Method Not Allowed

This status code indicates that the request method is known by the server but is not supported by the target resource. The method specified in the Request-Line is not allowed for the resource identified by the Request-URI. 

408 Request Timeout

This status code indicates that the server would like to shut down this unused connection, because the request exceeded the time that the server was prepared to wait. 

409 Conflict

This status code indicates a request cannot be completed because of a conflict with the current state of the target resource. This code is allowed in situations where it is expected that the client might be able to resolve the conflict and resubmit the request. Hence, the response body should include enough information for the client to recognize the source of the conflict.

410 Gone

This status code indicates that access to the target resource is no longer available permanently at the origin server and no forwarding address is known. 

414 URI Too Long

This status code indicates that the server refuses to process the request because the Request-URI provided by the client is longer than the server is willing to interpret.

415 Unsupported Media Type

This status code indicates that the server refuses to accept the request because the payload format is in an unsupported format. 

418 I’m a teapot

This status code indicates that the server refuses to brew coffee because it is, permanently, a teapot. 

429 Too Many Requests

This status code indicates the user has sent too many requests in a given amount of time (“rate limiting”). 

E. Server error codes

500 Internal Server Error

This status code indicates that the server encountered an unexpected condition which prevented it from fulfilling the request. This error response is usually used as a generic “catch-all” response indicating that the server cannot find a better 5xx status code to respond. 

501 Not Implemented

This status code means that the server does not support the functionality required to fulfill the request. 

502 Bad Gateway

This status code indicates that the server, while acting as a gateway or proxy, received an invalid response from the upstream server in attempting to fulfill the request. 

503 Service Unavailable

This status code indicates that the server is currently unavailable and is not ready to handle any request due to a temporary overloading or maintenance of the server. This response is used as a temporary measure which is expected to be alleviated after some time. 

504 Gateway Timeout

This status code indicates that the server, while acting as a gateway or proxy, did not get a timely response from the upstream server specified by the URI (e.g. HTTP, FTP, LDAP) or some other auxiliary server (e.g. DNS) in attempting to fulfill the request. 

Post navigation.

### HTTP Response Structure
![HTTPResponse](https://developer.mozilla.org/en-US/docs/Web/HTTP/Messages/httpmsgstructure2.png)

### HTTPS, SSL/TLC
Hypertext transfer protocol secure (HTTPS) is the secure version of HTTP, which is the primary protocol used to send data between a web browser and a website.

Secure Sockets Layer (SSL) is the technology responsible for data authentication and encryption for internet connections. It encrypts data being sent over the internet between two systems (commonly between a server and a client) so that it remains private. And with the growing importance of online privacy, an SSL port is something you should get familiar with.
Because data can be sent with or without the use of SSL, one way to indicate a secure connection is by the port number. By default, HTTPS connections use TCP port 443. HTTP, the unsecure protocol, uses port 80.

Transport Layer Security (TLS) is an update to the SSL protocol. 

## API
API stands for Application Programming Interface. 
An API is a set of programming code that enables data transmission between one software product and another. It also contains the terms of this data exchange.
The application programming interface must be clearly distinguished from a user interface. The user interface accepts data from users, forwards it to the application for processing, and returns the results to the user. The API does not interact with the user, but processes the data received from one program module and transmits the results back to the other module. Here’s how it happens.

![API](https://www.altexsoft.com/media/2019/06/1.png)

The working principle of an API is commonly expressed through the request-response communication between a client and a server. The client is any front-end application that a user interacts with. The server is in charge of backend logic and database operations. In this scenario, an API works as a middle layer between the client and the server, making it possible to send data requests and responses.

## Proxy
A proxy server is an intermediary server placed between the client and the server. As in the image below, a client forwards the request to the Proxy, the proxy forwards the request to the server and forwards the incoming response to the client.
![6](https://miro.medium.com/v2/resize:fit:1364/format:webp/1*J3vKylY8M22ByuTyQRADtA.png)

Functions:
- Data cash
- Filtering
- Load balancer
- Authentication (access control)
- Historing

Sources: 
1. https://www.simplilearn.com/what-is-client-server-architecture-article
2. https://medium.com/@nirajranasinghe/understanding-client-server-architecture-in-system-design-9da079efde60
3. https://ccm.net/computing/networks/10095-networking-3-tier-client-server-architecture/
4. https://www.geeksforgeeks.org/difference-between-osi-model-and-tcp-ip-model/
5. https://www.imperva.com/learn/application-security/osi-model/#:~:text=Cybersecurity%20101-,What%20Is%20the%20OSI%20Model,companies%20in%20the%20early%201980s
6. https://www.avg.com/en/signal/what-is-tcp-ip#:~:text=There%20are%20four%20layers%20of,when%20the%20data%20is%20received.
7. https://www.avast.com/c-what-is-an-ip-address
8. https://www.avg.com/en/signal/what-is-tcp-ip#:~:text=There%20are%20four%20layers%20of,when%20the%20data%20is%20received.
9. https://www.linkedin.com/advice/0/what-role-load-balancing-client-server-architecture-my4ke
10. https://developer.mozilla.org/en-US/docs/Learn/Server-side/First_steps/Client-Server_overview
11. https://alitunacanonar.medium.com/what-is-proxy-server-and-how-does-it-work-2d9224cc459e
12. https://medium.com/@adilrk/http-request-and-response-e7da8eb3a00c
13. https://learning.mlytics.com/the-internet/http-response-status-codes/
14. https://developer.mozilla.org/en-US/docs/Web/HTTP/Messages
15. https://www.godaddy.com/resources/skills/whats-an-ssl-port-a-technical-guide-for-https
16. https://www.altexsoft.com/blog/what-is-api-definition-types-specifications-documentation/
