## COMP90015 Assignment 1 Multi-threaded Dictionary Server
##### Name: Yuming Shen
##### Student ID: 719088
&nbsp;

### Section 1. Project Needs
---------------------------

+ This project is going to design and implement a multi-threaded server which can deal with concurrent issues with many clients at at time. Socket and Threads are two fundamental techonologies needed to be used in this project. Serveral requirements includes:
	- Architecture
		- A client-Server architecture is required
		- Either one of thread-per-request, thread-per-connection, or worker pool architectures is accepted.
	- Interaction
		- Must use sockets to connect all communication, and within each communicaiton,
		a specific messsage exchange protocol should be used.
	- Failure Handle
		- Errors should be properly handled
+ Basic functional requirements includes:
	1) Search Function
		- This dictionary needs to implements search function, When a user search a word, it should return one or more meaning if this word is in dictionary, otherwise, return a proper information message.

	2) Add Function
		- It should supports adding a new word (with corresponding meaning) to the dictionary. The user may add a word with more than one meaning.

	3) Remove Funciton
		- Removing an existing word (with its meaning) from the dictionary should be implemented
+ User Interface
	- A Graphical User Interface should be provided for user to do operations.


### Section 2. Introduction to the System
------------------------------------------
+ This section is going to introduce this multi-threaded dictionary system

+ 2.1  Architecture
	This dictionary system uses a client-server archiecture, which mainly includes 

+ 2.2 Interaction
	- Socket
	- java object serializable

+ 2.3 GUI & Functionalities 
	- UI for Client
		- Search
			- if the word is in the dictionary, return one or more meaning
			- if the word is not in the dictionary, return a proper message
		- Add
			- if the word is already in the dictionary, return a proper message
			- if the word is not in the dictionary, add it into the dictionary
			- user can add more than one word in the 
		- Remove
			- if the word is in the dictionary, remove it 
			- if the word is not in the dictionary, return a proper message
		- Exit
			- if the user clicks the exit, it will send a message to server and close both socket and GUI
	- UI for Server
+ 2.4 Error handles

### 3. An overall class design and an interaction diagram.
----------------------------------------------------------
+ <img src="https://github.com/Fannibals/S2/blob/master/DS/A1/Pic/UML.png" height = 900, width = 900>


### Section 4. Critical analysis
--------------------------------
+ pros
+ cons

### Section 5. Conclusion
-------------------------


