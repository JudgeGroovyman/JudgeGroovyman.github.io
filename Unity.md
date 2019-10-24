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



# Skills #
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

# Rename Script #
This is a very tricky business.  I just had success with the following but don't do this without a full backup and a way to figure out if it all worked.  You might want to list what objects use the script so you can check them afterwards.

1. In Unity project view in assets folder right click on the script and go to rename and rename it. 
2. Wait for things to resolve (~5sec?) but at this point your script components on your objects will seem to be broken. 
3. Open the script in Visual Studio
4. In the script in Visual Studio change the name of the class.

I haven't tested it with a 'refactor' style rename since this class was small and not referred to.   Update: That refactor rename did work in a small case

# Quirks #
* Custom Editors work great with some quirks: 1. you have to set dirty if you change something in the editor.  Sometimes.  If you don't you may get unexpected results.  2. Sometimes you have to put ExecuteInEditMode and sometimes you don't.  3.  I feel like a custom button that just calls a function should be a one liner header embedded in the code, but the boilerplate isnt too bad for making a custom editor.  it only takes 2 minutes for a simple one.
* Broadcast message works but if you run it in edit mode and send a message to a class that isn't set to ExecuteInEditMode you get an error reported but generally everything actually still works!?!  You won't be able to set the receiver's information as dirty though.  In my case it worked even with the error and still saved the received data since the receiver was brand new in the heirarchy and new = dirty.