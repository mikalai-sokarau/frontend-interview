### Can you compare TCP/IP and OSI model?
TCP/IP is a model that has four layers: the application layer, transport layer, internet layer, and network access layer. Each layer has a specific function in transferring data over a network.
The OSI model has seven layers: the application layer, presentation layer, session layer, transport layer, network layer, data link layer, and physical layer. Each layer has a specific function and interacts with the layers above and below it.

What's the difference between the two models?
One key difference is the number of layers. TCP/IP has four layers, while OSI has seven layers. This means that the OSI model is more detailed and provides a more granular view of how data is transferred over a network.
Another difference is the way the models are structured. TCP/IP is a simpler model that is easier to implement and use. OSI, on the other hand, is a more complex model that is better suited for larger and more complex networks.

In summary, TCP/IP and OSI are both models that describe how data is transferred over a network. TCP/IP has four layers, while OSI has seven layers. TCP/IP is a simpler model that is easier to use, while OSI is a more complex model that is better suited for larger and more complex networks.

### What happens when you enter a URL in the browser and hit enter?
1. The browser parses the URL and breaks it down into its individual components, which include the protocol (e.g. HTTP, HTTPS), the domain name or IP address, and the path to the resource on the server.
2. The browser checks if the URL has been cached in its local cache. If the URL has been cached, the browser will retrieve the page from the cache instead of making a request to the server.
3. If the URL has not been cached, the browser will make a DNS (Domain Name System) lookup to resolve the domain name in the URL into an IP address. The DNS lookup will use a DNS server to look up the IP address associated with the domain name.
4. Once the IP address has been resolved, the browser will establish a TCP (Transmission Control Protocol) connection with the server using the IP address and the port specified in the URL (usually port 80 for HTTP and port 443 for HTTPS).
5. Once the TCP connection has been established, the browser sends an HTTP request to the server for the resource specified in the URL.
6. The server receives the request, processes it, and sends back an HTTP response to the browser. The response includes the requested resource (e.g. HTML, CSS, JavaScript), as well as any additional resources (e.g. images, videos) referenced in the HTML.
7. The browser receives the response and starts rendering the page. It parses the HTML, CSS, and JavaScript to create the visual representation of the page that you see in the browser.
8. The browser may also make additional requests to the server for resources referenced in the HTML, such as images or videos.
9. Once the page has finished loading, the browser will cache the resources for future use, so that the page can be loaded more quickly if the user visits the same URL again.

### What is the difference between TCP and UDP protocols?
* Connection: TCP is a connection-oriented protocol, which means that a connection is established between the sender and receiver before data is sent. UDP, on the other hand, is a connectionless protocol, which means that data is sent without establishing a connection first.
* Reliability: TCP is a reliable protocol, which means that it guarantees that all data sent will be received by the receiver in the correct order. If any packets are lost or corrupted during transmission, TCP will retransmit them. UDP is an unreliable protocol, which means that it does not guarantee that all data sent will be received by the receiver, and it does not provide any mechanisms for retransmitting lost or corrupted packets.
* Speed: UDP is a faster protocol than TCP because it does not have to establish a connection before sending data, and it does not have the overhead of the reliability mechanisms used by TCP.
* Overhead: TCP has a higher overhead than UDP because it includes additional information in each packet to ensure reliability. This additional overhead can reduce the overall throughput of the network.
* Use cases: TCP is typically used for applications that require reliable data delivery, such as web browsing, email, and file transfers. UDP is typically used for applications that require speed and low overhead, such as online gaming, real-time video and audio streaming, and voice-over-IP (VoIP) services.

### How is a TCP connection established?
A TCP (Transmission Control Protocol) connection is established using a three-way handshake, which involves the following steps:

1. SYN: The client sends a SYN (synchronize) packet to the server, indicating that it wants to establish a connection. The SYN packet includes a random sequence number that the server will use to acknowledge the request.
2. SYN-ACK: The server responds with a SYN-ACK (synchronize-acknowledge) packet, indicating that it has received the client's request and is willing to establish a connection. The SYN-ACK packet includes the server's own random sequence number, as well as an acknowledgment number that acknowledges the client's sequence number.
3. ACK: The client sends an ACK (acknowledge) packet to the server, confirming that it has received the server's response. The ACK packet includes an acknowledgment number that acknowledges the server's sequence number.

Once the three-way handshake is complete, the TCP connection is established, and data can be sent between the client and server.
During the three-way handshake, both the client and server agree on various parameters of the connection, such as the maximum segment size (MSS) and the initial sequence number (ISN). These parameters are used to ensure reliable data transmission and to prevent data loss or corruption.
In summary, a TCP connection is established using a three-way handshake, in which the client sends a SYN packet, the server responds with a SYN-ACK packet, and the client sends an ACK packet. Once the handshake is complete, the TCP connection is established, and data can be sent between the client and server.

### What is the difference between REST and GraphQL?
GraphQL and REST are two popular approaches to building APIs (Application Programming Interfaces) that facilitate communication between clients and servers. While both serve the same purpose of enabling client-server interactions, they differ in several key aspects. Let's compare GraphQL and REST across different dimensions:

Data Fetching: In REST, each endpoint represents a specific resource, and the client sends a request to that endpoint to fetch or manipulate the resource. In GraphQL, there is a single endpoint, and the client can send a GraphQL query specifying the exact data it needs, allowing the server to respond with precisely that data in a single request. This enables clients to avoid over-fetching or under-fetching data.

Response Structure: REST endpoints typically have fixed response structures defined by the server. Clients have limited control over the shape and size of the response. In GraphQL, the client specifies the structure of the response by defining the fields it needs in the query. This allows for flexibility and eliminates the problem of over-fetching or under-fetching data.

Efficiency: REST APIs can suffer from over-fetching, where the server sends more data than the client requires, resulting in inefficient network usage and increased latency. GraphQL solves this problem by allowing clients to request only the data they need, reducing the number of requests and optimizing network usage.

Versioning: REST APIs often require versioning to introduce changes to the API. When a REST API evolves, clients may need to switch to a new version explicitly. In GraphQL, since clients request the exact fields they need, the server can evolve the API without requiring versioning. It can deprecate or add fields to the schema without impacting existing clients.

Type System: GraphQL has a strongly typed schema that defines the structure of the data available in the API. Clients can query this schema to discover available data and their types. REST APIs, on the other hand, lack a standardized schema, making it harder for clients to understand the available resources and their relationships.

Caching: REST APIs can leverage HTTP caching mechanisms effectively, such as ETag or Last-Modified headers, to enable caching at the network level. GraphQL does not have built-in caching mechanisms, but it allows clients to specify the desired cache control headers, and servers can implement caching strategies accordingly.

Tooling and Ecosystem: REST has been around for a long time and has a mature ecosystem with extensive tooling and support. GraphQL is relatively newer but has gained significant popularity. It also has a growing ecosystem with libraries, tools, and community support, although it may not be as extensive as that of REST.

The choice between GraphQL and REST depends on the specific requirements of your application. GraphQL is often favored when you need flexibility, efficient data fetching, and a strongly typed schema. REST, with its simplicity and widespread adoption, might be a better fit for smaller or more straightforward projects where a fixed resource-based approach suffices.

### GraphQL pros and cons
Pros:
1. Efficient Data Fetching: GraphQL allows clients to request exactly the data they need in a single query, eliminating over-fetching and under-fetching of data. This improves performance by reducing the amount of data transferred over the network.
2. Flexible and Declarative Queries: Clients can define their queries in a flexible and declarative manner, specifying the fields, relationships, and even nested data they require. This gives clients more control over the shape and structure of the response and simplifies the development process.
3. Strongly Typed Schema: GraphQL has a strongly typed schema, which provides a contract between the client and server. This schema acts as a single source of truth, documenting the available data, types, and relationships. It enables better collaboration, error checking, and tooling support.
4. Schema Stitching and Composition: GraphQL allows you to stitch together or compose data from multiple services or APIs into a single GraphQL schema. This promotes a modular architecture, where different services expose their own GraphQL APIs, and the client can query and retrieve data from multiple sources seamlessly.
5. Incremental Adoption: GraphQL can be incrementally adopted within an existing system or alongside existing REST APIs. You can start by implementing GraphQL for specific parts of an application and gradually expand its usage as needed, allowing for a smooth transition.
6. Real-time Capabilities: GraphQL supports real-time data with subscriptions. Clients can subscribe to specific data changes and receive updates in real-time, making it suitable for applications that require live updates, such as chat applications or real-time dashboards.

Cons:
1. Learning Curve: GraphQL has a learning curve, especially for developers who are unfamiliar with its concepts and syntax. Understanding how to design schemas, write efficient queries, and implement resolvers requires some initial investment in learning.
2. Backend Complexity: Implementing a GraphQL server introduces additional complexity on the backend. You need to define and maintain a schema, write resolvers to fetch data from various sources, and handle query parsing and validation.
3. Caching and Caching Validation: GraphQL does not have built-in caching mechanisms like REST. Implementing caching strategies in GraphQL requires additional effort and careful consideration. Cache invalidation can also be challenging, especially when dealing with complex queries and data relationships.
4. Performance Impact: Although GraphQL can improve efficiency by reducing over-fetching, poorly designed or inefficient queries can still impact performance. Care must be taken to optimize and structure queries effectively to avoid performance issues, especially when dealing with complex data fetching requirements.
5. Lack of Standardization: GraphQL, being a relatively newer technology compared to REST, lacks some standardization in certain areas. Best practices and conventions are still evolving, which can lead to inconsistencies across different GraphQL implementations and frameworks.





