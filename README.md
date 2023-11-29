# Pac-Man Live Project

## Introduction 💭

For two weeks during the C# and Unity Live Project - part of The Tech Academy's Game Developer Bootcamp - I worked together with a group of students to contribute to a legacy project that recreates classic arcade games. I chose to recreate Pac-Man as my project. Over the course of the Live Project I completed User Stories in five areas: <br><br>
  ✔️ Creating Basic Scenes <br>
  ✔️ Level Design & Player Behavior <br>
  ✔️ Adding Opposition Behavior <br>
  ✔️ Completing The Gameplay Model <br>
  ✔️ Adding Particles, Lights, Sounds, Models, Materials <br>

Below is a detailed description of the major features and a general description of other functionality implemented during each Story.

## Creating Basic Scenes  🍃 
For the purposes of this project, the only required scenes were Scene01 (where the game would take place) and a Lose screen. Because Pac-Man is a 2D game with an iconic level layout, all I needed to complete this Story was a sprite of the game board. I did consider adding other levels but did not have the time to do so. The Lose screen UI and functionality would be added later in the development process. The Title screen existed already, my game just needed to be added to the Menu.<br><br>

## Level Design & Player Behavior  🚧 
Rather than placing the Nodes individually in a path around the game board, which would be time consuming and add additional room for error, I created a master Node GameObject, placed box colliders around the level to create the desired path, and wrote two scripts - the Node Spawner script and the Node Deleter script.

***Node Spawner***

![image](https://github.com/megleedev/PacMan-Live-Project/assets/127007134/067d697e-a3b3-40fe-bf3c-ecf5abd9acb4)
  🔹 Sets variables for the cloned Nodes to be spawned <br>
  🔹 Creates a for loop that instantiates clones of the master Node GameObject <br>
  🔹 Once the script was run and the new Nodes spawned, I commented out the script because it wasn't needed anymore <br> 
  🔹 This created a full game board of Nodes, not the traditional path of Nodes that Pac-Man follows <br><br>

***Node Deleter***

![image](https://github.com/megleedev/PacMan-Live-Project/assets/127007134/bbb81b07-689f-4e45-93a4-c9c56a459d5c)
  🔹 Creates a function that determines if a Node is colliding with a placed box collider <br>
  🔹 If so, the Node is deleted <br>
  🔹 The final result is a path of Nodes for Pac-Man to 'eat' <br>
  🔹 This script was also commented out because it was only needed once <br><br>

![PacMan_GameSprites](https://github.com/megleedev/PacMan-Live-Project/assets/127007134/1c9ba85b-ddee-4384-8bff-c96d0705c2d4)<br><br>
To wrap up this story I searched for sprites for the elements of my game and found a sprite sheet used by Google for their web Pac-Man remake. I used the sprites for Pac-Man, Nodes, Ghosts, and score font in my game. Movement, Node eating, and the death animations for Pac-Man were also created using this sprite sheet. A Player Controller script was created to allow the player to control Pac-Man's movement using the WASD keys.<br><br>

## Adding Opposition Behavior ⚡ 
I created AI for the Ghosts by writing a sequence of code that determines the path they can follow and when they pursue the player. First, I used RaycastHit2D to shoot a line from each Node left, right, up, and down so they will be able to find where the Nodes around them are placed. <br>

![image](https://github.com/megleedev/PacMan-Live-Project/assets/127007134/457806b1-b39a-450d-a673-5baa1b0d6c97)
![image](https://github.com/megleedev/PacMan-Live-Project/assets/127007134/10c171c3-a3f2-4d06-babf-483818ca59d5)

Next, I created a function for the AI to determine what direction they can move from the Node they are currently sitting on. Depending on what direction the Nodes are placed around the spot the Ghost is located, the Ghost will decide which direction they can go. <br>

![image](https://github.com/megleedev/PacMan-Live-Project/assets/127007134/ee7fddc0-fd27-4069-af43-7e11ed238e53)

Lastly, the Ghost will begin to pursue the player if it has moved out of the spawn space and into the game space. The Red Ghost begins the game moving out of the spawn space. Pink Ghost and Blue Ghost are on separate timers. <br>

![image](https://github.com/megleedev/PacMan-Live-Project/assets/127007134/f88f2ce9-1a73-4052-9082-2819e5c74b59)
![image](https://github.com/megleedev/PacMan-Live-Project/assets/127007134/b7d41a7b-9a9d-41fc-b66e-bf05d9cb68a4)

***AI In Action***

![](https://github.com/megleedev/PacMan-Live-Project/blob/main/AI_behavior.gif)

This functionality gave me the most trouble by far. I intended to add the Orange Ghost as well but kept having movement issues with it that did not affect the others. I ran out of time to address it so the Orange Ghost was removed from the final product. I suspect that there is a problem with the distance between the Nodes in the spawn area but was in the process of debugging when the Live Project ended. <br>

## Completing The Gameplay Model  🚀 

As more Ghosts are spawned onto the game board and fewer Nodes remain, player movement was made easier by adding teleportation functionality. To accomplish this, I first added special Nodes to the warp areas on the left and right sides of the game board and deleted the Node sprite so they would appear invisible to the player. Then, I wrote code to determine whether Pac-Man was able to warp.<br>

![image](https://github.com/megleedev/PacMan-Live-Project/assets/127007134/fae0def2-526e-4ca2-a90c-4b91bdd5ee17)

Functionality was also added to allow the Ghosts to warp. <br>

***Warping In Action***

![](https://github.com/megleedev/PacMan-Live-Project/blob/main/Teleport.gif)

The score UI element and functionality was added during this User Story. As in the original game, if a player eats a Node, the score goes up. If the player gets caught by a Ghost, the Lose screen appears and the player has the option to restart the game or return to the Main Menu.

![image](https://github.com/megleedev/PacMan-Live-Project/assets/127007134/185bb22f-bbb6-4fff-90ea-00b82f7b5f2f)

## Adding Particles, Lights, Sounds, Models, Materials  🎉 

The final tasks on this project were to add the siren background noise and the sound of the Nodes being eaten. 
