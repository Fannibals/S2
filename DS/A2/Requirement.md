## DS Assignment 2

+ **Characteristics**: 
	- 1. create a **20x20 grid** where users on **different PCs**, **min of 2 people**, but allowing more if there are more players, will place letters on tiles of this grid to make words in turns.
	- 2. Users will **take turns** to place **a character** in a tile of the fixed grid mentioned above.
	- 3. When **tiles that touch each-other make a word**, then the person who placed the associated letter will get points equal to the **total length (number of tiles) of the word**.
	- 4. A proper word is judged when all players accept the word through a **visible voting GUI**.
	- 5. The game ends when all users have a turn and cannot find a word/extension to make, basically when **all players say pass when their turn comes through a GUI**.
	- 6. Words are written in English and can only be read from **left to right or top to bottom**. 
	- 7. Appropriate GUI for allowing appropriate controls and information to play as well as to follow it by all players.
	- 8. All users should be able to see **the same view of the game** on their machines without differences or errors between them. **Start and end game should be clear.**
	- 9. Users should be able to **logout from the game any time which would lead to end game as well**.
	- 10. There should be **a game membership pool** where users come in when they login to the game application and see other potential players. 
	- 11. You are welcome to have simplifying assumptions for membership and game start management such as having at most one game at a time and not allowing people to join games at any time but only at the beginning of a game. 
	- 12. You need to let any player initiate a game and **invite others who can then accept this**.
	- 13. You can get creative and implement a more complex game if you agree as a team. 


+ **Chanllenges**
	- **Dealing with concurrency** 
		- Regardless of the technology you use, you will have to ensure that access to shared resources is properly handled and that simultaneous actions lead to a reasonable state. The game logistics leads to some application level order which you need to implement so that the game board is altered by one person at a time for example. There are other cases where you need to do more to solve conflicts.
	- **Structuring your application and handling the system state** 
		- For example you can have one or more servers that communicate with each other, use a P2P or client server approach.
	- **Dealing with networked communication** 
		- You have to decide when/what messages are sent across the network. 
		- You may have to design an exchange protocol that establishes which messages are sent in which situation and the replies that they should generate. 
		- If you use RMI, then you have to design your remote interface(s) and servants for example.
	- **Implementing the GUI.** 
		- You can use any Java library for this implementation but no outside packages that implements the core features of the Distributed Application or the Game Interface.


+ **Future Requirements**
	- Users must provide a username when joining the game. There should be a way of uniquely identifying users, either by enforcing unique usernames or automatically generating a unique identifier and associating it with each username. 
	- All the users should see the same image of the game and should have the same player capabilities and no difference between player capabilities.
	- When displaying a board, the user interface should show the usernames of other users who are currently in the system and their scores etc. You cannot assume implicit knowledge of other players or that they are sitting next to you.
	- Users may connect and disconnect at any time and the game should not crash but stop gracefully such as announce a winner of the game at that state.
	- Users should be able to play and view the game state in real time, without delays. A change on one player should be visible on others immediately from a user point of view.

	- There is no need to authenticate users that want to access the system accept a simple system login page to get names etc and then listing online members at that time.

	- Important: you are NOT allowed to use ANY code taken from an existing shared game implementation.

+ **Simplification**
	- In real life boot strapping such a game would need elaborate mechanisms such as finding other users and downloading the application etc.

	- In our setup, you are welcome to explicitly enter IP addresses, port info etc in a simple game control interface to declare the location of others in the game. Thus we do not ask you to implement a web service or a P2P mechanism to locate others over the internet.

	- More elaborate schemes on this front are acceptable and encouraged.
