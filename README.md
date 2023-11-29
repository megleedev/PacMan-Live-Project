# Pac-Man Live Project

For two weeks during the C# and Unity Live Project - part of The Tech Academy's Game Developer Bootcamp - I worked together with a group of students to contribute to a legacy project that recreates classic arcade games. I chose to recreate Pac-Man as my project. Over the course of the Live Project I completed User Stories in five areas: <br><br>
  ✔️ Creating Basic Scenes <br>
  ✔️ Level Design & Player Behavior <br>
  ✔️ Adding Opposition Behavior <br>
  ✔️ Completeing The Gameplay Model <br>
  ✔️ Adding Particles, Lights, Sounds, Models, Materials <br><br>

## Creating Basic Scenes  🍃 


## Level Design & Player Behavior  🚧 
I created the main scene which included the game board the player can move around, the spawn area for the ghosts, and the nodes that can be collected. Rather than placing the nodes individually which would be time consuming and add additional room for error, I created a master Node GameObject, placed box colliders around the level to create a path, and wrote two scripts - the Node Spawner script and the Node Deleter script.

***Node Spawner***

![image](https://github.com/megleedev/PacMan-Live-Project/assets/127007134/067d697e-a3b3-40fe-bf3c-ecf5abd9acb4)
  🔹 Sets variables for the cloned Nodes to be spawned <br>
  🔹 Creates a for loop that instatntiates clones of the master Node GameObject <br>
  🔹 Once the script was run and the new Nodes spawned, I commented out the script because it wasn't needed anymore <br> 
  🔹 This created a full game board of Nodes, not the traditional path of Nodes that Pac-Man follows <br><br>

***Node Deleter***

![image](https://github.com/megleedev/PacMan-Live-Project/assets/127007134/bbb81b07-689f-4e45-93a4-c9c56a459d5c)
  🔹 Creates a function that determines if a Node is colliding with a placed box collider <br>
  🔹 If so, the Node is deleted <br>
  🔹 The final result is a path of Nodes for Pac-Man to 'eat' <br>
  🔹 This script was also commented out because it was only needed once <br><br>

![PacMan_GameSprites](https://github.com/megleedev/PacMan-Live-Project/assets/127007134/1c9ba85b-ddee-4384-8bff-c96d0705c2d4)<br><br>
To wrap up this story I searched for sprites for the Pac-Man characters and found a sprite sheet used by Google for their web remake. I used the Pac-Man, Node, Ghosts, and score font for my game. Movement, Node eating, and death aimations for Pac-Man were also created using this sprite sheet. A Player Controller script was also created to control Pac-Man's movement using the WASD keys.<br><br>

## Adding Opposition Behavior ⚡ 
I created AI for the Ghosts writing a sequence of code that determins the path they can follow and when they persue the player. First, I used RaycastHit2D to shoot a line from each Node left, right, up, and down to determine where the Nodes around them are placed. <br>

![image](https://github.com/megleedev/PacMan-Live-Project/assets/127007134/457806b1-b39a-450d-a673-5baa1b0d6c97)
![image](https://github.com/megleedev/PacMan-Live-Project/assets/127007134/10c171c3-a3f2-4d06-babf-483818ca59d5)

Next, I created a function for the AI to determine what direction they can move from the Node they are currently sitting on. Depending on where the Nodes are placed around the spot the Ghost is located, the Ghost will decide which direction they can go. <br>

![image](https://github.com/megleedev/PacMan-Live-Project/assets/127007134/ee7fddc0-fd27-4069-af43-7e11ed238e53)

Lastly, the Ghost will begin to pursue the player 

![image](https://github.com/megleedev/PacMan-Live-Project/assets/127007134/f88f2ce9-1a73-4052-9082-2819e5c74b59)
![image](https://github.com/megleedev/PacMan-Live-Project/assets/127007134/b7d41a7b-9a9d-41fc-b66e-bf05d9cb68a4)

***AI In Action***

https://im4.ezgif.com/tmp/ezgif-4-481543e596.gif


In your main gameplay scene, using primitive objects add some basic opposition and script their behavior. For example, if you are making Asteroids add some cubes as asteroids and script how they spawn, move, and blow up. If you are making something like Lunar Lander, the opposition could be the ground and how it is shaped. In a case like that, spend this time scripting a ground generator. To complete this story, you should have a nearly complete approximation of how your player interacts with the opposition in your game.

## Completing The Gameplay Model  🚀 
Add any remaining gameplay features. For example, if your game has a score add the UI elements and script the functionality for keeping track of it. If your game changes (ex- more enemies, faster music) as the score increases, add that functionality now. Script what happens when the player loses or wins or wants to play again. Make sure your game properly resets if the player chooses to play again. To complete this story, you should be able to start the Classic Games Arcade from the main menu, navigate to your game, play it, and either play again or go back to the main menu. It's also acceptable if you don't link your game to the Classic Games Arcade main menu. If you can start your main menu screen, play the game, and then restart/go back to your main menu, then that will count as completing this story as well.

## Adding Particles, Lights, Sounds, Models, Materials  🎉 
