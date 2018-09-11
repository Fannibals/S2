## Remote Invocation
### 1. Introduction
+ purpose: add one more middleware layer to make programming easier
+ High-level programming models in use
  - Remote Procedure Call
  - Remote Method Invocation

### 2. Request-Reply Protocol
+ based on three abstract operations:
  - **doOperation**
    - ```
      public byte[] doOperation (RemoteRef s, int operationId, byte[] arguments)
      ```
    - Sends a request message to the remote server and returns the reply
    - The arguments specify the remote server, the operation to be invoked and the arguments of that operation

  - **getRequest**
    - ```
      public byte[] getRequest ()
      ```
    - Acquires a client request via the server port

  - **sendReply**
    - ```
      public void sendReply (byte[] reply, InetAddress clientHost, int clientPort) 
      ```
    - Sends the reply message reply to the client at its Internet address and port
+ A typcial message in request-reply protocol:

| Fields | arguments| description|
|-----|------|-----|
| messageType|int   (0=Request, 1= Reply)| |
| requestId| int| requestId + identifier for the sender process(port and Internet address)|
| remoteReference|RemoteRef| |
| operationId | int or Operation| |
| arguments | array of bytes| |

+ for requestId
  - A doOperation in the client generates a requestId for each request message, and the server copies these IDs into the corresponding reply messages. 
  - This enables doOperation to check that a reply message is the result of the current request, not a delayed earlier call.
  
  
  
  
  
+ **Failure Model**
  - If operations are implemented using UDP, then they suffer from the same communication failures:
    - Lost messages
    - Out of order
  - crash failures 
    - failure of processes

+ **Design issues**
  - Fault tolerance measures:

| measures|description|
|-----|------|
| Timeouts| return immediately from doOperation with an indication to the client that the doOperation has failed|
| Discarding duplicate request messages|the protocol is designed to recognize successive messages (from the same client) with the same request identifier and to filter out duplicates.|
| Lost reply messages | strategy depends on whether the server operations are idemponent (add an element to a set is an idempotent operation)|
| History | For servers that require retransmission of replies without re-execution of operations, a history may be used. |

+ Three main design decisions related to implementations of the request/reply protocols are:
  - Strategy to retry request message
  - Mechanism to filter duplicates
  - Strategy for results retransmission


### 3. Styles of exchange protocols
+ Three different types of protocols are typically used that address the design issues to a varying degree:
  - The request (R) protocol
  - The request-reply (RR) protocol
  - The request-reply-acknowledge reply (RRA) protocol

+ RPC exchange protocols

|Name|Message sent by|sent by | sent by|
|---|---|---|---|
| | Client|Server|Client|
| R| Request|||
| RR| Request|Reply||
| RRA| Request|Reply|Acknowledge reply|   

### 4. Invocation Semantics
+ call semantics

|--|Fault tolerance measures|--| Call semantics |
|---|---|---|---|
| Retransmit request message| duplicate filtering|Re-execute procedure or retransmit reply| |
| No| Not applicable|Not applicable |Maybe|
| Yes| No |Re-execute procedure|At-least-once|
| Yes| Yes|Retransmit reply|At-most-once| 
