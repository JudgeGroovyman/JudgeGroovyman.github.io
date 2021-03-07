# Blender #

Around early 2019 Blender received a large and critical update called 2.8 which changed some key things about the user interface.  This document will focus on how 2.8 works not how previous version worked (except where mentioned).

# Shortcuts # 

## Navigation Shortcuts ##
* g is grab
	* gx is restrain movement to x (also gy and gz)
* click the hand and drag to move the scene
* Middle drag to rotate scene
* Shift Middle drag to pan scene
* alt middle click to center camera on that point
* alt middle drag to snap turn in that direction
* mouse wheel to zoom in and out

### Walk Navigation ###
This is really cool. If you are used to playing FPS games like doom you can move around the scene in somewhat the same way.  Shift+~ activates this mode and the controls are generally at the bottom but a few key features:
* wheel up to speed up all of your movement in this mode
* e and q to move up and down
* shift for a sprint
* space or middle click to teleport to the pointer spot
* click to stop there


## Shortcuts ##
* no shortcut on a menu item?  right click it.
* z to switch to wireframe and back
* Click and drag tiny corner in top left to split the window
	* right click and join windows to remove one of the windows you just created
	* or click and drag the tiny corner back towards the wall
* k knife tool
* shift a add objects
* a select all
* a a unselect all
* n brings up property tabs
* f to change brush size
* c is circle selection (select all faces around a vertex which spiders into many faces)
* 	right click exits circle selection
* 	alt a clears circle selection

Moving an object to the center
* Shift S -> cursor to world origin
* Object->Set Origin-> Center of Mass
* Select object -> Shift S -> Selection to Cursor



# Things to do #

## Sculpting ##
* Click on sculpting tab at the top to enable the sculpting toolbar.
* Check dyntopo in the top right of that toolbar, change detail to (0.5 for 2.81 and 6 for 2.80) and detailing constant detail
* sculpt button in top right -> symmetry x to turn that off (unless you want it on which could be pretty cool
* An icosphere with subdivision of 3 then has about 160 verts.
* Ctrl digs instead of adds

More details in these videos:
* [Low Poly Island](https://www.youtube.com/watch?v=0lj643VmTsg) 


## Vertex Painting ##

* Make a new material
* Select your mesh
* Go to vertex paint mode (in the object mode menu)
* select a color at the top by the radius slider
* change your brush size with f drag
* go to town with that color
* Add an input attribute node to your material


if you want to paint individual faces

* in vertex paint mode
* hit tab to go to edit mode
* select face select mode



Detailed at about 15:00 in this 
[Low Poly Island](https://www.youtube.com/watch?v=0lj643VmTsg) video.


## Bevel Corners ##
To make any model look kind of worn: Add Bevel modifier.  Width .01m, check only vertices.  Switch width to .03m or .04m for a different more circular and unique look.  Update: this leaves little tiny holes in the mesh.  

Doesnt alwyas work. Sometimes select a face, select similar faces by normal inset faces and drag it in just a bit then tranlate that center face up a bit.  gives at least one rounded edge.  Could do it twice for more roundings.  Also you can use something called 'fatten' and select the outer edges of what you're trying to bevel, fatten them, and then ...

## Sprite to 3D ##
Make it black and white (actually I had better success maxing and minniing brightness and contrast in preview, then saving and reloading and adding green tint) then in inkscape path->trace bitmap and I think single pass autotrace works, then you might have to delete the bitmap and you can tell the diff because when you select one of them it says at the bottom whether it is an image or a path
then import the svg and scale it up in blender by 100 maybe (compare to a reference cube) then on the right in the path tab change resolution down to 2-4 or whatever to make it more low poly, 
then geometry->extrude .01 or so or geometry->bevel depth .0002m or so (To make a tile its probably offset .0001 extrude .004 bevel depth .001)

then select one of hte top faces and select -> similar -> byy normal and then faces->beautify faces
then object -> Convert ot mesh from curve then wireframe and drag select all of the sides then fatten them with 

Triick: When editing path in blender: offset.01 extrude .01 beveldepth .001 makes a cool outline mesh with neat intersections

## Other cool things ##
1. Join a bunch of cubes.  a Mesh/Vertex/Face Menu -> Clean Up -> Merge by Distance
2. for a mesh joined like above to make something kind of get bigger like its going to explode or pop then Face->ExtrudeFacesAlongNormals
3. Shift-D to duplicate
4. Shift-A to add a new primative like a cube or a plane
5. After doing most things type x y or z to lock to that plane only or xz to lock to those two planes
6. After locking to a plane (or not) type 1 or 2 or .5 or whatever to apply that much.  like g to grab and then y 1 to move 1 along the y axis
7. Removing Interior Faces.  First it has to be just one object (join meshes) then wireframe and edit mode tab, then merge by distance in the mesh->cleanup menu and then and 3 for faces mode a to deselect all and then select -> select by trait -> interior faces  
	* HOWEVER thats kind of a lot of setup I know and it still selects interior faces on the outside.  For example if you make a cube with 9 blocks on each side then it will take all the ones out of the inside of the mass of blocks but it will also remove the center face on each of the sides of 9 blocks
	* I'm trying to figure out how to combine many squares into one big one.  
8. Join meshes - in object mode object->join
9. Remove Doubles is now called mesh->cleanup->mergebydistance 
10. Select - Select Linked - Link Flat Faces to select them all on one plane and then f to combine into ngons
11. Press f to make a bunch of flat things into an ngon.  



# Fiji #
Scientific image manipulation

If you want to make a black and white image into greyscale with smooth transitions between black and white:

1. Open it in Fiji (not in binary mode needs to be in 8bit)
2. Image->Scale  2x2 Bilinear interpolation

If you want to make a gradient of pyramids or triangles

1. Open a black and white checkerboard in Fiji
2. Process->Binary->Make Binary
3. Process->Binary->DistanceMap
4. then use the scale above to smooth it out even more

To get outlines of squares in black and white
1. Open a black and white checkerboard in Fiji
2. Process->Binary->Make Binary
3. Process->Binary->Outline


# Best Addons #
1. [Tissue](https://www.youtube.com/watch?v=pVNYyJeLGZI&list=PLJThqQUeIsPTsFMYNoPpqfUQbi8AJh1Ii) (thats a whole playlist) I [heard about tissue here](https://www.youtube.com/watch?v=R5_2pyISN2c&t=240)
2. In the comments to the tissue video above two people say "Tissue, Sverchok, and Animation Nodes are just three of the addons that seriously push Blender into amazing territory. Thanks to  Alessandro and the other devs who extend the functionality of these great tools." and then "Don't forget about Sorcar and modular tree. With those two that's all the node based addons available on blender."


[Straight Skeleton](https://www.blendernation.com/2020/05/23/free-blender-add-on-straight-skeleton/) theres an add on and a builtt in [inset straight skeleton.](https://archive.blender.org/wiki/index.php/Extensions:2.6/Py/Scripts/Modeling/Inset-Polygon/)



# Best Competitors #
https://blogs.dust3d.org

[FreeCAD - your own 3D Parametric Modeler](https://www.freecadweb.org)  and heres a [Playlist about automated modeling in FreeCAD](https://www.youtube.com/watch?v=9EzxiwjKzTQ&list=PLJThqQUeIsPTw-SQeY595Kpz_xQeZxz4o)
