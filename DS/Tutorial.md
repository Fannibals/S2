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
