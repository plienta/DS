# BI (Business Intelligence)

## communicate between system and system through web-sevice (API)

1. Business needs
2. Easy maintainance
3. Technology evolution
4.

``` mermaid
graph TD;
    A(NEC)-->B(Delivery);
    B-->A;
    A-->C(Toreta);
    C-->A;
    B-->C;
    C-->B;
```

## Interface

### Intergrate 2 bank
1. Get A/B remove the other
2. Intergrate C = A + B
3. Develop C
4. keep both A and B
5. The mix of 2 and 4
<li> Must merge the data
<li> Cannot merge some
    
## Webservices application
### What is a Web Service?
A Web service is a collection of open protocols and standards which are widely used for exchanging data between systems or applications.
Software applications are written using various programming languages and running on multiple platforms. It allows you to use web services to exchange data over computer networks.

### Types of Web Services
Web services should be implemented in various ways. The two types of widely used web services are SOAP and RESTful web services.

<li>SOAP – SOAP is a protocol which was designed before REST came into the picture. The main idea behind creating SOAP was to ensure that programs built on different platforms and programming languages could securely exchange data.</li>
<li>REST – This was designed specifically for working with components such as media components, files, or even objects on a particular hardware device. Any web service which is defined on the principles of REST can be called a RESTful web service. REST uses the normal HTTP verbs of GET, POST, PUT and DELETE for working with the required components.</li>

### Features of Web API
<li>Efficiency
<li>Wider reach
<li>Customizable
<li>Personalization
<li>Data ownership
<li>Easy integration with GUI
<li>Time effective
<li>Language-independent
<li>Features of Web Services
    
Here are some essential features of web services:
<li>Loosely coupled
<li>Synchronous or asynchronous functionality
<li>Ability to support remote procedure calls
<li>Supports document exchange

### Chalenges:
(+) 
<li> Transparnecy
<li> Heterogenerity
<li> Security
<li> Openess
<li> Quality
    
(-)
<li> Scalability
    
## API
API is the acronym for Application Programming Interface. It is a software interface that allows two applications to interact with each other without any user intervention.
APIs provides product or service to communicate with other products and services without having to know how they're implemented.

## differences between Web services and API.

|Web Service|	API|
|--|--|
|All web services are APIs.| All APIs are not web services.|
|It supports XML.|Responses are formatted using Web API's MediaTypeFormatter into XML, JSON, or any other given format.|
|You need a SOAP protocol to send or receive and data over the network. Therefore it does not have light-weight architecture.|API has a light-weight architecture.|
|It can be used by any client who understands XML.|It can be used by a client who understands JSON or XML.|
|Web service uses three styles: REST, SOAP, and XML-RPC for communication.|API can be used for any style of communication.|
|It provides supports only for the HTTP protocol.|It provides support for the HTTP/s protocol: URL Request/Response Headers, etc.|

### Advantages of API Services
Here are pros/benefits of using API:
<li>API supports traditional CRUD (Create Read Update Delete) actions as it works with HTTP verbs GET, PUT, POST, and DELETE.
<li>API helps you to expose service data to the browser
<li>It is based on HTTP, which is easy to define, expose in REST-full way.

### Advantages of Web Services
<li>Offers faster communications within and across organizations
<li>Each service exists independently of other services.
<li>Interoperability has the highest priority.
<li>Using Web services, your application helps you to publish its message or function to the rest of the world.
<li>Web services help solve interoperability issues by giving different applications a way to link their data.
<li>Web services help you to exchange data between different applications and different platforms.
<li>It allows applications to communicate, exchange data, and shared services among themselves.
<li>Web services are specifically designed to be used as a web page request and help you to receive data.
<li>It serves as building blocks which makes it easy to reuse web service components in other services. Web Services are deployed on internet standards such as standard Apache, and Axis2. It provides WSDL, HTTP, driven services.

### Disadvantages of API
<li>Creating API is a very time-consuming process
<li>A fixed scale is necessary
<li>Imprecise boundary delineation
<li>To create API, programming knowledge is necessary
<li>Maintenance cost is very high
<li>It can crash when testing API


### Disadvantages of Web Services
<li>It does not access from browser
<li>Not leverage emerging Web developments (Semantic Web, AJAX XMLHttpRequest, etc.)
<li>Some web services are simple to use, but there are some flaws of using it.
<li>Any time one creates a service to handle a variety of customers, there is a demand for specialized machine requirements.
<li>The HTTP protocol is not reliable, so it does not offer any guarantee of delivery of the response.

## KEY DIFFERENCE
<li>Web service is a collection of open source protocols and standards used for exchanging data between systems or applications whereas <li>API is a software interface that allows two applications to interact with each other without any user involvement.
<li>Web service is used for REST, SOAP and XML-RPC for communication while API is used for any style of communication.
<li>Web service supports only HTTP protocol whereas API supports HTTP/HTTPS protocol.
<li>Web service supports XML while API supports XML and JSON.
<li>All Web services are APIs but all APIs are not web services.
    
# SOAP vs REST
SOAP (Simple Object Access Protocol) and REST (Representational State Transfer) are both web service communication protocols. 
SOAP was long the standard approach to web service interfaces, although it’s been dominated by REST in recent years, with REST now representing more than 70% of public APIs according to Stormpath.  

## SOAP vs REST
| | SOAP | REST |
|--|--|--|
| |SOAP, on the other hand, exposes components of application logic as services rather than data. Additionally, it operates through different interfaces.|REST operates through a solitary, consistent interface to access named resources. It’s most commonly used when you’re exposing a public API over the Internet.|
| |SOAP performs operations through a more standardized set of messaging patterns.|REST accesses data|
| |SOAP was originally created by Microsoft, and it’s been around a lot longer than REST. This gives it the advantage of being an established, legacy protocol. |But REST has been around for a good time now as well. Plus, it entered the scene as a way to access web services in a much simpler way than possible with SOAP by using HTTP.|
|Privacy |It offers some additional assurances for data privacy and integrity, provides support for identity verification through intermediaries rather than just point-to-point, as provided by SSL (which is supported by both SOAP and REST).| |
|Error handling |SOAP offers built-in retry logic to compensate for failed communications.| REST, on the other hand, doesn’t have a built-in messaging system. If a communication fails, the client has to deal with it by retrying. There’s also no standard set of rules for REST. This means that both parties (the service and the consumer) need to understand both content and context.|
|Data format|SOAP only allows XML.|REST allows a greater variety of data formats|
| | |REST provides superior performance, particularly through caching for information that’s not altered and not dynamic.|
|Bandwidth | |REST is generally faster and uses less bandwidth.|
| |SOAP’s standard HTTP protocol makes it easier for it to operate across firewalls and proxies without modifications to the SOAP protocol itself. But, because it uses the complex XML format, it tends to be slower compared to middleware such as ICE and COBRA.| |
| |In some cases, designing SOAP services can actually be less complex compared to REST. For web services that support complex operations, requiring content and context to be maintained, designing a SOAP service requires less coding in the application layer for transactions, security, trust, and other elements.| It’s also easier to integrate with existing websites with no need to refactor site infrastructure. This enables developers to work faster rather than spend time rewriting a site from scratch. Instead, they can simply add additional functionality.|
| |SOAP is highly extensible through other protocols and technologies. In addition to WS-Security, SOAP supports WS-Addressing, WS-Coordination, WS-ReliableMessaging, and a host of other web services standards, a full list of which you can find on W3C.| |
|Use Case|<li>Use cases require greater transactional reliability than what can be achieved with HTTP (which limits REST in this capacity) such as ACID-compliant transactions, SOAP is the way to go.</li>|<li>It is the protocol used most often for major services such as Yahoo, Ebay, Amazon, and even Google.</li> <li> support for browser clients (JSON (which typically works better with data and offers faster parsing))</li> |

