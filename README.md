[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/MjLLqDcN)
# HW1
## W1L2 In-Class Activity

Put your notes from the W1L2 (Thurs, Jan 9) in-class activity here.
HW1 activity

Game Objects
UI (Seeds planted text and seeds remaining text)
Does not decrease past 0
Seeds planted does not increase past the original remaining seeds number
Player
Action: 
movement with WASD
put down plant with space
Very cute :D
Plants 
Appears at the position the player is at when space is pressed
Appears on top of player
Cannot place down after number of seeds remaining is 0
Can overlap 
When SPACE: increase planted count and decreases seeds count

Scripts/Classes
Player (actions: movement and planting)
UI update 

Potential improvements:
Restart game
Indication for overlapping plants?
Player animation when moving
End game after all seeds are planted
Add world bounds 

## Devlog
Prompt: Include the HW1 break-down exercise you wrote during the Week 1 - Lecture 2 (Jan 9) in-class activity (above). If you did not attend and perform this activity, review the lecture slides and write your own plan for how you believe HW1 should be built. If your initially proposed plan turned out significantly different than the activity answers given by Prof Reid, you may want to note what was different. Then, write about how the plan you wrote in the break-down connects to the code you wrote. Cite specific class names and method names in the code and GameObjects in your Unity Scene.


Write your Devlog here!

In the class notes, we said player actions include movement with WASD keys and planting with the space key. 
This is done by the update function in player script that updates each frame while the game runs.
There are 4 if statements indicating each key press for movement and 1 if statement that differ a bit because it uses GetKeyDown because it does not require user to hold key down. 
The PlantSeed function is called in the if statement so a seed can be placed when space is pressed
In the function, Instantiate is used to plant a plant when the _numSeedsLeft is greater than 0(as indicated in our notes), number of seed left and seeds planted is updated as one decrease and the other increase, and the UI is updated referring to the UpdateSeeds function in the PlantCountUI script where the number parts of the UI is updated.
I noticed in the game that the plants appear on top of the player so i ordered the layering to match that. 

While coding, I referred to some of my codes, mostly from the blob battle and the final project assignments in 31. 
The only time i got a bit stuck is when i forgot to attatch the event system to the player and the UI wasn't updating but i quickly realized it after seeing the error messages.

## Open-Source Assets
If you added any other outside assets, list them here!
- [Sprout Lands sprite asset pack](https://cupnooble.itch.io/sprout-lands-asset-pack) - character and item sprites
