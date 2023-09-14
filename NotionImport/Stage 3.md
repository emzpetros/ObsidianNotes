Make sure build has enough instructions for playtesting

  

Attendence:

5 all here

Missing chibidum

  

Citations in slides

  

Team 5

Waiting on power ups , attacks , dash

Player should die when leaving ring

Cute menu animation

Voxel art

Didn't want to end up with asset soup

Picks random location on grid

Feedback on border

Beat boss for progression: could speed up, shrink

  

Feedback from Class

- Speed up ring movement
- For demoing, consider making a special build that has a preset ring path

  

Build Comments

- Attack bug still present, melee worked briefly then stopped for some reason
- Adding a sound effect for the melee could be nice, some kind of whoosh effect
- This may not look as good as it sounds, but the player sprite could flash when hit? Might sell the impact of the knockback a bit more
- Faster ring speed is a big gameplay improvement
- Sprites facing the camera also improves the visuals a ton

  

Team 6

New storyline

Wake up in room and escape

Pay attention to items

Multiple endings

- Wake up in small room, NPCs are ghost

Sounds and footsteps

Keypad minigame!

Next week: storyline and level design improvement

- Add gravity so item actually drops, improve icons

UI scaling

Nice animations on door opening

Inventory system is nice

3d environment looks nice

  

How to know what items are clickable

How to know what the goal is

  

Some kind of intro material: intro blurb

  

Camera clipping

Noise feedback for keypad +

  

Can they retrigger the same dialog - yes

  

Feedback from Class

- UI scaling needs to be fixed
- Could be hard to know which items in the world are interactable
- Inventory system and 3D environment look great
- Having some feedback for the keypad when you input the correct code would help
    - Also making the keypad visible on the door

Build Feedback

- Bug where pressing F duplicates what is in my inventory
- Some issues in the starting room where the camera clips through the walls
- Icon for crowbar and hammer are the same which is a bit confusing
- Animations on the opening cabinets look excellent
- Overall 3D environment is well done
- If time permits, having more interactable objects would be nice. Letting the player open up multiple drawers and cabinets for example

  

Team 1

BGM original

Enemy upside down is a hit goofy: robot, only flip if the spotlight is on one side of it

Come is more gradual

Different enemy behaviors

Audio cue before switch

UI slightly lopsided

Item count vs score

  

Feedback from Class

- Flip the enemy sprite based on if the vision cone is on one one side or the other
- Consider adding an audio cue or other alert before switching players
- UI could be more balanced
- Consider changing “score” to “item count”

Build Feedback

- I would increase the time each player has control, currently I find myself just running back and forth from the same room without time to explore the rest of the map
- Consider refining some of the colliders on the furniture in the rooms. I would get stuck on parts of the scenery more than I expected

  

Team 2

All here

Death screen

Loading screen

10 to L2

Max energy changes

Really really fast

Piskel

UI a bit hard to read

  

Slow down power up???

  

Can we the obstacles pop in and spawn in:

- Exclamation point
- More dead space

Unlimited energy power up

  

Feedback from Class

- Change text UI to be easier to read
- Slow down time power up could be cool
- Make it so the obstacles don’t pop in on screen
- Consider adding more warning of incoming obstacles or more space before they enter the board so the player has time to react
- Add option to pause game w/ ESC key

Build Comments

- Died once instantly after unlocking 2nd level which was sad but I think y’all mentioned this as something you were addressing already
    - Adding a level select would definitely be nice
- Found the later levels much more fun since there was more space before the obstacles reach you, so you had more substantial time to react
- Something to consider: when you’re on zero energy and there’s no flies in range it sucks to die waiting for the recharge time. This of course can just be part of the design and punish poor planning. However, to reduce the changes of this happening you could also implement a slightly shorter recharge time when you are on zero energy. The player would likely not notice the difference but the effect would be that they feel unfairly killed less often
- Overall gameplay was challenging but addicting. Definitely had the “one more try” feeling when I died

  

Team 3

Bullet hell

Will change engine dial

Faster scroll credits

Difficultly on enemy spawns

Good enemy audio cue

  

UI scaling adjustment  
Ends abruptly: ramp up the start too

  

Background on pause menu; opacity

  

Feedback from Class

- Consider adding an opaque box to the pause screen to make it more readble
- UI could be scaled up across the board
- Great adjustment to the steering minigame

  

Question about saving data between scenes: in my experience what has worked for small amounts of data is player prefs, you can also create an obj with a script that you store data in and use [**Object**](https://docs.unity3d.com/ScriptReference/Object.html)**.DontDestroyOnLoad** to maintain it across scenes. Finally, for data persisting between sessions you can write data as a JSON file [https://prasetion.medium.com/saving-data-as-json-in-unity-4419042d1334](https://prasetion.medium.com/saving-data-as-json-in-unity-4419042d1334)

  

Build Comments

- After I killed ~3 enemies no more spawned?
- Steering minigame
    - Lets you fly off screen on the top or bottom and bypass the asteroids
    - What is the motivation to play this game? Unlike the engine which stops the timer what is stopping the player from just ignoring this minigame
- Is there anyway to recover health? Maybe killing enemies sometimes drops health?
- Make sure the timer stopping is very obvious. Once or twice I didn’t notice it had stopped at all
- Mouse disappears after timer runs out and you go back to the difficulty select

  

Team 4

How to play not working

Overlay on background

Other stuff in the house

  

Human to mouse feedback :current task for human

  

Feedback from Class

- Adding feedback about the human’s current focus to let the player know if the mouse is close to being caught
- Making tasks repeatable would make the gameplay more engaging
- Keeping the zoom in to the minigames consistent with the original background would make the transitions smoother

Build Feedback

- Make sure to have a read me or have the how to play screen implemented: it isn’t obvious for example that you need to click to enter the minigames + press ESC to exit
- Sometimes the draggable objects disappear from view during the minigames
- Since the checkbox system is for the entire game it is hard to know when you’ve done all the tasks in each individual game? Maybe highlighting how many are currently available to be checked off when you enter the minigame
- Cannot access the menu again from the game screen
- Music does not play during the game just on the start screen?
- Having sound effects to go with the minigames would add a lot: glass breaking with the TV, water running with the faucet etc.

Some kind of zoom in to the mimigames

Transparent background