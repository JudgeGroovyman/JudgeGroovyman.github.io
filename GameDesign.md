
# Learned from Amiga games

Back in the day they thought that making home games should be like making games for the arcade at home.  They thought people would want the exact arcade experience at home.  And they thought that people wanted the games to be hard to give them a challenge.  To some degree they were right about all this but in the name of making games hard and in the name of faithfully bringing arcade games into the home publishers and developers regularly committed some cardinal sins some of which I have identified and will list here:
1. Limited number of credits for the home game.  This one completely baffles me: If you wanted to bring the arcade experience home then absolutely do that.  Let people put in as many virtual quarters as they want.  This ruined so many games back then it blows my mind.  So many people would have had so much more fun if this completely artificial limitation hadn't been introduced.  And the weird part is it wouldn't have stopped hardcore players from beating it in 3 continues (true it would have changed their motivation curve and changed the satisfaction they got from the built in challenge, but that could have been mitigated by adding a simple mode in the options that limited continues to 3!?!) but it just would have given more casual players more fun, would have let them see the whole game (which is a lot of why I always wanted to play games: to see and experience and live in the content and world of fantasy they had created for me) and would have given real value to customers from the games they bought.  As it is in many cases (mine certainly) people bought a game and gave up because they made no real progress for hours while repeatedly having to play the same sections of the game (level 1) over and over.
2. Difficult or impossible to play without taking hits.  The better you do the fewer hits you should take and the player should always know that if he does it very well he doesnt take any hits.  It should be a matter of degree (I took a little damage because I didnt do it perfectly, or I took a lot of damage because I haven't figured out how to avoid damage -  which is often revealed by you getting shot when standing in one place os you know to stand in another) or puzzle solving (how do I avoid all of the shots, what is this enemies attack pattern so I can avoid their shots).
3. Difficulty shouldn't come from having to do a few things perfectly or you die.  Like falling in pits in zelda 2 or castlevania.  its annoying to fall into pits in mario but in mario theres not a life bar so hits kill you (exceptions granted) but in zelda and castlevania most things hurt you a bit but those pits kill you instantly? and the worst part about those is knockback into pits. That should be game-illegal. Same with bad dudes on the train level and golden axe when you have to jump those pits, and double dragon on SMS and NES, except in those games theres not just a simple jump, you have to do a simple attack combo to jump those pits and if you slip up just a bit you die.  That can and has changed a great run into a failed run from just a few little mistakes.  Your mistakes shouldn't have that much gravity (no pit-pun intended) unless its naturally built into the game (like a final boss or something)
4. Difficulty should be in the process of doing hard things the game not in the process of doing hard things for 30 minutes without making too many mistakes.  Checkpoints fix this and checkpoint balance is an art.  Lets try using a trainer and a walkthrough (that came with the WHDLoad) 
5. Tip for level designers.  dont put enemies in places that the player cant shoot them.  Best example: Enemies below you on a downward slope if the player cant shoot down and forward and at exactly the correct angle.  Second best example: enemies that are below the players shot line when he cant duck.  Unless jumping over them is a clear solution and jumping is well done and expected in your game and theres a clear and safe place to land dont put short enemies in front of the player like that.  Metroid is an example which sort of did it right. imho it should have made them hittable from standing position butsince samus cant duck she is encouraged to jump over them or later bomb them and both of those solutions work.  In Cool spot amiga or assassin amiga you are going down a slope and there are blind things beneath you that you cant shoot so as soon as  you see them you jump them only to have them track your position and you land righ ton them or you land on something else which was positioned right after it.  Jumps to avoid damage should be clear and visible or just give the player a little break and only put enemies on upslopes and make the level a bit longer.



Much of this is about the continue structure of the game.  One simple way to do it is separate into shortish levels and let you try that level as many times as you want until you beat it with no passwords or anything.  its tragic to me that so many games could have done something simple like this back then but made the game so hard that half of the people didnt play it.  An important part of the reason that people pirated games in the 80s was to fix their difficulty.


Continue Structures that work and can be fair
1. Save at any moment
2. Save between levels
3. Save between small sets of levels



## Good ideas ##
Character entry like bad dudes where the player sprite is the pointer to the letter.  It worked great and was fun to do!


# Sounds
Sounds create satisfaction.  Each sound should be satisfying and each action should have an associated satisfying sound.  The motion and action of thew world in response to your actions should also be satisfying but thats not about sounds.


# My stories are like this:
3. Hero experiences apparently unrelated bad events
4. Hero wins in the end but only because the bad things  turned out to be blessings in disguise.

# I would like to make games like other games
I would like to show myself that I can do it and I would like to have the fun of having the game to play.

### Pac Man on C64

### Tetris

### Rock N Roll Racing

### Thunderstrike

### Peter's Quest

### Gauntlet / The Chaos Engine

### Doom
With lots of high Jumping and platforming and dodging and raining destruction down from above.
I actually already made this exact game in coppercube.

### A thousand different interesting trippy effects generators

### Hogans Alley

### Smash TV

### RPG

### Beat Saber

### Serious Sam

### Zork

### Hoi

### Wonderboy III: The Dragon's Trap

## Thoughts
### Combinations
Maybe I could combine some of these: Gauntlet (Find keys and food and the exit, enemy generators), Smash TV (control scheme, map based), Thunderstrike (Collecting Treasures from generators, transporting them to safe zones), Rock N Roll Racing (Fast paced rollaball based racing controls over tracks where things changed every lap)

# Elements of Game Design


# Structural elements

### Doom ###
Here are some of the elements that the doom engine and its surrounding ecosystem provides game developers out of the box without having to develop any of these things themselves.  Note: To be clear I mean no disrespect to game developers who make games using the doom engine since they still have to design the maps and layout all of the beasties and powerups and everything and do that for every difficulty level and playtest it all so theres still a lot of involvement and I have huge respect for everyone who does this.  Also there is a non trivial learning curve to get all the different bits and bobs hooked up and settings set in just the right way and to learn how to do all of that hooking up and setting and to learn to use all of the tools.  Its generally easier to learn to use a well designed and mature tool than to develop a tool yourself from scratch but that doesnt mean its trivial (although for some people I bet it is pretty trivial).  I don't have any insight into how well all of those processes are documented but my guess is they are documented very well as of 2019.  Also many game developers add their own textures and things so they are investing their own art into the process too.

* Character controller
	* Movement
	* Aiming
	* Shooting
	* Shot Calculations
	* Health Management
* UI
	* Health display
	* Ammo display
	* Level Complete
	* Game Over
	* Deep detailed options menu 
	* options screens
	* Deep in-game control reconfiguration
	* Screen transition animations
	* Simple Overworld level transition screens
* Continue Structure
	* Load at any moment
	* Save at any moment
	* Intuitive and Instant
* Scoring
	* Timing
	* Par time to beat
	* Statistics
	* Secret count
	* Kill count
* Many Guns
	* Models
	* Sounds
	* Shot Animations
	* Projectile Art
	* Projectile Animation
	* Ammo maintenance
* Weapon switching
	* Inventory
	* Animations
	* Several switching schemes
* Health Pickups
	* Several varieties
* Weapon Pickups
* Player Damage
	* Damage received indications
	* Damage received animations
* Enemy Damage
	* Damage animations
	* Damaged enemy graphics
	* Blood
	* Gibs
	* Remaining blood
* Enemy AI
	* Movement Speed
	* Attack Pattern
	* Actions
	* Pathfinding
* Many enemy types
* Levels
	* Secrets
	* Buttons
	* Switches
	* Doors
	* Colored Keys
	* Multiple wall types
	* Stairs
	* Moving platforms
	* Elevators
	* Walk through wall secrets
	* Hidden buttons
	* Trigger to spawn enemy groups
	* Enemies hidden behind doors
	* Enemies hidden on top of platforms
	* Windows
	* Outdoor areas
	* Multiple skyboxes
	* Darkness and Light
* Automap
	* Really detailed
	* Live while moving around
	* HUD based
	* Minimap in corner (iirc)
* Level Editor
	* Ecosystem
	


### Gauntlet
* Explore Dungeon
* Mazes of blocks
* Puzzles
* Traps
* Secret Walls
* Teleporters
* Locked doors everywhere
* Battle mighty foes (monsters)
* Generate more enemies from generators
* They swarm you
* They are only held back from attacking you by the dungeon blocks
* Enemies die after a number of hits
* Getting shot hurts enemy
* Touching player hurts enemy too
* Enemies hurt player
* by touching him
* and sometimes by shooting him
* Search for exit to move to next level
* Start on level one every game
* Add a quarter to get an extra life
* Search for items
* Keys open locked doors
* Food gives life
* Poison takes life

### Elements I like
* Doom 
* Colored Keys
* Secret doors


### Desert Golf
* Launch ball into hole
* Screen advances when you get ball in hole
* No enemies
* Endless game
* Thousands of screens
* No menu screen

### Mutant Storm
* 100 Linear levels
* Stage select
* Only for unlocked stages
* Have to beat 10 levels to unlock the next stage
* High scores locked in once stage is beat
* Each screen is a level
* Unlimited continues
* Unlimited tries to beat all 10 levels in the stage

### Mutant Storm Reloaded
* Like Mutant Storm
* Difficulty defined by the belt you choose
* Score attack mode
*  

### Super Mario Bros
* 36 Linear Levels
* No stage select


# My Structural Designs

### Game Mode 0
* Like Desert Golf
* Achieve Goal
* Short Ad every 2-4 goals
* One screen at a time
* Scrolling is ok
* Endless game
* Thousands of screens
* No menu screen



# Credits
* Put your name at the bottom and the publisher at the top
* like in Dunk Hoop

