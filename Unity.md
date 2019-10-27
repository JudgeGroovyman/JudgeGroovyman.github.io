# Unity #





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
* TODO Manager - $0 Searches your project for TODOs
* Scene Heirarchies



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


# How to Rename a Script #
This is a very tricky business.  I just had success with the following but don't do this without a full backup and a way to figure out if it all worked.  You might want to list what objects use the script so you can check them afterwards.

1. In Unity project view in assets folder right click on the script and go to rename and rename it. 
2. Wait for things to resolve (~5sec?) but at this point your script components on your objects will seem to be broken. 
3. Open the script in Visual Studio
4. In the script in Visual Studio change the name of the class.

I haven't tested it with a 'refactor' style rename since this class was small and not referred to.   Update: That refactor rename did work in a small case

# Quirks #
* Custom Editors work great with some quirks: 1. you have to set dirty if you change something in the editor.  Sometimes.  If you don't you may get unexpected results.  2. Sometimes you have to put ExecuteInEditMode and sometimes you don't.  3.  I feel like a custom button that just calls a function should be a one liner header embedded in the code, but the boilerplate isnt too bad for making a custom editor.  it only takes 2 minutes for a simple one.
* Broadcast message works but if you run it in edit mode and send a message to a class that isn't set to ExecuteInEditMode you get an error reported but generally everything actually still works!?!  You won't be able to set the receiver's information as dirty though.  In my case it worked even with the error and still saved the received data since the receiver was brand new in the heirarchy and new = dirty.