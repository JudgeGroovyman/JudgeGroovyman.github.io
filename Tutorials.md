# Tutorials #

* [Low Poly Island](#Low-Poly-Island)

# Hitchhikers Guide to the Tutorialsphere #



Unity3D is a great tool but when you are starting out it is overwhelming.  For a beginner it will be easier to pick up than Unreal Engine 4 because the way it does things is a bit more in line with the way the rest of the world does things, but even so it will take time to get used to even a fraction of what Unity3D has to offer.  Fortunately if you are clever about the learning process you don’t have to ‘learn it all’ and by learning the right parts of Unity3D you will be able to make something useful or fun or special.  

To do this following along with tutorials is wise and fun, but honestly there are so many tutorials on the web and on youtube that at first glance its impossible to know where to start.  This page is here to help guide you through the ‘tutorial-sphere’ and help you find the tutorials that are right for you as well as avoid tutorials which have fallen prey to the deadly ‘tutorial-rot’

* I just invented the term ‘tutorial-sphere’!  not bad eh?
* tutorial-rot (aka tut-rot) – the phenomenon that tutorials experience over time when they become so old or unclear that new tut-ees will just find them frustrating.

As a result of all of the above here is a curated reference list of the best and most effective tutorials about Unity3D.


# How To Tutorials #
## Unit Testing ##

[TESTING AGAINST MONOBEHAVIOURS USING MOCKS](https://www.youtube.com/watch?v=r7VkbV0PRC8)
(~30Min)
This is a good video by Unity3D College whose videos are quality because they explain everything that is going on, use discipline in their coding and show you shortcuts and best practices.  In this video he shows use of the NSubstitute dll which once you have defined an interface for a class (which Visual Studio makes pretty easy) you can use to create a replacement instance or ‘mock’ which you can configure how you like.  Its also a good example of running unit tests in Unity and getting around one of the biggest hurdles namely you can’t directly instantiate Monobehaviours (using new) to use in your tests.
(added Dec 4 2018)


## Portal ##
~60min
[Portal](https://www.youtube.com/watch?v=sK9Qf8ElFHo)
This tutorial makes a portal shooter so you can shoot two portals and walk into one and walk out of the other (which comes from the game portal in case you hadn’t heard).  He also shows how to mirror the view from the one portal into the other.  Its a really cool effect to simulate and fun to do the tutorial and it takes less than an hour to follow along.  This tutorial doesn’t talk about rotation and due to the mouse look routines getting that right is non-trivial so I just ignored that.  This does a great job explaining how simple raycasting works.  Note1: he claims in the middle that to get the mirroring effect you will need unity pro but you don’t.  Note2: Near the end of the video he shows the dragging of the texture to the material, but the material pane looks different now so it still works but you just need to drag the texture to a slightly different place in the same pane: Instead of what he did drag the texture to the little box to the left of ‘albedo’.

Added Sep 15 2017

# Game Tutorials #

### Roll A Ball ###
~60min
[Roll-A-Ball Tutorial](https://unity3d.com/learn/tutorials/projects/roll-ball-tutorial)
On the [Unity – Learn](https://unity3d.com/learn) website there are a number of useful tutorials and the first one you will probably encounter in the Tutorials section is the ‘Roll-a-Ball’ tutorial and it is excellent.  It only takes about an hour to go through, is detailed, fresh, and shows you a ton of what you can do with the engine and I have a feeling that the workflow that the author lays out here would be applicable for almost any project.  He shows great tricks and best practices and you end up with a simple deployed game too so I can’t recommend diving into Unity without running through it.  The one thing he doesn’t show how to do is change the screen layout of the Unity3D engine to match his.  That is in Window->Layouts->”2 by 3″.  Update: [This is a text based version](http://www.instructables.com/id/How-to-make-a-simple-game-in-Unity-3D/) of the Roll-A-Ball video tutorial which may be helpful to work with instead of (or in compliment to) the video.
(added Jul 31 2017)

### Space Shooter ###
~8hrs
[Space Shooter Tutorial](http://johnmcgarey.com/2017/08/02/meta-tutorial-of-the-space-shooter-tutorial-using-unity3d-2017-1/)
Also on the Unity-Learn website is the Space Shooter Tutorial.  The link above doesn’t link directly to the space shooter tutorial on the Unity-Learn website however since a lot has changed since that tutorial was made so I have something better: A Meta-Tutorial of the whole Space Shooter Tutorial!  This is a walkthrough of the whole tutorial but done using Unity 2017.1 and it will show you the puzzles that I encountered and how I solved them.
(added Aug 2 2017)

### Runner ###
Unknown Length
[Runner - A minimal Side Scroller](http://catlikecoding.com/unity/tutorials/runner/)

This is quite simply one of the best tutorials I’ve ever seen.  note: I have not walked through this tutorial or done a meta tutorial on it, I found it and am blown away by the quality of the presentation of the whole thing.  Its got text explanations for everything with links for things that are more complicated along with extensive screenshots covering every checkbox and field you need to fill in.  All of the code that you need to change is highlighted as well!  Very impressive.
(added Aug 20 2017)

### Pong ###
[Pong Tutorial](https://www.awesomeincu.com/tutorials/unity-pong/)
This tutorial is unique since it is entirely text based.  There are advantages to both text and video so its always nice to find text based ones.
(added Dec 12 2017)


### Third Person Shooter ###
[A SIMPLE THIRD PERSON SHOOTER](https://roystanross.wordpress.com/beginnertutorialpart1/)
HOW HE TEACHES UNITY TO HIS FRIENDS 
~4HRS
This tutorial series is called Beginner to Hero and teaches all of the basics of Unity to total beginners.  The author has a good sense of humor too [for example](https://roystanross.wordpress.com/beginnertutorialpart13/): “Setting the Editor to Shaded Wireframes makes me feel like the projects I work on are more complex.” in another fun example when he gets something working he just says the word “Baller”.  Between clever quips he does a fantastic job showing all the little steps in a clear and elegant way of how to get a game like this working well.  Some of the code is hard to read ([explanation here](http://youtu.be/wkLpIa_JCw0?hd=1)) but that doesn’t get in the way of the efficacy of the material.
 (added Dec 12 2017)

### Pac Man ###
[Pac-Man NoobTuts tutorial](https://noobtuts.com/unity/2d-pacman-game)
This is a text based tutorial which makes a Pac-Man clone with only 62 lines of code using Unitys 2D features.  It was probably written around 2015 and I'm about to try it to see how bad the tut-rot is on this one.
#### Notes on this Tutorial ####
I like that it has you adjust the colliders manually.  Hint: I found it convenient to hold ctrl which activates Unitys built in snapping tools (at least in modern versions of Unity).  It probably takes 45-60 min to do it by hand, but its good practice and shows what is important when making a game.  Sometimes you have to do things that seem like grunt work like this to make a game that really works.  All sorts of problems happen if positions or colliders are not aligned perfectly, but if they are it works well (so far!).  If you don't align everything perfectly and set all settings perfectly for the sprites and colliders, then the player will sometimes get stuck on walls.  I don't so much enjoy the movement in this game.  
##### Movement Problem #####
When all was said and done I had to do quite a lot of work (several hours plus a lot of thinking) to get movement with the dots working really at all.  It seems to work at first but is entirely fragile.  I changed the raycast to cast out 1.1 times further than it was, and I used a layermask to only get the maze (in the same way that [this documentation](https://docs.unity3d.com/ScriptReference/LayerMask.html) only checks for walls), and I put the keyboard checking in update, and I had to round the position of the player to crisp numbers in code so that rigidbody imprecisions didn't mess up the raycasting. (to crisp the position I rounded 100xposition and then divided that by 100f (on each axis)).  Now the movement seems to work properly.
#### Using Unity 5.0.0f4 ####
I am completely re-doing the tutorial in unity5.  Its nice because all of the boxes and screenshots match the user interface so you can do exactly what it says to do.  Wow the movement works perfectly like its supposed to.  Using the newer unity it really doesn't work, but using this version it works just perfectly.  I suspect it has to do with the changes to the physics collisions behind the scenes, but maybe not since the script seems to mostly override those.
#### Making new levels ####
If you want to make a new level it works best if you follow these guidelines: 
1. Bottom Left sprite import anchor
2. Line up all walls on 8 pixel boundaries
3. 16 pixels between walls (thats the right amount of space for pacman to move)
If you don't line things up right then pacmans movement lines will be offset on top of the wall lines.

Tut-Rot: The settings on the rigidbody have been renamed.  I suspect 'fixed angle' is now 'Constraints/Freeze Rotation'.  
Added Sep 9 2019
Unity 2018.3.4f1
Topics: 2D Sprite Animation, Mecanim, 

### Arkanoid ###
I'm doing [this Arkanoid tutorial from noobtuts](https://noobtuts.com/unity/2d-arkanoid-game)

The blocks arent breaking consistently.  Maybe my speed is too fast?  Nope in the tutorial it says to set the box collider on the blocks to be way 1% the size it should have been (.16x.08 instead of what it should have been: 16x8)

This took me 80 minutes and I did it all while I was watching John Carmacks Oculus Connect 6 keynote.  Its a good tutorial and you end up with a fun simple game when you're done!




# Starting Points #
1. [Unity Learn](https://unity3d.com/learn) website
2. Brackeys 10 min game challenge
3. Noobtuts

# Great Channels #
1. Brackeys channel
2. [Unity3dCollege](https://www.youtube.com/channel/UCX_b3NNQN5bzExm-22-NVVg)


# Blender #

In 2019 Blender received a large and critical update called 2.8 which changed some key things about the user interface.  

## Blender 2.8 ##
* [Make a low poly animal](https://www.youtube.com/watch?v=6mT4XFJYq-4) (or anything really) starting with a picture to trace from in just 10 minutes


# Low-Poly-Island #
[Low Poly Island](https://www.youtube.com/watch?v=0lj643VmTsg) 

Following along with the low poly island tutorial.  this will be the first Blender 2.8 tutorial I have ever followed along with.  


## Blender 2.79 ##
(anything before Blender 2.8)

1. How to make [simple 3d Low Poly Tree model](https://www.youtube.com/watch?v=GsPDxcub3-4) (5min)
2. (My Video) [Basic Blender Operations](https://www.youtube.com/watch?v=P_npoIprUcA): Curves and Macbook pro trackpad
3. (My Video) [Low Poly Mesh from pixel art in Blender] (https://www.youtube.com/watch?v=kBVVXhdAQ5A)


# Shaders #

As of 9/27/2019 my understanding of shader programming is somewhere between the first half of [this video about shaders for noobs](https://www.youtube.com/watch?v=JfC_ye23MvY) (which I understand pretty well) and [this video about truchet tiling](https://www.youtube.com/watch?v=2R7h76GoIJM&t=1160s) (which every step was almost entirely over my head)



