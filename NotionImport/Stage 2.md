Attendance

Team 1Cibidim

  

Team 4

Placeholder brick assets for now

Sink game: nice turn on sink interaction; snap to counters, turn off facets; breaking everything

Checkmarks show progress on minigame

Human not working yet: queue of tasks to address

Cat and mouse will be animated next week

How many total minigames

Feedback: scoring, minigames,

  

Is the score displayed? Timer? : mouse getting close to exit

MF: consider changing interaction method to be more catlike, make end goal intuitive (path through the rooms)

Class: when can the human see the mouse (alert the player, map maybe)

  

overall really great progress

  

Feedback from Class:

- Consider changing interaction to be more catlike vs mouse clicks
- Consider having an alert of some kind when the human switches their priority to chasing the mouse: can be a minimap if that would be useful or just a sprite alert with a sound effect

TA Comments:

- Great work implementing the minigames, excited to see the final animations in place
- Remember to add sound effects on actions like the faucet and picking up plates
- This might be out of scope but if the player does really well at the minigames (finishes them very fast?) maybe they get a speed boost or similar to reward skilled play

  

  

Team 3

Love the logo

tracking gun and bullets

Health bar decreases

Aim + click to shoot, camera follows reticle a bit, camera shake nice

Engine timer: alert effect

Pick up money

Steering minigame: can navigate around obstacles

Have stuff going towards you

Round timer: what happens now when timer ends

Pick planet you go to

Sound effects!

Pause menu and options is nice touch

  

Bar overheating: gesture

warnings

  

MF: lots of UI in different places

Alerts for when timer is low

Make combat bigger to compensate less tasks

  

Feedback from Class:

- Display engine timer as an overheating bar, allow player to “vent” the engine by holding down a key
- Keep the steering minigame consistent with moving at light speed: maybe change perspective so obstacles move toward you more dynamically
- Make sure to include sufficient alerts so the player knows when a task is reaching a critical point

TA Comments:

- Love the logo and music!
- Great work on implementing features, excited to see the art integration
- The camera effects on the shooting are very nice, adding sound effects would add even more

  

Team 6

Feedback: not using kit, make own music, new story + mechanics

Detective game / escape room: find out murderer via conversations + descriptions of objs

Talk w/ NPCS

Story framework elements in game

Third person camera Detective:

Unlockable interactions

Escape room: different rooms w/ evidence

Level designer

Need to add interactions to objs

Dialogue System:

- dialogue box shows descriptions or NPC speech

  

Character floating

UI scaling

  

Can you choose responses to the NPCS?

Different gestures and emotions

How does the player report the murder

  

Does the murderer change? Can arrest the wrong person, 4 different endings

  

Class: Increasing walk speed

Is there any time pressure?

Red herrings nice

  

Key feature implemented?

Escape room - item combos

  

Puzzle locked linear progression

  

When can you start arresting? Have to carry correct objs to right person

  

The room games: interaction

  

  

Grade harsher but can make up

  

Feedback from Class:

- The escape room aspect does not come through well, either rework the story premise to match the idea of getting out or don’t describe it as an escape room since it sets up people’s expectations
- Think about how to make gameplay more dynamic then just pick up objects and talk to people. In games like The Room [https://www.fireproofgames.com/games/the-room](https://www.fireproofgames.com/games/the-room) even though the main point is puzzles and thinking, the interactions are more in depth
- Make sure to verify UI scales correctly

TA Comments:

- Player currently appears to float a bit above the ground when walking around the environment?
- Like the idea of having fake clues that could lead you in the wrong direction
- Dialogue system implementation is very impressive

  

Team 1

Liam Gongola: enemy work

- Moves from room to room and stays in center

Cute animation

Impressive

UI a bit busy, same style as the rest of the art

Specific items to go towards?

- Warning before swap

Special doors look great

Two 2.5 min rounds

DX: art

Feedback: balance with the tables,

Does player two have to remember where the item came from

What happens when you’re seen ? Score deduction

IC: UI elements, timer

Class:

- Ghost of the item
- Telegraph?

  

Class Feedback:

- Adding the ghost of the item when it is removed would be helpful
- UI blends in a bit with the background: consider changing the color to have it pop more or otherwise distinguish it from the rest of the art

Build Comments

- Art is fantastic!
- Movement feels great, I can see the competitive gameplay being very fun!
- UI did not show up in build (see attached)
- Tables to place items also did not show up
- I was able to go through the secret door and exit the map completely (see attached)
- Not sure if I was playing an older build but make sure to verify everything works when built

  

Team 5

Movement, attacks, beginnings of map, placeholder sprites

- Ring movement: balancing ring movement speed
- How does the player attack back?
    - Mouse click attack

4 x 4 grid of zones: ring goes square by square

**Reflecting projectiles! dash?**

- Can defeat projectile stuff

Camera angle clipping through building

  

**Can you zoom in the view anymore**

Music overly serious

Enemy sprites are cute!

Player character

**theme mechanics**

  

Power ups? Knock back resistance, ppush power

  

Class Feedback:

- A progress bar for the ring could be helpful
- Allowing variable zoom would help gameplay and show off your art better
- If possible integrating the themed areas into mechanics could be interesting: custom projectile effects? Ice cream slows you down?
- Adding a dash to get out of tight spots could be fun

Build Feedback / Player Attack Bug:

- Movement feels good, definitely think a zoom option would help
- It’s a little odd that I can move the player totally out of the camera field of view: maybe think about limiting their movement to within the camera frame
- Got the ray visualzation to work (we needed to be looking at the scene view!) w/ Debug.DrawRay(transform.position, ray.direction, Color.green);
- Seemed that all the rays were coming out in one direction wherever I clicked
- You may have to rotate the plane object you are raycasting from so it points in the same direction as the player to mouse direction

  

  

Dash ???

  

Team 2

Crash + die

logs just moved horizontally for now

SY: grid generation, movement + shooting

LB: art for coins + spawning, flies

CB: movement charges

Raunak: logs

  

Different sized grid

  

**Could the logs speed up?? + more**

empty spots

Fly difficulty

  

Class Feedback

- Consider have the logs speed up / having different sized logs to ramp up difficulty
- I like the idea of putting empty spots on the grid as well in harder levels

Build Comments

- Good balance so far of energy recharge rate + max energy
- First level has a good level of difficulty, will be interesting to see how it plays with logs from multiple sides
- Possible power up idea: temporary invincibility maybe on a cooldown or with a limited number of uses. Could help get out of a tight spot where you can’t wait for the recharge but also don’t have any convenient fly spawns
- I think this was addressed in class but you can definitely spam the fly catching mechanic as is