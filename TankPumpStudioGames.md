# Alignment City 1987 #
(preceded by 1986 and 1985)
I'm proud of how fun these games ended up (so far) especially how fun it is just to flap the dragons wings.  Theres a lot of potential for fun platforming with this guy.  As of Sunday June 7 2020 I feel like there are lots of ways to make levels the biggest difference being between the level in 1986 and the levels in 1987, and even within the 1987 levels there is some significant variety.  The 86 game had only one level with 5 layers of depth.  The 87 game has 8 levels most of which have 4 or 5 layers of depth.  Those levels took me about a week of super part time work to make but I'm certainly getting faster at making them.  I can now probably make one layer in 30 min to an hour but then I'm a bit creatively burned and need to go play a VR game or take a nap to refresh.

### Description of Alignment City 1985 ###
Use left and right and jump keys (wasd or arrows plus the spacebar, or a four button gamepad) to touch the tops of buildings (cubes) and proceed to the end of the game as quickly as possible.  Your score is based on the number of buildings you touch and the time it takes you to get to the exit   The more buildings you touch the higher the score and the longer you take the lower your score.  

There are several teleports which may allow you to skip sections of the level (and some that take you backwards).

### Description of Alignment City 1986 and 1987 ###
Welcome to Alignment City where you are a a dragon who can flap its wings and glide around the world and your job is to paint as many buildings as possible by touching them in the shortest time possible.  You will receive three scores: one which is your speed, one which is the exploration score (how may buildings youve found and painted and which naturally rewards your exploration of the world), and finally a technical score which is a mathematic calculation based upon those scores where you could get a high technical score even if you didnt paint as many building as you wanted to.  

Tips:  Going right generally will get you to the end but there are many secrets and reasons to explore the world.   Touch the teleport spheres to teleport further into the world (or back).

Controls:
Use a gamepad or WASD or the arrow keys with shift and spacebar as the jump button.   Press Escape or q to quit.  



# Axehand
Made in Coppercube which is an interesting engine but ultimately not maintainable.  

It did provide some things that other engines dont (AI Characters, built in starting resources, great first party FPS tutorial), but it lacked some key features like any way to copy and paste between scenes at the time I felt like 

The biggest disadvantage is there is no community to speak of to go to for assistance or to see the solutions they have come up with.

I had fun making it and even playing it and have thought about re-creating it in a more maintainable engine.

# Space Shooter

# Survival Shooter


# Game ideas & Projects #

* Serious Sam Shooter with those PBR enemies and fighters
* Hogans Alley and Jungle hunt Shooter with the Tower Defense pack
* Gauntlet Dungeon Crawler with that dungeon pack I'm getting tomorrow and some $20 projectile particle pack and with the cool statues and things that I downloaded
* Alien Breed Dungeon Crawler using the metal Textures from one of the free assets I've got or seen recently or some of the PBR that I have bought before with each level having different color point lights and different statues with point lights and with some objects with only partial metal covering with emissive color textures underneath


* Sprites on Chipped Dominoes
* A pack of low poly blockout shapes with chipped shapes based on the ground shapes in the tower defense pack and the polygon prototyping pack vertex shaded
* Lots of generated low poly terrains by that open source terrain generator I found yesterday 
* Identify the top 10 materials I like best and want to use for my games (plus the meat of course) and 10 more cool normal patterns


## Inspired by Amiga Games ##
* Alien 3 is a great game.  See my review in the amiga section but a game like this with unlimited ammo and lots of exploration in tight corridors even overhead view I think would be a ton of fun.



# Speed Chunk #
The daring escape of Biff Speedchunk

Levels:
0. Title Screen
1.1 1 Shroom
1.2 2 Shroom
1.3 3 Shroom
1.4 4 Shroom
2.1 1 Skelly
2.2 4 Skelly
2.3 1 Shroom & 1 Skelly
2.4 2 Shroom & 2 Skelly
3.1 1 Snake
3.2 4 Snake
3.3 1 Snake & 1 Skelly & 1 Shroom
3.4 2 Snake & 1 Skelly & 1 Shroom
4.1 1 Mage
4.2 4 Mage
4.3 1 Mage & 1 Snake & 1 Skelly & 1 Shroom
4.4 2 Mage & 2 Snake & 2 Skelly & 2 Shroom
End Scene with Escape Animation and Credits and cool ending theme and eventual restart

Build Index:   Password:
1				1sh
2				2sh
3				3sh
4				4sh
5				1sk
6				4sk
7				1sk1sh
8				2sk2sh
9				1sn
10				4sn
11				1sn1sk1sh
12				2sn1sk1sh
13				1ma
14				4ma
15				1ma1sn1sk1sh
16				2ma2sn2sk2sh

The creation of this game was originally inspired by a tutorial on noobtuts.com​​ which while fantastic, did not work with modern versions of unity (but I tried it this week and it works perfectly in Unity 5.0.0f4 which is still available for download) so while I licensed different art and made my own map I couldn't use the code from that tutorial for this game.  The development approach for the core gameplay is identical however.

# Noobtuts Bejeweled #
I punched in the premium noobtuts tutorial [noobtuts-bejeweled](https://noobtuts.com/unity/2d-match-3-game) (aka noobtuts-2d-match-3-game) this is what I came up with.  This was a really good tutorial with some very clever and straightforward ways of solving the problems that make it easy for a newbie to understand.  For example to determine whether two jewels are the same it didn't keep some complicated data structure, it just did a find and searched for the prefab at that location and compared the sprite.  Perhaps for more advanced games there are better ways but this works perfectly and is easy to understand and implement which is exactly what [noobtuts.com](https://noobtuts.com/about) is all about.

# The Monsterous Three #
This is a cute match three game with 3 monster sprites in 2 colors each.  Theres no title screen or scorekeeping but just straightforward match 3 gameplay.

### Gameplay ###
If you haven't played a match-three game like this before you will swap monsters with neighbors to try to get three in a row of one monster.  Four in a row or five in a row also works.  You can't swap monsters unless that swap will result in a match (at least 3 in a row).

I added a blocking feature so it will wait before it destroys each of your matched monsters.  You control the selector using the arrow keys and then press either shift key to go into swap mode.  For example press shift+right to swap the selected monster with the monster on its right (if that is a valid swap).

### Background ###
 Originally based on the the noobtuts bejeweled tutorial I refactored and rewrote the code and some of the solutions I came up with are quite elegant if I do say so myself using some cool C# tricks such as extension methods but ultimately this game uses the same core approach to make it tick.   If you want to see the differences or play the original noobtuts version you can play [my implementation](https://fabdynamic.itch.io/noobtuts-bejeweled) or if you want to learn some Unity game programming then grab the premium noobtuts tutorial [noobtuts-bejeweled](https://noobtuts.com/unity/2d-match-3-game).  [All of their Unity tutorials](https://noobtuts.com/unity) have been fantastic so far.  
 
 I also put in some new CC0 sprites from [Jellybot Enemies](https://opengameart.org/content/jellybot-enemies) by GrafxKid but changed their colors and arranged the colors in such a way that you can easily see the differences between the sprites.   




