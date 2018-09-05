## COMP90015 Assignment 1 Multi-threaded Dictionary Server
##### Name: Yuming Shen
##### Student ID: 719088
&nbsp;

### Section 1. Project Needs
---------------------------

+ This project is going to design and implement a multi-threaded server which can deal with concurrent issues with many clients at a same time. Socket and Threads are two fundamental techonologies needed to be used in this project. Serveral requirements includes:
	- **Architecture**
		- A client-Server architecture is required
		- Either one of thread-per-request, thread-per-connection, or worker pool architectures is accepted.
	- **Interaction**
		- Must use sockets to connect all communication, and within each communicaiton,
		a specific messsage exchange protocol should be used.
	- **Failure Handling**
		- Errors should be properly handled
+ Basic functional requirements includes:
	1) **Search Function**
		- This dictionary needs to implements search function, When a user search a word, it should return one or more meaning if this word is in dictionary, otherwise, return a proper information message.

	2) **Add Function**
		- It should supports adding a new word (with corresponding meaning) to the dictionary. The user may add a word with more than one meaning.

	3) **Remove Funciton**
		- Removing an existing word (with its meaning) from the dictionary should be implemented
+ User Interface
	- A Graphical User Interface should be provided for user to do operations.

### Section 2. Discription of the components of the system
------------------------------------------
+ The whole multi-threaded dictionary system consists of:
+ **Client Part:**
+ UI for Client
+ <img src="https://github.com/Fannibals/S2/blob/master/DS/A1/Pic/ClientUI.png" height = 400, width = 400>
	- for the Search function
		- if the word is in the dictionary, after the user click search button, the dictionary will return one or more meaning
		
		- if the word is not in the dictionary, it will tell user that it is not in the dictionary.
		
	- Adding a new word
		- if the word is already in the dictionary, it will not let user to edit any more.
		
		- if the word is not in the dictionary, then the user can add the word(more than one meaning is enabled through clicking + button) in the dictionary.
		
	- Removing a word
		- if the word is in the dictionary, remove it
		 
		- if the word is not in the dictionary, return a proper message
		
	- Exit 
		- if the user clicks the exit, it will send a message to server and close both socket and GUI.

+ **Server Part:**

+ <img src="https://github.com/Fannibals/S2/blob/master/DS/A1/Pic/ServerUI.png" height = 400, width = 400>

+ UI for Server 
	- Counting active client numbers
	- Recording all clients' actions
	

+ Error handlings


### Section 3. Overall Class design and interaction diagram
+ 3.1 Class Strucure:
	- **Server Part**
		- Server Class
			- It is the main class of the Server part
		- EachConnection Class
		- ServerStatus Class
		- SGUI Class
		- Message Class
	- **Client Part**
		- Client Class
		- MessageListener Class
		- ClientUI Class 
		- Message Class
	- **Others**
		- dict.txt
		- jackson jars

+ 3.2 Interaction diagram
	- <img src="UML", width="600", height="600">


### 3. An overall class design and an interaction diagram.
----------------------------------------------------------
+ <img src="https://github.com/Fannibals/S2/blob/master/DS/A1/Pic/UML.png" height = 900, width = 900>


### Section 4. Critical analysis
--------------------------------
+ pros
+ cons

### Section 5. Conclusion
-------------------------


