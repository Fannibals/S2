## Tutorial 1

### 1. Provide a definition of a Distributed System
  + A system in which hardware or software components located at networked computers  
  communicate and coordinate their actions only by passing message.
    - components: 
  + A collection of independent computers that appears to its users as a single coherent system
    - their own OSs and no shared memory => independent
  + Examples:
    - CDN (Content Delivery Network)
### 2. Briefly explain the difference between a computer network and a distributed system.
  + **A Computer Network** is a collection of spatially separated, interconnected computers that  
  exchange messages based on specific protocols. Computers are addressed by IP addresses.
  
  + **Distributed System** means Multiple computers on the network working together as a system.  
  The spatial separation of computers and communication aspects are hidden from users.
    - run on top of the network
  + DS can be regarded as a part of the network
    - DS provides the service to users, network may not be

### 3. List three reasons for using a distributed system
  + Funcitonal Separation
  + Inherent distribution
  + Reliability: back-up (regular backup) --- what system maintainers, designers care about
  + Availability(uptime): users care
  + Economy(cost effective)
    - resource sharing
  + Scalability
    - vertical scalling : improve performance of each computer, but it has limit
    - horizontal scalling : add new computers
  + Super vs. DS 
    - super computer: all nodes in same OS
    - DS: can be in different OSs
  
  + Amdahi's law
  
### 4. Briefly explain four consequences when using distributed systems.
+ **Concurrency**
  - A can do the his work on A's computer while B can do his work on B's computer  
    and A and B can share resources like web pages or file when necessary.
+ **Heterogeneity**
  - Different hardware, different software, different protocols, different OSs
+ **No global clock**
  - there are limits to the accuracy with which the computers in a network can synchronize their clocks –  
    there is no single global notion of the correct time.
  - This is a direct consequence of the fact that the only communication is by sending messages through a network.
+ **Independent Failures**
  - Each component of the system can fail independently, leaving the others still running. 
  
  
  
### Extra questions
+ what should consider when designing a DS?
  - geography
  - Data segragation
  - SLAs
  - Security
  - Usage tracking
  - Development and configuration management

##
##
## Tutorial 2

### 1. Briefly discuss three aspects of the Socket interface.
endpoint of the interprocess communication
both server and client are processes
socket is the object of server/client

+ server
+ client
+ the port can be used both for sending and receiving
+ there is only one socket response for the port
+ each socket is associated with one protocol (UDP, TCP)

UDP
  - <8kb, 
### 2. Briefly explain three possible failures that can happen when using UDP for communication.
+ **Omission failures**
  - Messages may be dropped occasionally, either because of a **checksum error** or  
  because **no buffer space** is available at the source or destination.
+ Ordering
  - Messages can sometimes be delivered out of sender order.
+ duplicated data
+ data corruption - checksum
### 3. Briefly explain three aspects of TCP that address issues not addressed by UDP.
+ The processes using the connection cannot distinguish between network failure and failure of the process at the other end of the connection.
+ Reliablity 
  - acknowledgement
+ order 
  - sequence number
+ congestion control
+ Message Size
  - no data tranformation limit
 
+ The communicating processes cannot tell whether the messages they have sent recently have been received or not.
### 4. List the steps involved at the client and at the server to establish a TCP stream socket connection.
  
  
+ connnection establishment
  - request
  SYN - 1
  ACK - 1


### Exploring an interactive Client/Server
+ |Client|    Server|
  | ----|-----|
  | 1. create a clientsocket(xp,port) (automatically build the connection)|1. create a server socket|
  | 2. create a scanner object| 2.invoke different sockets for different connections|
  | 3. get inputstream and outputstream from client socket| --|
  | 4. write data to output stream|
  | 5. read inputstream|
  
  
  
+ using buffer(r/w) due to I/O stream is really expensive
+ getlocalport = 4444 , which is server port
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
