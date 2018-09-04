## COMP90015 Assignment 1 Multi-threaded Dictionary Server

### Section 1. Functions needed to be implemented

+ 1.1 Search Function
	- This dictionary needs to implements search function, 
	- When user search a word, it will return one or more meaning if this word is in dictionary, otherwise, return proper information message.
	- error handler

+ 1.2 Add Function
	- It should supports adding a new word (with corresponding meaning) to the dictionary
	- The word may include more than one meaning
	- handle errors

+ 1.3 Remove Funciton
	- Removing an existing word (with its meaning) from the dictionary should be implemented
	- handle errors


### Section 2. Introduction to the System

	2.1  Architecture
	client-server archiecture

	2.2 Interaction
		- java object serializable

	2.3 Failure handle

	2.4 Functionalities 
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
		- 
### 3. An overall class design and an interaction diagram.
+ UML <img src = "", height = 600, width = 400>

+ ss

### Section 4. Critical analysis
+ 

### Section 5. Conclusion

