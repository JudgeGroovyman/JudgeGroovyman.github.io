# Unity #

# Competitors #
* Love
* Godot
* Unreal (of course)
* Construct
* Game Maker Studio - Community: toxic.  I even tried to argue in favor of it 'it cant be that bad' and I was assured that it was.  I own one version of this in humblebundle.
* Amazons
* RPG Maker - I own VX Ace and XP and a bunch of tile packs in humble bundle.

## More Obscure Competitors ##
* [JLud2D](https://github.com/rafael-esper/JLud2D) this looks like a great tiled compatible way to make Sega Master System and Genesis style games.  Updated May 2018
* Defold
* [Superpowers](http://superpowers-html5.com/index.en.html)
* Clickteam Fusion - I own multimedia fusion 2 in humble bundle (Windows only for running, pay to export to mac)
* Phaser.io
* Pygame and its competitor for python ... (forgot name)
* Raylib - C/C++ Code with no external dependencies.
* Arcade is a python library for 2d arcade games - open source updated 4 days ago.
* [Piston](https://www.piston.rs/) - A modular game engine written in rust updated 1month ago. 

## More specific competitors ##
* OpenBOR [OpenBOR Community](http://www.chronocrash.com/forum/) for making double dragon games and shooters and more.  Active development.  
* Frogatto has a [built in level editor](https://frogatto.com/developer-info/) for making platform games
* [Solarus](https://www.solarus-games.org/) Lightweight foss Action RPG engine.  Written in C++ games in LUA specifically for 16bit action rpgs like Zelda.  Updates in last weeks.
* [Lionheart](https://www.b3dgs.com/v7/page.php?lang=en&section=lionengine) an engine dedicated to games like Lionheart or other Amiga style 2d games.  
* Mario
	* [The Secret Chronicles of Dr.M](https://secretchronicles.org/en/) a mario clone but with completely original IP and a built in level editor and a scripting language.
	* [SuperTux](https://www.supertux.org/) updated 1hr ago
	* [Mario-Game](https://github.com/jazzyjester/Mario-Game) plus level editor
* [Rockbot](https://github.com/protoman/rockbot) megaman engine which is pretty flexible. 
* [Dust Racing](http://juzzlin.github.io/DustRacing2D/index.html) Micro Machines or Super cars game engine with qt based level editor for new tracks.  
* Minecraft all three updated recently
	* [MineTest](https://www.minetest.net/) an open source voxel game engine.  Make your own game or play one of their many games.
	* [Terasology](https://terasology.org/) Minecraft clone voxel game open source.
	* [Veloren](https://veloren.net/) 
	* [Hematite](https://github.com/PistonDevelopers/hematite) written in rust with the piston game engine.
* [Xonotic](https://xonotic.org/) a 3d game engine primarily for multiplayer gaming
* [Portal](https://glportal.de/) Free portal clone recently updated
* [Nightdive Kex](https://www.nightdivestudios.com/kex/) For early 90s FPS games this is custom made for those games.  Apparently been around for a while even though I haven't heard of it before today (12/3/2019) System Shock, Blood:Fresh Supply, Turok, Turok 2 all made in this.  XboxOne, Switch, Windows, Mac, Linux, PS4 platform support.  "Great for creating simple/retro themed games without the constraint over bloated engine features"  Unfortunately I can't figure out how to download it or buy it or try it at all.  
* [Cube Sauerbraten](http://cubeengine.com/wiki/Main_Page) This FPS game engine lets you edit maps from inside the game.  You can make  your own maps and mods, but I dont know if you can sell them, but you certainly can't sell this engine as a standalone game without replacing all of the textures maps and sounds from scratch yourself.  YOu can even do cooperative in game editing.  

## Investigate ##
* Skyline (drag and drop)
* 001 Game Creator (PC only, templates available)
* Cry Engine
* PlayCanvas (Unity’s lightweight younger sibling)
* GameGuru (The FPS Template master - easiest for 3D, Windows only - made by appgamekit creators))
* Stencyl (has templates (kits), and good for simple games, subscription based?) 
* AppGameKit (expensive-ish ($20-80 + asset bundles), very fast compilation cross platform)
* GameSalad ($12-25/month subscription)
* Buildbox ($2-300/yr sub, with the templates this is probably the fastest of all to make a simple commercial game)
* Urho3D - free lightweight, cross platform 2d, 3d C++ MIT License.  
* Duality2d - Promising Open source, clean understandable code in .net, life editing, introduce game logic via plugins, hot reload resources & plugins, updated recently.


# Want #
The same kind of resources Coppercube gives you out of the box in Unity + Some unreal features.
* AI Enemies (patrol, chase, attack in a radius) models and code so you can drag and drop them into a scene which shoot projectiles and Ragdoll when killed
* 

# Starting Point #
1. Title Screen
2. Scoring
3. Game Over Screen
4. High Score Screen (optional) (could be part of title screen)
5. Rotator
6. InGameText fields
7. Quick Level Loader

## Starting Point Assets ##



# Improvements to QOL #
* [TODO Manager](https://assetstore.unity.com/packages/tools/utilities/todo-manager-142600 - $0 Searches your project for TODOs in the folders you want and with the formats you want also tells you whether its assigned or not (based on whether you put a username in the todo) and I like how it does all of this with a profile scriptable object so you can just copy that SO to other projects to use the exact same settings or copy someone elses settings effortlessly.  You just launch the window from the window menu. The ignore folders feature works well.  You can select todos by assignment.  It also seems to work just fine from the plugins folder (so its not tied to cluttering up the top level of the assets folder like some assets are) Only one thing makes me not wholly recommend this: When you click on the todo it doesn't open the file or even select it to be opened.  I fully assumed it would open the file right to the TODO line in visual studio (or whatever editor you are using) but it doesn't at least in Unity 2019.2.8f1.  At least it will show you the full path if you check an option box so you can find the file in just a few steps.   Its got great PDF documentation actually with clear screenshots and descriptions of everything.  Its also fast at scanning your files and it only weighs about 56KB.
* Scene Heirarchies
* History Selection - [$20 History & Favorites Ultimate](https://assetstore.unity.com/packages/tools/utilities/history-favorites-ultimate-126302) or 
	* [$6 History Inspector](https://assetstore.unity.com/packages/tools/utilities/history-inspector-44279) which looks like it works with prefabs or 
	* [$0 Simple Selection History Lite](https://assetstore.unity.com/packages/tools/utilities/simple-selection-history-lite-130881) which I got and its pretty good and does what it advertises (I left a positive review for this one its just so simple and good) or 
	* [$0 History and Working Set Window](https://assetstore.unity.com/packages/tools/utilities/history-and-working-set-window-60202) which lets you drag prefabs in and you can even drag and drop from the window into your public inspector fields.  It was last updated Jul 2018 and it shows because there are a 8 warnings that show up when it is imported in Unity 2019.2.8f1.  Just select it from the window menu and the window pops up.  Its really just a simple favorites window and it works well.  It has a feature that some other similar tools don't have: You can drag from the favorites window into any inspector field which is a really smooth timesaver as opposed to clicking it and then having it be selected and then dragging from there.  you can put folders on there too.  There is one thing to know if you want to move the folder (I like to keep these kinds of things in a plugins folder) then you have to change a line of code.  Easy.  Its got some great shortcuts in its help menu too, you can easily drag and drop to reorder the items in the menu or even move items to the bottom by dragging to the right (which I think is a very clever and useful gesture).  Dragging to the left doesn't seem to work for some reason but is supposed to send to the top.  Middle click removes the item and ctrl+double click opens files in the windows explorer (thats a great shortcut).  All of this in about 30k. 
		* Comments: Drag left doesn't work in 2019.2.8f1.  Shift + click on something like a folder generates a red error but should probably just be silent and do nothing (warning at worst).  Control double click works but only after you ctrl double click twice.   
* Possibly could use [Choose Your Own Inspector](https://assetstore.unity.com/packages/tools/utilities/choose-your-own-inspector-73126) which lets you add components from many different objects to a custom window and there are more
* In Unity Script Editors - This can dramatically speed up workflows.  $40 [Script Inspector 3](https://assetstore.unity.com/packages/tools/visual-scripting/script-inspector-3-3535) then Hidden in this cool [$15 power inspector - Oct 25 2019](https://assetstore.unity.com/packages/tools/utilities/power-inspector-140430) package is an in-unity editor.
* Easily add a button to execute a routine in your script with [$10 Inspector Gadgets](https://assetstore.unity.com/packages/tools/gui/inspector-gadgets-pro-83013) or with the [$0 Button Inspector](https://assetstore.unity.com/packages/tools/utilities/buttoninspector-72858) which I tried and it works great.  You just have to write two lines of code for every button you want so its extremely easy to use.  It isn't trying to be a complicated inspector replacement which means it just does one thing and it does that well: Effortlessly add a button to the inspector that calls one of your public methods.  Previously if you know the code like I do adding a button was a several minute boilerplate editor code job, and theres still a place for using editor scripts to make your own custom inspector when you want to do more interesting things than just call a method, but when all you want to do is call a method then theres nothing simpler than this. Its perfect.  I confirmed that it works perfectly in Unity 2019.2.8f1.  
* Snapping To surfaces while dragging in the center using translate hold shift and control (command on Mac) to snap to the intersection of any collider and for Rotations: hold same combo to rotate the object towards a point on the surface of any collider which is a good way to make objects orient towards one another

# Investigate #
* .CSX files and Roslyn (with https://assetstore.unity.com/packages/tools/visual-scripting/ucodeeditor-117349)
* Scriptcs.net
* Building C# from within visual studio for instant running of unit tests
* [Unity Runtime Inspector](https://github.com/yasirkula/UnityRuntimeInspector) - This seems really cool allowing you to change a bunch of values from within the game world.  This seems like it could be almost universally useful. [Here is a youtube video](https://www.youtube.com/watch?v=bpy4yAUHNps) about how to use it.  Here it is on [Unity Asset Store](https://assetstore.unity.com/packages/tools/gui/runtime-inspector-hierarchy-111349?aid=1011lQ8D&cid=1100l6EZxMsF&utm_source=aff)  [Tweakable Member](https://gist.github.com/Danik/85d4a7b6d344e69c7579) does something very similar but you just add that tag to your properties.
* [Giles](https://github.com/Unity-Technologies/giles) lets you adjust settings during runtime but its a level editor also that saves data as JSON



# Skills #
Part of the point of developing your skills is so you can focus on the problem space.  if you're trying to make a pacman game you don't want to have to spend your time trying to solve problems with scene loading or editor scripts or displaying text to the user.  These are things that most or all games have to deal with and problems which have been solved before.  YOu want to be able to make your game out of problems that you can solve without them dragging your attention away from the unique problem you are trying to solve.  You want to make a game mostly out of problems that have been solved already and a little bit out of problems that you have to solve uniquely for this game.  

* Scene heirarchies - Preload your character and camera in one scene and make it dont destroy on load then load the rest of your levels via other destroyable scenes.  Also in other scenes if theres no player then load the main scene.  Also you could load the other scenes super smooth without disrupting gameplay much at all.
* Probuilder
* UI fields that can be easily changed from scripts
* TextMeshPro
* Extra Primatives
* Tween Assets
* UV Free Shaders
* Vertex Shaders
* Motion Shaders (like grass for a lively world (brackeys has a video on a grass shader but I think there is one in the unity standard assets)
* Delegates rather than messages (more work to do on this one)
* Extension Methods
* Editor Scripts (able to make one from nothing in 2 minutes with no mental complexity)


# Level Design #
1. [Surface snapping](https://unitycoder.com/blog/2015/11/18/surface-snapping-in-editor/) Shift command when in center mode and transforming from the center gizmo Snap to any collider
2. [Rotation Pointing](https://unitycoder.com/blog/2015/11/18/surface-snapping-in-editor/) point an object at any point on any other collider by using the rotate tool in pivot mode and then starting to rotate any axis or all 3 and press shift cmd.
3. [MAST - Modular Asset Staging Tool](https://assetstore.unity.com/packages/tools/level-design/mast-modular-asset-staging-tool-154939) Free - for the objects setup with their components, this lets you: see the available objects, easily select them, easily put them in the scene, and snap to a grid, super easy rotation, raise and lower the grid and a robust randomizer for varying props.
4. [Level Building Tools](https://assetstore.unity.com/packages/tools/utilities/level-building-tools-93315) $8 lets you randomize position, rotation, scale, stack objects, clone objects to the mouse, snap to surfaces like terrains.  Select a few prefabs and then click and it will select them randomly and align them to the surface normal to create variation.  
5. [Smart Snap Buttons for Inspector](https://assetstore.unity.com/packages/templates/systems/smart-snap-buttons-for-inspector-106586) Free - for any given selected object enable surface snapping, snap axes, it looks really good.  
6. Use [Game Builder](https://store.steampowered.com/app/929860/Game_Builder/) engine


# How to Rename a Script #
This is a very tricky business.  I just had success with the following but don't do this without a full backup and a way to figure out if it all worked.  You might want to list what objects use the script so you can check them afterwards.

1. In Unity project view in assets folder right click on the script and go to rename and rename it. 
2. Wait for things to resolve (~5sec?) but at this point your script components on your objects will seem to be broken. 
3. Open the script in Visual Studio
4. In the script in Visual Studio change the name of the class.

I haven't tested it with a 'refactor' style rename since this class was small and not referred to.   Update: That refactor rename did work in a small case

# Cinemachine #
## Camera Confiner ##
1. Add the extension at the bottom of the cinemachine virtual camera (working example in Akashenen 2d character controller)
2. Setup a kinematic 2d rigidbody on an empty game object (call it camera confiner) with a composite collider 2d with polygons geometry type, then add colliders (polygon, box, whatever) to make the shape you want.  
3. Attach the 'camera confiner' gameobject to the bounding shape 2d in the confiner script on the virtual camera.  Confine screen edges, and damping 0.

# Quirks #
* Custom Editors work great with some quirks: 
	1. you have to set dirty if you change something in the editor.  Sometimes.  If you don't you may get unexpected results.  
	2. Sometimes you have to put ExecuteInEditMode and sometimes you don't.  
	3.  I feel like a custom button that just calls a function should be a one liner header embedded in the code, but the boilerplate isnt too bad for making a custom editor.  it only takes 2 minutes for a simple one.
* Broadcast message works but if you run it in edit mode and send a message to a class that isn't set to ExecuteInEditMode you get an error reported but generally everything actually still works!?!  You won't be able to set the receiver's information as dirty though.  In my case it worked even with the error and still saved the received data since the receiver was brand new in the heirarchy and new = dirty.
* Renaming a script shouldn't be rocket science - I saw one reply suggesting "In a perfect world you will name your scripts correctly to begin with" which is the lamest cop-out in history and completely ignores reality, and shits on the process of refactoring.
* There is no good reason that you have to get a script involved to make an animator flip a sprite.  Its so common that virtually every 2d dev does this daily and has to write code to do it.  There should be a feature built into the animator that flips the sprite based on a boolean.  There are two that seem related: 1. flipx in the renderer (which you can't access from the animator without a script) and mirror in the animation state (which doesnt flip the sprite).  Otherwise you can just effectively double your frames of animation that you have to create (wont take long) and maintain (makes the relevant folders in your asset folder less readable and easily understandable and all sprites harder to find)