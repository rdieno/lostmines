
Offline Game
	Navigate to client/LonelyPlaneteer/x64/Release

	Plug 4 x-box 360 controllers into the computer for a full game. You can
	Plug in 1 controller for testing.

	Launch LonelyPlaneteer.exe

	Using a mouse:
		Click Start Game on the screen
		Click Ready

	Use the directional pad to move your character (Not the analog stick)
	X button is to attack
	B button is to mine a magic well

	Purple wells can be only mined by wizards
	Brown wells can be only mined by knights
	Grey wells are inactive wells

	First team to 1000 points wins

Networked Game

To start the server:
	Navigate to lost-mines/server
	There is a make file that will compile the server code
	
	The commands are as follows:
		make       - Compiles the server application
		make clean - Removes the already compiled executable
		make run   - Runs the executable

	There is already a compiled executable of the server and can be run with the above         commands or "./lostMinesServer"

To start the client
	The networked version of the game requires a keyboard in order to play

	Navigate to "client/LonelyPlaneteer/x64/Release"
	Press "Play"
	
	With the server already running, type in the IP address of the server and click         	"Connect"

	If the client connects, you will see the lobby screen and be waiting for the remaining           clients to connect

	Once the required amount of clients have connected (3), the game will automatically load         into the game map.

	Controls are as follows:
	W     - Move up
	S     - Move down
	A     - Move left
	D     - Move right
	E     - Hold when near a mine to gain points
	Space - Attacks with the given class of the player (fireball/sword swing)

	The game mode has been changed for the networked version. It is not the featured King of 	the Hill game mode but is instead a team deathmatch game mode. Players kill each other 	until one team reaches the required amount of kills (10).

Problems with Networked Version
	Players will not be rendered facing the correct way but the default way when they spawn 	in the game initially.

	The game will not recognize that the game has ended from the client side but the server 	will terminate the UDP reader and writer. This will cause the client to no longer 		receive game updates.
