## Lecture 1: Introduction to Distributed Systems and Characterisation

### This subject aims:
+ to cover characteristics of networked computers that  
  impact system designers and implementers
+ to present the main concepts and techniques that have been developed to help  
  in the tasks of designing and implementing systems and applications that are  
  based on networks


### 1. Distributed Systems

#### Definition
+ A system in which hardware or software components located at **networked** computers  
  communicates and coordinate their actions only by **message passing**
+ A distributed system is a collection of independent computers that appear to  
  the users of the 

### 2. Networks vs. Distributed Systems
+ **Networks**: A media for interconnecting local and wide area computers and exchange messages  
&emsp;&emsp;&emsp;&emsp;&emsp; based on protocols. Network entities are visible and they are explicitly addressed
  - Networks focuses on packets, routing, etc.
+ **Distributed System**: existence of multiple autonomous computers is transparent
  - DS relies on services provided by a computer network
  
  
### 3. Reasons for Distributed Systems
+ Functional Separation
  - Existence of computers with different capabilities and purposes
  - Beneficial to separae collection from processing
+ Inherent distribution
  - The process/activity is naturally distributed
  - Information, people
+ Power imbalance and load variation
  - Distribute computational load among different computers.
+ Reliability
  - Long term preservation and data backup (replication) at different locations.
+ Economies
  - Share resources ==> reduce cost, statistical multiplexing


### 4. Consequences of Distributed Systems
+ **Concurrency**
  - A can do the his work on A's computer while B can do his work on B's computer  
    and A and B can share resources like web pages or file when necessary.
+ **Heterogeneity**
  - Different hardware, different software, different protocols
+ **No global clock**
  - there are limits to the accuracy with which the computers in a network can synchronize their clocks –  
    there is no single global notion of the correct time.
  - This is a direct consequence of the fact that the only communication is by sending messages through a network.
+ **Independent Failures**
  - Each component of the system can fail independently, leaving the others still running. 

### 5. Characteristics of DS
+ Parallel activities
  - Autonomous components executing concurrent tasks
+ Communication via message
  - No shared memory
+ Resource sharing
  - printer, database etc.
+ No global state
  - No single process can have knowledge of the current global state of the system
+ No global clock
  - Only limited precision for processes to synchronize their clocks


### 6. Goals of DS
+ Connecting Users and Resources
  - widely available
+ Transparency
  - user only need to know how to use rather than the complexity behind
+ Openness
  - anyone can interface with, understand and extend system
+ Scalability
+ Enhanced Availability

### 7. Diff with Parellel systems
+ Extensibility of clusters leads to heterogeneity
  - Adding additional nodes as requirements grow
+ Extending clusters to include user desktops by harnessing their idle resources
  - E.g., SETI@Home, Folding@Home
+ Leading to the rapid convergence of various concepts of parallel and distributed systems

### 8. Examples
+ Web
+ Data centers an Clouds
+ ...

### 9. 

<img src="https://github.com/Fannibals/S2/blob/master/pic/internet.png" alt="alt text" width="600" height="450">
<img src="https://github.com/Fannibals/S2/blob/master/pic/intranet.png" alt="alt text" width="600" height="450">
<img src="https://github.com/Fannibals/S2/blob/master/pic/mobile.png" alt="alt text" width="600" height="450">
<img src="https://github.com/Fannibals/S2/blob/master/pic/web.png" alt="alt text" width="600" height="450">


### 10. Challenges
+ Heterogeneity
  - Heterogeneous components must be able to interoperate
    - Different OS, hardware, programming languages, etc.
+ Distribution transparency
  - Distribution should be hidden from the user as much as possible
    - Access transparency(OS), Location transparency(DNS), Failure transparency 
    - Replication transparency(DNS), Migration transparency
    - Concurrency, performance, scaling, application level transparencies
+ Fault tolerance
  - Failure of a component (partial failure) should not result in failure of the whole system
+ Scalability
  - System should work efficiently with an increasing number of users
  - System performance should increase with inclusion of additional resources
+ Concurrency
  - Shared access to resources must be possible
    - Provide and manage concurrent access to shared resources
+ Openness
  - Interfaces should be publicly available to ease inclusion of new components
+ Security
  - The system should only be used in the way intended
    - Confidentiality
    - Integrity
    - Availability
    - Non-repudiation
      - through Encryption, Authentication, Authorization
