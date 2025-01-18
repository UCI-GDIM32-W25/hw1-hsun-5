[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/MjLLqDcN)
# HW1
## W1L2 In-Class Activity
HW1 activity

Game Objects
- UI (Seeds planted text and seeds remaining text)
  - Does not decrease past 0
  - Seeds planted does not increase past the original remaining seeds number
- Player
  - Action: 
    - movement with WASD
    - put down plant with space
  - Very cute :D
- Plants 
  - Appears at the position the player is at when space is pressed
  - Appears on top of player
  - Cannot place down after number of seeds remaining is 0
  - Can overlap 
  - When SPACE: increase planted count and decreases seeds count

Scripts/Classes
- Player (actions: movement and planting)
- UI update 

Potential improvements:
- Restart game
- Indication for overlapping plants?
- Player animation when moving
- End game after all seeds are planted
- Add world bounds 

## Devlog
In the class notes, we said player actions include movement with WASD keys and planting with the space key. 
This is done by the update function in player script that updates each frame while the game runs.
There are 4 if statements indicating each key press for movement and 1 if statement that differ a bit because it uses GetKeyDown because it does not require user to hold key down. 
The PlantSeed function is called in the if statement (when space is pressed) so a seed can be placed when space is pressed
In the function, Instantiate is used to plant a plant when the _numSeedsLeft is greater than 0(as indicated in our notes), number of seed left and seeds planted is updated as one decrease and the other increase, and the UI is updated referring to the UpdateSeeds function in the PlantCountUI script where the number parts of the UI is updated.
I noticed in the game that the plants appear on top of the player so i ordered the layering to match that. 

While coding, I referred to some of my codes, mostly from the blob battle and the final project assignments in 31. 
Some issues i ran into is when i forgot to attatch the event system to the player and the UI wasn't updating but i quickly realized it after seeing the error messages. I also didn't remember including Quaternion in Instantiate for rotation. As well as not converting int to string in the UpdateSeeds function for updating UI.

## Open-Source Assets
If you added any other outside assets, list them here!
- [Sprout Lands sprite asset pack](https://cupnooble.itch.io/sprout-lands-asset-pack) - character and item sprites

## Prof comments
Thank you for making the connection between your break-down and the code that you wrote clear for this Devlog. :)

Please consider formatting your break-down activities with the hyphen '-' symbol as suggested above. Also, you can remove the prompt text. This will make it a lot easier for me to read. See the [README formatting guide here](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).
