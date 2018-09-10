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
