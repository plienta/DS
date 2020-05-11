# Cluster vs Cloud vs Grid

## Cluster
A cluster is usually a concept of several servers that work together, usually dividing the load between them so that from the outside 
the can be regarded as a single system. Simply, cluster is a very general pattern for dividing workload and providing redundancy to 
prevent failure.

## Grid
A grid often refers to a set of servers that work together on a given massive computation. Instead of just distributing the workload 
coming from many customers, they divide a single job into sub parts, providing the job the total resources that are available (or at 
least a dedicated set of servers which is a subset of the grid).

## Cloud
A cloud is a unique form of a cluster. The main goal of the cloud is the effective use of resources. The resources are allocated on demand 
and later released to the pool for serving other needs. The cloud is virtualized, in the sense that the workload is not aware about the 
actual physical location and resources processing it. Also the user is not enabled to directly access these physical resources but rather 
is allotted access to the logical servers it consumes. The cloud is also built for self-service. This means the user gets resources and 
defines networking between the resources using APIs or UI without admin intervention. Finally, a cloud architecture allows workloads to 
scale up and to scale out by requesting more resources when needed.

## 

|Cluster         |Grid                           |Cloud                         |
|----------------|-------------------------------|-----------------------------|
|Stand alone	 | |             |
|           | | |
|           | | |

# Centralized vs Distributed

## Distribted

```mermaid
graph LR
A[CPU1 memory disk] --> B[CPU2 memory disk]
C[CPU3 memory disk] --> A
B --> C
```

## Centralized

```mermaid
graph LR
A[processing, resources, computing] --> D(( ))
A --> B(( ))
A --> C(( ))
```

# Client-Server vs Peer to peer

## Disadvantages & Anvantages

|     |Cient-Server  |peer to peer |
|----------------|-------------------------------|-----------------------------|
|Pros |<li> Can intensionaly scale up (extend the server). <li>Security is more advanced than a peer-to-peer network, you can have passwords to own individual profiles so that nobody can access anything when they want. <li>All the data is stored onto the servers which generally have far greater security controls than most clients. server can control the access and resources better to guarantee that only those clients with the appropriate permissions may access and change data. <li>Easy for maintainance (eg: backup) management.<li> More popular (>70%), no only becuz it is more easy to manage, but also becuz of business|<li>Easy and simple to set up only requiring a hub or a switch to connect all computers together, no need server <li>Connectivity: You can access any file on the computer as-long as it is set to a shared folder. <li>If one computer fails to work all the other computers connected to it still continue to work.<li>Faster.|
|Cons |<li>More expensive than a peer-to-peer network you have to pay for the start up cost. <li>When the server goes down or crashes all the computers connected to it become unavailable to use  (single point of failure). <li>When you expend the server it starts to slow down due to the Bit rate per second. <li>When everyone tries to do the same thing it takes a little while for the server to do certain tasks.<li>By itself is not scalable as peer to peer.<li>Availability|<li>Security is not good other than setting passwords for files that you don't want people to access. <li>Different communication of peer.<li>Higher cost of maintainance|
  
  
|BASIS FOR COMPARISON |CLIENT-SERVER |PEER-TO-PEER|
|----------------|-------------------------------|-----------------------------|
|Basic	|There is a specific server and specific clients connected to the server.|Clients and server are not distinguished; each node act as client and server.|
|Service	|The client request for service and server respond with the service.	|Each node can request for services and can also provide the services.|
|Focus	|Sharing the information.	|Connectivity.|
|Data	|The data is stored in a centralized server. |Each peer has its own data.|
|Server	|When several clients request for the services simultaneously, a server can get bottlenecked.	|As the services are provided by several servers distributed in the peer-to-peer system, a server in not bottlenecked.|
|Expense	|The client-server are expensive to implement.	|Peer-to-peer are less expensive to implement.|
|Stability	|Client-Server is more stable and scalable.	|Peer-to Peer suffers if the number of peers increases in the system.|
|Applications |<li>High security. <li>Resources consistency|<li>Communication services.<li>V2V| 


```mermaid
graph LR
A[Client] --> B[Server]
B --60ms--> A
```
Bottleneck
```mermaid
graph LR
A[Client] --> B[Server]
B --2mins--> A
```
## Fog computing[https://www.cisco.com/c/dam/en_us/solutions/trends/iot/docs/computing-overview.pdf]
The fog nodes closest to the network edge ingest the data from IoT devices. Then—and this is crucial—the fog IoT application directs different types of data to the optimal place for analysis.

Hybrid
