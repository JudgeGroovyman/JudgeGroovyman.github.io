<!--
  _____                    _       _            
 |_   _|__ _ __ ___  _ __ | | __ _| |_ ___  ___ 
   | |/ _ \ '_ ` _ \| '_ \| |/ _` | __/ _ \/ __|
   | |  __/ | | | | | |_) | | (_| | ||  __/\__ \
   |_|\___|_| |_| |_| .__/|_|\__,_|\__\___||___/
                    |_|                         
-->

# Templates #
## Full Game Templates ##
- [Awesome space shooter on github](https://github.com/Blurlingite/space-shooter-pro) with a [demo at itch.io](https://blurlingite.itch.io/space-shooter-pro) Its got great graphics and explosions and sound.  Its super simple with probably random enemies coming at you, and the view is such that you cant see when theyre coming, but the basics are there for sure.  






<!--
   _____           _       _   _             
  / ____|         (_)     | | (_)            
 | (___   ___ _ __ _ _ __ | |_ _ _ __   __ _ 
  \___ \ / __| '__| | '_ \| __| | '_ \ / _` |
  ____) | (__| |  | | |_) | |_| | | | | (_| |
 |_____/ \___|_|  |_| .__/ \__|_|_| |_|\__, |
                    | |                 __/ |
                    |_|                |___/ 
					
-->

# Scripting #
## Script Inspector 3 ##
1. I heard a rumor thats not true: 
2. Biggest thing to get used to: Window Resizing to view google simultaneous (use a virtual desktop perhaps?
3. Doesn't indent to line up with other lines in a block comment
4. Doesn't explicity do a smart reformat.  I fully expected I could hit a key combination and it would reformat the whole document to meet coding standards (someones coding standards) but you have to open it in VS to do that (which is easy enough honestly so its not a show stopper)



## Runtime ##
I love the idea of having game logic able to be changed during runtime with no ill effects.
Possibly one of these would do the trick
* [Freedom Script](https://assetstore.unity.com/packages/tools/freedom-script-67440) or [Freedom Script Demo](https://assetstore.unity.com/packages/tools/freedom-script-demo-68621)
* [Moddable](https://assetstore.unity.com/packages/tools/integration/moddable-29573)
* [Miniscript](https://assetstore.unity.com/packages/tools/integration/miniscript-87926) voted as the least intimidating programming language


## Visual Scripting ##
* [Panda BT Free](https://assetstore.unity.com/packages/tools/ai/panda-bt-free-33057)  $0 Text based (the pro version is $30 and has an inspector drag and drop editor) but apparently works fairly well.
* [AI Machine](
https://assetstore.unity.com/packages/tools/ai/ai-machine-aim-visual-programming-and-ai-122906) $10 No.  This looks like a great visual scripting solution but there are no reviews.  It was updated earlier this year.  Not until there are reviews or a detailed how to on youtube.
* [Behavior Bricks](https://assetstore.unity.com/packages/tools/visual-scripting/behavior-bricks-74816) $0  No because reviews indicate shitty documentation lots of bugs and spotty support


# Event System #

- There is a system called [$0 Event Delegate System](https://assetstore.unity.com/packages/tools/integration/event-delegate-system-68785) that looks really good.
- [Script Intelligence Pack](https://assetstore.unity.com/packages/tools/integration/sip-script-intelligence-pack-96227) Free Updated in July. This lets scripts talk to one another.  "This has made my life as a beginner dev so much easier. You don't have to think about what a script can access and just do it and make everything coherent in a logical way thats very easy to understand"

# AI #
- [2D Platformer AI](https://assetstore.unity.com/packages/templates/packs/2d-enemy-ai-platformer-prefabs-137265) $5 and has 4 different interesting AIs for 2D platform games.  

# Controllers #

## 2D Platformer ##

BTW: To get tilemaps working without tearing change the cell gap on the grid to -.0001 (for xyz)

### Free from Asset Store ###
- [Platformer Microgame](https://assetstore.unity.com/packages/templates/platformer-microgame-151055) Free on the asset store, updated Aug 2019, Only compatible with Unity 2018.4.6 or before.
- [Sunny Land](https://assetstore.unity.com/packages/2d/characters/sunny-land-103349) Free Full platformer asset without wall jump and advanced things but still. 
- [Flat Platformer Template](https://assetstore.unity.com/packages/2d/environments/flat-platformer-template-108101) Free and looks pretty well featured
- [Standard Assets](https://assetstore.unity.com/packages/essentials/asset-packs/standard-assets-32351) Free and there is a simple 2d platformer scene in the standard assets

### Free from Github ###
- [Akashenen 2d Platformer Controller](https://github.com/akashenen/2d-platformer-controller) #Favorites MIT License updated in May with all features I can imagine.  Moving Platforms, Wall Jump, slide, one way platforms.  This one is really good with good code and examples and everything.  To use you have to copy all of the files over to a new project.  Issues: 
	1. Sprites don't flip left and right with the given shaders.  Have to make a new sprite material using default 2d shaders (lwrp->2d->Sprite-Lit-Default).  just swap the material in the prefab.  
	2. Have to start with the included scenes because 
		1. the default settings on the 2d character controller scripts are all 0s so you need reasonable values to start with (rationale: there are a ton of fields and theres no reason to learn what all of them mean and optimize them without even being able to try it out first and play with the values), 
		2. the camera has some special scripts attached too
		3. Theres also a physics config object that is required
	3. When you use the included scene:
		1. make a new tilemap and use the layers ground,ladder,box,owplatform,character,etc.
		2. swap your sprite, and animator for the player
			1. You will probably have to move the sprite renderer to the top level prefab from the child.  Probably delete the child.
		3. Reconfigure the ActorAnimation animator with your animation clips
			1. you can drag sets of sprites in to make animation clips
			2. You can probably (untested) drag your clip into the 'motion' field when you click on one of the animation states.  Once you have your animations in the project somewhere that should make this part pretty easy.
			3. You know what .. I dont think this package has any mechanism for flipping the sprite.  Easy Fix: Add a check for it where you set the animation data in the character controller 2d and flip the scale.x if its going left  This works well for me (Tested)
	4. Left xbox stick only works going to the right, dpad works both directions.
	5. Ladders dont work with tilemaps.  Only with sprite renderers. Clarification: it doesnt work with tilemaps witha ny kind of collider on them.  It works if theres a box collider on a parent empty gameobject and a tilemap as a child.  NO! That only partially works.  What works: Tilemap with child collider on ladder layer.  dont adjust the size of the collider just the size of the empty game object containing the collider.  If climbing to a platform make the collider align with the top of the platform
	
- [Vrompasa](https://github.com/vrompasa/2d-platformer-character-controller) a 2019 updated 2d platformer character controller.  No noted license information.  Simple code.  Wall jumping and sliding. one way platforms.  
- [Cjddmut Unity 2d Platformer Controller](https://github.com/cjddmut/Unity-2D-Platformer-Controller) Free - Updated 3-4 years ago but pretty advanced.
- [JPBotelhos Unity Platformer Controller](https://github.com/JPBotelho/Unity-Platformer-Controller) Everything but wall jump including double jumping and jetpacks.  Updated May 2018
- [Brackeys simple 2d Character Controller](https://github.com/Brackeys/2D-Character-Controller) 

### Commercial from Asset Store ###
- [Platformer Pro 2](https://assetstore.unity.com/packages/templates/systems/platformer-pro-2-140510) $80 and pretty advanced.  Competition with Corgi
- [Triangulo 2d Platformer Game Template](https://assetstore.unity.com/packages/templates/packs/2d-platformer-game-template-139368) $5 and has sword combat built in which loosk amazing imho.
- [Ghostisz Pixel Platformer Game Asset](https://assetstore.unity.com/packages/2d/characters/pixel-platformer-game-asset-156285) $15 and already used in a full game
- [UniPhys Advanced Platformer 2D](https://assetstore.unity.com/packages/templates/systems/advanced-platformer-2d-15175) $15 Ladders, Railings, Wall Jump, Moving Platforms, Updated this year, Tutorial included.
- [MCGames retro Platformer 2D](https://assetstore.unity.com/packages/templates/packs/retro-platformer-2d-132015) $9 Contra style game.  Probably a bit clumsy. Updated 1yr ago.  Looks great though.  
- [GraphicDNA Platformer Code Toolkit](https://assetstore.unity.com/packages/templates/tutorials/platformer-code-toolkit-130597) $9.90 for super mario 1 controls, art not included.
- [Wizcorp 2D Platformer Mini Staarter Kit](https://assetstore.unity.com/packages/templates/2d-platformer-mini-starter-kit-32816) $10 No because last update was 2015


## FPS ##
- [FP All In One] (https://assetstore.unity.com/packages/templates/systems/first-person-all-in-one-135316) Free and looks high quality.  Doesnt have shooting built in.


## 2D overhead ##
- [The Dungeon Game Kit](https://assetstore.unity.com/packages/templates/packs/the-dungeon-game-kit-136459) $5 mouse based dual stick shooter. Updated May 2019.  Comes with enemy and Boss AI
- [Aesmailsparta Food Fight on Github](https://github.com/aesmailsparta/FoodFight_C-Sharp_Game_Project) #Favorites a top down 3d shooter MIT license.





<!--
  __  __           _      
 |  \/  |         (_)     
 | \  / |_   _ ___ _  ___ 
 | |\/| | | | / __| |/ __|
 | |  | | |_| \__ \ | (__ 
 |_|  |_|\__,_|___/_|\___|
-->


# Music #

* [Chuck for Unity](http://chuck.stanford.edu/chunity/) is a music programming language and synthesizer right inside Unity
* [Procedural Music Generator](https://assetstore.unity.com/packages/audio/music/orchestral/procedural-music-generator-99791) 
* [$25 70 Retro Musics](https://assetstore.unity.com/packages/audio/music/electronic/retro-music-pack-70-59704)
* [$12.99 Wonderful Pop songs for happy games](https://assetstore.unity.com/packages/audio/music/pop/teen-pop-volume-1-147607) I absolutely love these for Beldevere the BatDragon
* [$10 Perfect for Time Crisis Exciting Game](https://assetstore.unity.com/packages/audio/music/electronic/retro-synthwave-music-pack-161716)
* [$25 for a full castlevania soundtrack or an epic RPG or Dungeon Crawler](https://assetstore.unity.com/packages/audio/music/electronic/retro-music-pack-70-59704)

with many styles available and a desktop demo to see what it can do.  Its pretty cool honestly but its a bit tricky to figure out how to make it sound consistent.  For the style presets it has though you could just hit go and it would be perfect. 











<!--
 __      __________   __           _____           _   _      _           
 \ \    / /  ____\ \ / /   ___    |  __ \         | | (_)    | |          
  \ \  / /| |__   \ V /   ( _ )   | |__) |_ _ _ __| |_ _  ___| | ___  ___ 
   \ \/ / |  __|   > <    / _ \/\ |  ___/ _` | '__| __| |/ __| |/ _ \/ __|
    \  /  | |     / . \  | (_>  < | |  | (_| | |  | |_| | (__| |  __/\__ \
     \/   |_|    /_/ \_\  \___/\/ |_|   \__,_|_|   \__|_|\___|_|\___||___/

-->

# VFX & Particles #

### Mesh Effects ###
$23 This is a cool package for adding cool glowy effects to any mesh
Dripping Water
Flaming like lava
Lightning 
Glowing like its hot
Creepy lava energy trails
+17 more

You can change the color

Trick for Mobile Platforms: disable HDR and check 'Use 32-bit Depth Display Buffer' for bloom to work correctly


[This is a library of particle effects, which you can freely use in your own projects.](http://wiki.unity3d.com/index.php/Particle_Library) I dont know how up to date they are but its cool anyway






<!-- 
  _                     _____      _                       _   
 | |                   |  __ \    | |           /\        | |  
 | |     _____      __ | |__) |__ | |_   _     /  \   _ __| |_ 
 | |    / _ \ \ /\ / / |  ___/ _ \| | | | |   / /\ \ | '__| __|
 | |___| (_) \ V  V /  | |  | (_) | | |_| |  / ____ \| |  | |_ 
 |______\___/ \_/\_/   |_|   \___/|_|\__, | /_/    \_\_|   \__|
                                      __/ |                    
                                     |___/       
-->
# Low Poly Art #
Well and other art too

Key Words for low poly:
Faceted
Polyart (poly-art poly art)
rigged
animated
mixamo
mechanim
Humanoid

## 2D Levels ##

- 1. [Top Down Pixel Dungeon by BitGem](https://assetstore.unity.com/packages/2d/environments/top-down-pixel-dungeon-level-02-22948)

## Levels ##

Terrains and Meshes 

- $5 for [23 beautiful hand painted terrain textures](https://assetstore.unity.com/packages/2d/textures-materials/hand-painted-terrain-textures-35188)
- $8 for [70 low poly terrains and backgrounds](https://assetstore.unity.com/packages/3d/environments/landscapes/horizon-low-poly-backgrounds-162115)
- $10 for [Low Poly Landscapes](https://assetstore.unity.com/packages/3d/environments/landscapes/low-poly-landscapes-pack-93955) 150 low poly items, mountains and possibly terrains.  could scatter the objects all over to make it look interesting.
- $20 for [1500 Modular Low Poly Terrain Prefabs](https://assetstore.unity.com/packages/3d/environments/low-poly-modular-terrain-pack-91558)
- * $15 for [25 Low Poly Terrains beautifully mapped and shaded](https://assetstore.unity.com/packages/3d/environments/landscapes/polyworld-low-poly-vistas-34775) They are meshes not terrains.  Comes with 14 faceted skyboxes.  

Modular


- $3.00 [Block World Pack](https://devilsworkshop.itch.io/essential-low-poly-isometric-3d-block-and-hex-pack) Like Kubikos World but way less detailed
- * $5 [Ground Block] From Cube World It looks so beautiful.
- $8 [Stone Blocks] Beautiful grass covered stone blocks th grass looks amazing
- $10 [Edge Isometric World like FEZ](https://assetstore.unity.com/packages/3d/environments/fantasy/edge-isometric-world-122886) Flat shader on each side of the asset, Cool snappy shapes, some cool glowy shapes and maybe a particle effect, Cool vertical fog, cool vertical shader, 
- $12 [Low Poly Asset Pack Blocky Snakes Environments](https://assetstore.unity.com/packages/3d/environments/low-poly-asset-pack-environment-map-blocky-snakes-126692) There are 6 cool environments here which all look really cool in their own right (or just $20 for 21 cool blocky snake models which look amazing)
- $15 [Low Poly Tower Defense](https://assetstore.unity.com/packages/3d/low-poly-tower-defense-pack-93334) loads of towers, some simple tiles and environment models which look super clean for these purposes.  The towers are not animated
- $15 [Low Poly Forest Parts](https://assetstore.unity.com/packages/3d/environments/low-poly-forest-seasons-set-81244) no terrains just clouds and forests and stuff.  Could use clouds as mountains tho!?! 

Free

- [Low Poly Hexagon Terrains](https://assetstore.unity.com/packages/3d/environments/low-poly-hexagon-tiles-and-objects-132355) By Black Dragon lots of cool colors of hexagon plus lots of little meshes to put on them or in them.  This could work for Time Crisis
- [Hexlands Low Poly](https://assetstore.unity.com/packages/2d/textures-materials/hexlands-low-poly-style-133586) these are lovely low poly style hex tiles.  High res ones are just $6
- [Voxel Environments 1](https://assetstore.unity.com/packages/3d/environments/fantasy/voxel-environments-1-152920) simple voxel block environment
- Quaternius - Some amazing Low Poly Stylized Trees especially
- Kenny

Premium Modular 

- $24.99 for [Kubikos 3D Cube World](https://assetstore.unity.com/packages/3d/environments/kubikos-3d-cube-world-117341)  There are also similarly priced packs for a village, city, and characters, animals, and a super active dev.  This would be fooking amazing for wave function collapse.  Also [$25 Kubikos 3D Cube City](https://assetstore.unity.com/packages/3d/environments/kubikos-3d-cube-city-147691) or [$25 Kubikos 3D Cube Village and farm](https://assetstore.unity.com/packages/3d/environments/kubikos-cube-village-farm-kit-137877)
- $30 [Proto Series Cube World](https://assetstore.unity.com/packages/3d/environments/cube-world-proto-series-144159)
- $50 [Low Poly Ultimate Pack](https://assetstore.unity.com/packages/3d/props/low-poly-ultimate-pack-54733) Enormous set of low poly assets, reminds me of the Polygon assets but vastly cheaper.  They are vertex shaded all of them I believe.  Updated This month!

Tools

- $8 [Minecraft style Retro Terrain](https://assetstore.unity.com/packages/3d/characters/retro-terrain-63693#reviews) looks just like minecraft, but can only be used for small maps or it gets too memory hungry.  Also comes with a cool blocky water system which fills things and spreads out and stuff.  Auto generates the world too which is cool.  I think this could be used for Time Crisis.

- * $10 [Terrain Creator Low Poly](https://assetstore.unity.com/packages/tools/terrain/terrain-creator-low-poly-146834) lets you draw terrain heightmaps using curves, and paints them for you and looks great. 
- * $15 [Low Poly World - Terrain Generator](https://assetstore.unity.com/packages/tools/terrain/low-poly-systems-low-poly-world-55808#reviews) I love how this looks.  I love it very much.  Changes your terrain to be low poly with adjustable options for size and facets.  It will then paint it for you.  You can't paint manually or change any colors of your terrains.  
- $25 [Low Poly Terrain](https://assetstore.unity.com/packages/tools/terrain/low-poly-terrain-46528) converts any terrain in to a low poly terrain.
- Free RunFlySwim Terrain Tools 
- $7 [Really nice Low Poly looking Terrain Textures](https://assetstore.unity.com/packages/2d/textures-materials/floors/low-poly-terrain-texture-pack-140922)

Premium Tools
- $30 [Clayxels](https://assetstore.unity.com/packages/templates/systems/clayxels-165312) Voxel system that lets you design whole levels and characters and everything in editor with simple shapes and great performance and even change things in game (destructible environments???)s
- $75 [Polaris V2 low Poly Terrain Generator](https://assetstore.unity.com/packages/tools/terrain/low-poly-terrain-polaris-v2-144645)

Water

- [$5 Hard Water Shader](https://assetstore.unity.com/packages/vfx/shaders/hard-water-70562)
- [Free Low Poly Water](https://assetstore.unity.com/packages/tools/particles-effects/lowpoly-water-107563)
- [Free Realistic Water Shader](https://assetstore.unity.com/packages/vfx/shaders/nvjob-water-shader-149916)
- [Free Mobile Water Shader](https://assetstore.unity.com/packages/vfx/shaders/mobile-depth-water-shader-89541) with a real simple look
- [Free VR Water Shader](https://assetstore.unity.com/packages/vfx/shaders/vrwatershader-108207) lets you make balls of water and looks really cool sloshing around.  Not for mobile or quest or go.
- [$5 Lowpoly Waves and Water](https://assetstore.unity.com/packages/2d/textures-materials/water/lowpoly-waves-and-water-156565)

## Space ##

Best

- $Free [Kenney.nl] assets are all free including characters.
- $30 [Dozens (60) of the cutest spacecraft ever!](https://assetstore.unity.com/packages/3d/vehicles/space/spacecraft-mini-103291)


Ok

- $Free [Spaceship Block Collection](https://fertile-soil-productions.itch.io/spaceship-blocks-collection) a modular set of spaceship assets
- $Free [Cool free spaceships](https://niko-3d-models.itch.io/free-sc-fi-spaceships-pack)
- $20 Low Poly [Space Invaders](https://www.cgtrader.com/3d-models/character/fantasy/low-poly-space-invader-set)

unsorted
- [Great Modular Spaceship Enemies](https://fertile-soil-productions.itch.io/spaceship-blocks-collection)
- More in bookmarks
- $1 [Cool Free Street pack](https://quaternius.itch.io/lowpoly-modular-street) modular
- $1 Cool [Free Racekart Track](https://fertile-soil-productions.itch.io/modular-racekart-track)

### Dungeon ###

Crawler or dual stick shooter

- $Free [Voxel Character Collection](https://assetstore.unity.com/packages/3d/characters/voxel-character-collection-73842) with animations
- $5 [Blocky Hero Creator](https://assetstore.unity.com/packages/3d/characters/humanoids/low-poly-warrior-cubits-warrior-81859) rigged with 10 animations
- $20 for [5 Heroes or square headed enemies](https://assetstore.unity.com/packages/3d/characters/humanoids/sd-rpg-pack1-45491) And 20 more characters just like these


- $5 [60 Voxel Fantasy Characters](https://assetstore.unity.com/packages/3d/characters/humanoids/voxel-fantasy-characters-pack-92617)
- $10 [70 Voxel Fantasy Characters](https://assetstore.unity.com/packages/3d/big-voxel-kingdom-pack-82841)
- $10.50 Shard Saga [Enemy Goblin Pack](https://www.cgtrader.com/3d-models/character/fantasy/shard-saga-enemy-goblin-pack) Interchangeable parts, No Textures (all vertex shaded, one material), rigged for shard saga animations also have a fantasy hero pack too
- $13.99 Shard Saga [Fantasy Hero pack](https://www.cgtrader.com/3d-models/character/fantasy/shard-saga-fantasy-hero-pack) interchangeable heads
- $20 for [Voxel Huge Pack of 55  Minecraft Monsters](https://assetstore.unity.com/packages/3d/characters/creatures/voxel-monsters-pack-154044) 

Premium

- $40 [1000+ pieces character creator](https://assetstore.unity.com/packages/3d/characters/humanoids/fantasy-customizable-pack-68910) to make enormous variety of custom humanoid characters, animated with 17 animations, mecanim support, From Suriyun
- $50 [MeshTint Toon Enemies Pack](https://assetstore.unity.com/packages/3d/characters/toon-enemies-pack-50421) 300 faceted animated dungeon enemy models

## Gritty ##
Best



- $5 for [5 Boximon Enemy Models](https://assetstore.unity.com/packages/3d/characters/boximon-pack-10-mega-toon-series-156475) absolutely perfect for a dual stick shooter or dungeon crawler - there are like 50 other boximons available so I would never run out
- $7 for 6 cute [animated dungeon monsters](https://assetstore.unity.com/packages/3d/characters/humanoids/3d-monster-pack-vol-1-144527)

- $20 [An Entire low poly War with tanks, planes, soldiers, jeeps, animations, controllers](https://assetstore.unity.com/packages/3d/props/low-poly-war-pack-124419)
- $25 for [5 awesome low poly soldiers](https://assetstore.unity.com/packages/3d/characters/humanoids/toon-soldiers-52220)
- $27 for [5 color configurable awesome robots](https://assetstore.unity.com/publishers/20422)
- $30 for [5 great soldiers](https://assetstore.unity.com/publishers/43520) just buy them independently
- $30 for [5 configurable mechs](https://assetstore.unity.com/packages/3d/characters/robots/sci-fi-animated-space-robots-43041)
- $44 [Sexy Girl Model](https://assetstore.unity.com/packages/3d/characters/humanoids/masa-124326)
- $50 [Meshtint Toon Enemies Pack](https://assetstore.unity.com/packages/3d/characters/toon-enemies-pack-50421)  also theres a [second pack](https://assetstore.unity.com/packages/3d/characters/toon-enemies-pack-2-64355)


unsorted

- $2 Super Low Poly [Creepy Graveyard Assets](https://www.cgtrader.com/3d-models/various/various-models/pigeon-game-assets) enemies, and landscape, and props
- $3.00 Low Poly 3D RPG assets [here](https://devilsworkshop.itch.io/low-poly-3d-and-pixel-2d-rpg-game-assets) and [Here](https://devilsworkshop.itch.io/low-poly-3d-rpg-item-asset-pack)
- $7 [Crawling Bug](https://www.cgtrader.com/3d-models/character/fantasy/crawling-bug) legacy mecanim animations
- $9.09 [Fat Troll Pack](https://www.cgtrader.com/3d-models/character/fantasy/fat-troll-family)
- $20 [33 Unique Skeleton Prefabs](https://assetstore.unity.com/packages/3d/characters/humanoids/33-animated-skeletons-set-17467) By Honeti who have lots of other types of enemies like zombies, animations are included, not recently updated
- $28 [Strange Robots](https://www.cgtrader.com/3d-models/character/fantasy/strange-robots) Possible problem with textures
- $30 for 8 [Fantasy Creature Enemies](https://assetstore.unity.com/packages/3d/characters/creatures/fantasy-enemy-pack-13489) recent update,

## Cute Characters ##

### For Tag Safari ###

Safari Hunt on its levels had
3 animals - wild turkey, fish, rabbit
3 animals - bear armadillo parrot
4 animals - bat spider monkey panther

- $Free [5 low poly animals in simple nature scene](- https://assetstore.unity.com/packages/3d/environments/simplistic-low-poly-nature-93894)
- $5 [28 low poly rigged animals](https://assetstore.unity.com/packages/3d/characters/animals/low-poly-rigged-animals-123656) wow what a bargain.  They look great too!
- $5 [9 Low Poly Animated Animals](https://assetstore.unity.com/packages/3d/characters/animals/animated-low-poly-animals-93889) OVERLAP WIth the free one
- $5 [Polyart Farm Animals](https://assetstore.unity.com/packages/3d/characters/animals/9t5-low-poly-farm-animals-163740s)
- Free [5 Faceted Nature Enemies](https://quaternius.itch.io/animated-easy-enemies) also [5 Dinosaurs](https://quaternius.itch.io/animated-lowpoly-dinosaurs) and [4 Monsters](https://quaternius.itch.io/lowpoly-animated-monsters) dont like the humanoid monster here but the other 4 are cool also [5 Farm Animals](https://quaternius.itch.io/lowpoly-animated-animals) without attack animations
- $5 [26 Animated and Rigged Animals](https://assetstore.unity.com/packages/3d/characters/animals/animal-pack-deluxe-99702) PBR some have secondary colors for variations, attack animations, and others
- $5 [32 Animated Animals](https://assetstore.unity.com/packages/3d/characters/animals/animal-pack-deluxe-v2-144071) second pack from previous, Elephant included!  Bat too!  Rhino,, tiger, camel
- $5 [9 Animated Dinos](https://assetstore.unity.com/packages/3d/characters/animals/dinosaur-pack-1-0-4362#reviews) mixed reviews due to some clumsiness
- $5 for [5 cool woodland creatures](https://assetstore.unity.com/packages/3d/characters/animals/small-animals-cartoon-critters-pack-86346) snake, turtle, snail, hedgehog, squirrel
- $5 [8 Cute animated Voxel Animals](https://assetstore.unity.com/packages/3d/characters/animals/voxel-animals-88264)
- $16 [38 Cute Non Animated Voxel Animals](https://assetstore.unity.com/packages/3d/characters/animals/little-voxel-69649)

- $30 [23 Realistic Low Poly Animated Animals](https://assetstore.unity.com/packages/3d/characters/animals/low-poly-animated-animals-93089) real high quality I love how they look and they all have animations.
- $24 [19 Realistic Low Poly Prehistoric Animals](https://assetstore.unity.com/packages/3d/characters/animals/low-poly-animated-prehistoric-animals-154363)
- $15 [6 realistic Low Poly Dinos](https://assetstore.unity.com/packages/3d/characters/animals/low-poly-animated-dinosaurs-110313)

Would be cool if you could only shoot the ones which were the right colors

### For BatDragon ###
Best Style match for my current game - this is probably best

- * $10 [33 Voxel Cute Animals](https://assetstore.unity.com/packages/3d/characters/animals/voxelblock-cute-animals-153014) I really like this one.  Animations unlikely
- * $10 [40 Voxel Cute Animals](https://assetstore.unity.com/packages/3d/characters/animals/cute-3d-voxel-animals-139406) Note: Reviews report this asset might be broken. these might even be cuter than the others!
- * $35 [21 Cute Zoo animals](https://assetstore.unity.com/packages/3d/characters/animals/cute-zoo-2-146060) 21 super cute animated animals!  also theres Cute Zoo 1 with 11 more and Cute Pet with 22 farm animals!  All three for $75

Perfect

- $5 [23 Voxel Animals](https://assetstore.unity.com/packages/3d/characters/animals/voxel-animals-23-130937) probably not rigged or animated
- $5 [8 Crossy Road Animals](https://assetstore.unity.com/packages/3d/characters/animals/voxel-animals-88264) with animations
- $4.99 [Cartoon Adventure Characters](https://assetstore.unity.com/packages/3d/characters/cartoon-adventure-characters-pack-136942) Animated, Super Cute, Recent Release, only 6 of them tho
- $10 [8 Configurable Cute Low Poly Toon Animal superpack](https://assetstore.unity.com/packages/3d/characters/animals/cute-low-poly-animals-super-pack-118520) Super configurable with hundreds of color variations, from REM Storm, includes a cute pug!
- $20 [9 Micro Monsters](https://assetstore.unity.com/packages/3d/characters/micro-monster-bundle-faceted-style-147722) Faceted style (polygonal style) with lots of variations and probably 15 other monsters I can get in the future. looks like they can be recolored too to make different enemies, and that they have some variations.  15 unique animations per monster too.  Only 9 monsters though so the scope of the game can't be up there with like Super Mario.  But I have the little Drago so I could do a test
- $10 [23 unanimated Cute little candy characters Tamago](https://assetstore.unity.com/packages/3d/characters/creatures/tamago-105799) No animations so I would have to make them, otherwise thse are wonderful!
- $12 [Gummies Animated Character Constructor](https://assetstore.unity.com/packages/3d/characters/gummies-toon-animated-character-constructor-120469) a base Gummy slime character, toon or smooth shaded, with large configurability

- $12 [22 Kubikos Mini Animals](https://assetstore.unity.com/packages/3d/characters/animals/kubikos-22-animated-cube-mini-animals-100696) animated and super cute
- $12 [Kubikos Mini Birds](https://assetstore.unity.com/packages/3d/characters/animals/kubikos-animated-cube-mini-birds-137343)
- $20 [60 voxel animals 30 plants](https://assetstore.unity.com/packages/3d/characters/animals/voxel-animals-plants-96469) all rigged and with optimized geometry.  I dont love it but they are interesting models and quite a bargain.
- $71 or $15 for [5 from Quirky Series](https://assetstore.unity.com/packages/3d/characters/animals/pet-animals-quirky-series-119975) SO DAMN CUTE and colorful! [also buy this](https://assetstore.unity.com/packages/3d/characters/animals/forest-animals-quirky-series-137294) [Also Buy these](https://assetstore.unity.com/packages/3d/characters/animals/farm-animals-quirky-series-118790)  [Also this forest number 2](https://assetstore.unity.com/packages/3d/characters/animals/forest-animals-quirky-series-137294) also more are available for $5 each

For Bosses!

- $30 [43 variations on Hamsto Model](https://assetstore.unity.com/packages/3d/characters/animals/hamsto-95596) with humanoid Animations - this would be PERFECT for a whole variety of mini-boss and full boss characters!
- $25 [12 unique variations on Funny Bear model](https://assetstore.unity.com/packages/3d/characters/humanoids/funny-bear-84649) This is a cool teddy bear like sack boy with 12 different variations including smoe scary ones.  Some could be enemies for sure.

### General Cute ###
Premium

- $30 for [Humanoid Yippy Kawai](https://assetstore.unity.com/packages/3d/characters/humanoids/yippy-kawaii-2-136853) humanoid dogs frogs monkeys but with huge cusomtizability variety so they can play lots of different roles
- $30 for [Humanoid Yippy Kawai 1](https://assetstore.unity.com/packages/3d/characters/humanoids/yippy-kawaii-88488) Cat Bunny Panda hugely configurable

- $120 (if you buy all three packs) for [9 creatures with 3 levels of upgrades](https://assetstore.unity.com/packages/3d/characters/creatures/monster-evolution-01-pack-01-cute-series-163585) [evolution 2](https://assetstore.unity.com/packages/3d/characters/creatures/monster-evolution-02-pack-01-cute-series-166745) [evolution 3](https://assetstore.unity.com/packages/3d/characters/creatures/monster-evolution-03-pack-01-cute-series-167016)
- [Free Pug with other farm animals](https://quaternius.itch.io/lowpoly-animated-animals)




Good

- $2-4/character with dozens or maybe hundreds of stylized sprites at [tokegameart](https://tokegameart.net/game-assets/page/7/?orderby=price)
- $20 [Super Chick Little Chicken with human legs](https://assetstore.unity.com/packages/3d/characters/humanoids/super-chick-142970)
- $40 [11 Micro Monsters](https://assetstore.unity.com/packages/3d/characters/low-poly-micro-monster-pack-8606) Not faceted style rigged and animated


Ok

- $10 [Toon Zombie Pack](https://assetstore.unity.com/packages/3d/characters/toon-zombie-pack-117481) Super Configurable zombies from REM Storms - good but I dont like them
- $20 [Crazy Micromonsters](https://assetstore.unity.com/packages/3d/characters/crazy-micromonsters-3664#content) low poly beasts with weird shapes and facial expressions
- $30 [13-21 VOxel animal prefabs](https://assetstore.unity.com/packages/3d/characters/animals/voxel-animals-pack-1-151257)
- $Free [Kenney.nl] assets are all free including characters.

## Unsorted ##


- $120 Amazing for a whole huge set of dungeon creatures heroe sand enemies from [Dungeon Mason](https://assetstore.unity.com/packages/3d/characters/humanoids/modular-rpg-heroes-polyart-138600) foor a medieval fantasy game
- MANY MORE IN BOOKMARKS


## Places to find art ##
- reddit.com/r/gameassets
- itch.io
- unity asset store
- cgtrader (usually $5-20 for a character)

- Craftpix.net for 2d art there are tons of attractive tilesets here.  1 month is $11 and 1 yr is $30 and you can use the assets forever.

- might be able to commission some more assets from
- [this guy](https://connect.unity.com/u/matheus-antonio)
- [janpec](https://assetstore.unity.com/publishers/1066)


## Specifics ##
Great

- [Synty](https://assetstore.unity.com/publishers/5217) has tons of cool polygonal animals
- [Meshtint](https://assetstore.unity.com/publishers/3867) probably have my favorites
- [Suriyun](https://assetstore.unity.com/packages/3d/characters/animals/tiny-dragon-161097) so many cool cute enemies!
- [BitGem](https://assetstore.unity.com/packages/3d/environments/nature-pack-proto-series-157704)

Good

- [Quaternius](https://www.patreon.com/quaternius)
- Kenney.nl
- [Honeti](https://assetstore.unity.com/publishers/5245) at the asset store
- David Oreilly [All characters from a dark movie](https://davidoreilly.itch.io/external-world-characters)
- Toon Enemies at the asset store
- [REM Storm](https://assetstore.unity.com/publishers/778)
- [Tycoon Tile](https://assetstore.unity.com/packages/templates/systems/tycoon-tile-156866) $65 makes populous looking terrains at runtime looks so amazing to me.


Custom Models
- This guy makes great models https://assetstore.unity.com/publishers/43520

<!--
  __  __           _               
 |  \/  |         | |              
 | \  / | ___  ___| |__   ___  ___ 
 | |\/| |/ _ \/ __| '_ \ / _ \/ __|
 | |  | |  __/\__ \ | | |  __/\__ \
 |_|  |_|\___||___/_| |_|\___||___/
-->





# Meshes #

### Optimization ###

### Level Optimizers ##
For lots of meshes (like especially for modular levels) there are some assets which optimize these levels
[Free Github Mesh Combiner](https://github.com/dawid-t/Mesh-Combiner/blob/master/README.md) Recent Updates.  Reduces batch calls significantly.  Might not cull unseen faces.
[$10 Easy Mesh Combiner MT](https://assetstore.unity.com/packages/templates/systems/easy-mesh-combiner-mt-138805) this one seems to do the job and is updated recently with great reviews.
[$15 Mesh Face Optimization](https://assetstore.unity.com/packages/tools/modeling/mesh-face-optimization-99412?q=mesh%20face%20optimization&orderBy=0) Recent Updates Almost no reviews. Not automatic like the other two, but i think it would do a good job in some circumstances.
This is for when you have combined primatives or other meshes to make bigger more interesting meshes and want to optimize them.  If you combine  meshes then they sit on top of and inside one another and this looks at that combined mesh and removes the invisible faces.
[$45 Super Level Optimizer](https://assetstore.unity.com/packages/tools/utilities/super-level-optimizer-25370) Recent updates Good reviews
[$45 Mesh Combine Studio](https://assetstore.unity.com/packages/tools/modeling/mesh-combine-studio-2-101956) My notes say its flaky, recent updates, good reviews

Different is this [$20 tool that doesnt lower tris but makes everything look low poly](https://assetstore.unity.com/packages/tools/level-design/low-poly-mesh-generator-59295) I wonder if it could take shitty realistic meshes and make them look so cool like low poly

## Blasting Meshes ##
(See below for more)

1. Mesh Explosion
2. Mesh Baker
3. Mesh Slicer
4. Alternatives
5. Mesh Animator
6. Mesh Creation and Decimation
7. Mesh Kit
8. Mesh Deformer
9. Fracturing & Destruction
10. Megapack

New Ones:
1. [$10 Fragmented Object Unity 3D](https://assetstore.unity.com/packages/3d/props/fragmented-objects-25699)


### Mesh Explosion ###
$20 Blast apart a mesh into its triangles
Level 2 (specific usefulness, great support)
updated last month released in 2012

it doesnt blast apart into different meshes but just into consituent triangles, but still it looks great!  You can even use a physics mode for each triangle with colliders and everything.
### Mesh Baker ###
$65  Combine skinned meshes and materials to reduce draw calls
Level 1(Great Usefulness, great support)

Fixes models and creates atlases so many meshes can share materials for static dynamic batching.  You run a report to see what objects are using what shaders and then make a mesh baker object for each shader, then assign each mesh to the mesh baker object for that shader.

It would be cool to make a #benchmark with this asset

Updated last month.  5 stars with 92 reviews.

### Mesh Slicer ###
$70 Slice Meshes, very performant
Level 2 (Specific usefulness, great support)

If slicing meshes is what you need then this seems to be a great asset. Reviews say its fast even on large meshes, it seems to add a texture to the inside of the mesh and also make mesh colliders out of the sliced sections.

#### Alternatives ####
I have a feeling that none of these are as performant as this asset
- I have something called fracturing and destruction (unfortunately deprecated but replaced by advanced tools megapack which is also out of date) that lets you do something related though not quite the same.  
- [EZY-Slice](https://github.com/DavidArayan/ezy-slice) is an MIT open source option 
- [Blinded Am Me](https://github.com/BLINDED-AM-ME/UnityAssets) is an open source option Here's a [video about the code](https://www.youtube.com/watch?v=xgoUmrhXyYE) and [another which uses the code extensively](https://www.youtube.com/watch?v=rL2JVgnit_c).  It was updated just a few months ago.
- [Turbo Slicer 2](https://assetstore.unity.com/packages/tools/modeling/turbo-slicer-2-73236) $60 All of these seem to be 2 years old!?!
- [Go Shatter Toolkit](https://assetstore.unity.com/packages/tools/go-shatter-toolkit-1017) $80 Two years old, doesnt shatter skinned meshes.

### Mesh Animator ###
$25 4-100x as many animated skinned meshes with this script
Level 1 (Great usefulness, great support)

It has a demo of thousands of uniquely animated meshes - theyre all the same skinned mesh but they are animated and move uniquely.

First released in 2014 its latest update was June 2019 so its really been kept up to date well. 

#### Some Quotes ####
- "Support for this asset is the best I have ever received"
- Really can get 10k units working on 970 class hardware
- "This asset increased my game's performance by 100x, seriously and literally."

### Mesh Creation and Decimation ###
Here are some of my own videos about this:
- [Low Poly Mesh from Pixel Art](https://youtu.be/kBVVXhdAQ5A)
- [Generating a 2.5d platformer level](https://youtu.be/6n9lCmTXtUA)
- [Making a platformer level from a picture](https://youtu.be/wEc3nc9n6mQ)
Also there are some great videos about making low poly objects like:
- [Making Low Poly Animals](https://youtu.be/JjW6r10Mlqs)

### MeshKit ###
$69
1. An easy to use in-unity decimator.  
2. An automatic LOD builder.
3. More

This is a really professional asset and has great tutorials and introduction videos and a really nice in-unity interface.
The decimator clearly works on high poly objects, and lowers a 250k mesh down to 60 with no visible changes.  I wonder how well it works on lower poly objects.

Videos:
[Demo of Decimation and Auto LOD Features](
https://www.youtube.com/watch?time_continue=156&v=c5504F5l7pA)

Unity Forum Post:
https://forum.unity.com/threads/meshkit-3d-editing-optimisation-and-asset-management-plugin.322637/


### Mesh Deformer ###

Current (Released March 2019) is compatible with 2018.3 (which is what I'm using atm)
Its mature and really cool.  You just take any mesh that you want to be a segment of something longer, then you make it 'rigid' then 'append' and use its spline editor to roughly position the next segment, and so on and so forth.  Eventually you click 'loop' if you want it to make a seamless loop, and then you click 'set mirrored mode' and it fills in the gaps and makes it all real smooth!

For a few things it seems to work really well such as making tracks like in the original video and for making curved walls for a castle boundary that would be great, easily changing the pivot on a mesh, and subtly bending meshes to make things more interesting, however I spent several hours with it tonight (7/4/2019) and I couldn't figure out a way to deeply and consistently leverage it for my purposes.  I feel like it has promise for me and plan to keep it in mind.

It has great reviews (the only bad review is someone who sent an email to the wrong address) and like I said before its really useful for some things so this is a very good asset.

1. Super simple mesh combination
2. Deforming meshes (making them bendy)
3. Modify Pivots
4. Apparently it can subdivide too

If you do something wrong there are lots of console errors about the GUI but they don't affect functionality.  

### Fracturing & Destruction ###
I bought this last November for $30 but its not available anymore.  Soon after 
I bought it it was deprecated and replaced by [a different package](https://assetstore.unity.com/packages/templates/systems/advanced-tools-mega-pack-43671) 

This works very well actually.  It pretty easily lets you explode a mesh and lets the parts fall on the ground.  Its pretty awesome!  I've used this quite a bit in my best VR game.

Since on the Unity Asset Store its deprecated, here's some info about the package [from their website](http://www.ultimategametools.com/products/fracturing)
They've got an overview, help, scripting, and an FAQ on that site.

It looks like of all of the tools in the Advanced Tools Mega Pack this is the only one that has been deprecated on the Asset store.
#### My Feelings about the package ####
The replacement for this deprecated package costs 6 times as much as I paid.  It also includes the Automatic LOD tool that I also already bought and when you add up what I've spent previously I am just a few bucks shy of what this costs but I don't get support for my old package.  This leaves a bad taste in my mouth.

### Advanced Tools Mega Pack ###
This is $180 and includes a number of tools: 
1. Fracturing & Destruction (which I already bought for half off of $60)
2. Ultimate Rope Editor (which I don't think I care about)
3. Concave Collider (which looks cool but I don't completely understand)
4. Mesh Combiner (which I already have several of)
5. Automatic LOD (which I already bought for half off of $90)
6. Mesh Simplify (which apparently comes included in F&D above)

Oddly the latest reviews seem identical to the Automatic LOD pack.  I'm not sure why that is.  The reviews on the rope editor are different.  Some of the reviews of the Mesh Simplify tool are the same.

A common theme in the reviews is that the developer isn't providing support. That is so disappointing especially on a package that is $180.  The latest version of the whole $180 package was released on August 10 2017 which as of today is 23 months ago (almost two years).   I emailed them on July 6 2019 and will be interested to see if and when they reply.

They have a [website](http://www.ultimategametools.com/products/advanced_tools_mega_pack)

The Concave Collider looks pretty awesome actually.  It allows for complex colliders instead of having convex colliders which provide a really rough and imprecise solution.  The [video on this](https://www.youtube.com/watch?time_continue=6&v=mu__FxT8Gzk) explains it pretty well. 



## Investigate ##
- Concave Collider (in advanced tools mega pack)


## Just Ok ##

### Scene OBJ Exporter ###

Free ( Nov 2018 )
Seems to export all of the meshes in your entire scene into one OBJ
[Scene Object Exporter](https://assetstore.unity.com/packages/tools/utilities/scene-obj-exporter-22250)

### FBX Exporter ###
Free (Nov 2018)
The latest version of this is available via the package manager from Unity 2018.3+
Its supposed to setup a round trip workflow between Unity and your Modeling software.

### Meshinator ###

Free (I own this)
Real time mesh deformation
This one deforms the mesh based on physics calculations
[Meshinator](https://assetstore.unity.com/packages/tools/physics/meshinator-realtime-mesh-deformation-8228)

It can smoosh spheres and make crystals break and shatter
Last release was in 2015 so I don't know how well it will work now.

### Automatic LOD ###
$90 (Purchased Nov 27 2018)
If I'm being honest this asset makes me mad.  I remember buying it last fall when it was on sale at the time I was thinking it would help me make my games less resource intensive.  I also felt at the time like I really needed it so I didnt have to do all of the LOD on my own.  Although certainly doing that on my own would take longer, and an automatic solution is a godo plan, I'm feeling a little taken advantage of.  The asset called MeshKit is less money (not too much more than I paid when this was on sale) and has this feature and many more.  This one has (since I bought it) been somewhat abandoned.  There are reports in the reviews of it not working with recent Unity versions and the publishers not responding to requests for support.  Other reports of it just not doing a good job. Others saying the extra LODs takes up a lot of space.  Others say it messes up the skins on decimated models.  Others say it works but doesnt do any batching.  That parts ok I guess.  They both have good video documentation.  I of course am responsible for having bought it but I regret it now and wish I had bought the other one.  I also suspect I can get this feature for cheaper in some other asset that I don't even know about yet.  I just have a bad taste in my mouth at the moment.  On the bright side maybe when I get to the point where I might need it I will love it.  

## Not Recommended ##

### Mesh Toolkit ###
AKA Mesh TK
$10 (Purchased Dec 8 2017)
This lets you manipulate meshes in some pretty advanced ways and vertices and save them as new OBJ or FBX assets and lets you set pivots and remove unused vertices and much more.  It could be a little like having a basic blender in Unity.

The video shows the features of selecting triangles and faces, extruding, subdividing, deleting, flipping (faces I think), selecting by face, selecting with a click and paint, selecting multiple faces.  You can make those changes and then save them back to the files in the scene or you could export them to mnew objects.

I couldn't get it to do anything at all in Unity 2018.3.4f1  Further the authors website is entirely dead.  I can't imagine this is ever going to work or get any support.  The last update was 2015, there is no longer a support or documentation website since those links are now entirely down.  Other people (in reviews) are reporting that it doesn’t work for them in Unity 2018 either.  
Recommendation:  Supported Unity versions on the asset store say 4.0 or later however I think thats no longer accurate and needs to be changed to 4.0 through Unity 2017.


# Procedural Generation Toolkit #

The [Procedural Generation Toolkit](https://github.com/Syomus/ProceduralToolkit) seems to do some things that make procedural generation more pleasant.  Looped arrays (so you can just keep adding 1 to the index I presume), Color gradients, and colors in HSV 

## Investigate ##
[Procedural Toolkit](https://github.com/Syomus/ProceduralToolkit)
[Straight Skeleton](https://en.wikipedia.org/wiki/Straight_skeleton) which can be done by the Procedural toolkit!  This might be perfect for what I need for beldevere!
[CJ Lib](https://github.com/TheAllenChou/unity-cj-lib)
[Bear Framework](https://github.com/MrSpecjal/unity-bear-framework)












<!--
  _                    _   _____            _             
 | |                  | | |  __ \          (_)            
 | |     _____   _____| | | |  | | ___  ___ _  __ _ _ __  
 | |    / _ \ \ / / _ \ | | |  | |/ _ \/ __| |/ _` | '_ \ 
 | |___|  __/\ V /  __/ | | |__| |  __/\__ \ | (_| | | | |
 |______\___| \_/ \___|_| |_____/ \___||___/_|\__, |_| |_|
                                               __/ |      
                                              |___/       
											  
-->
# Level Design #
* [MonKey](https://assetstore.unity.com/packages/tools/utilities/monkey-editor-commands-productivity-booster-119938) seems to have some effective level design shortcuts built in.  its regularly updated and is made by game devs who are using it day to day so I have a good feeling about this.
* Octave looks really useful.
* Free for GPL Software [Universal Sprite Sheet Character Generator](https://www.gamefromscratch.com/post/2019/08/06/Universal-Sprite-Sheet-Character-Creator.aspx)


# How much variety #

Wonder Boy 3
27 + 6 bosses in wonder boy 3 I think that doesnt even include variations like red, green blue
11 musical numbers

Chris' Maps had 20-30 terrain tile types in each map (although they were randomized somewhat for variety

# Wave Function Collapse #

Infinite City
Why did I find out about this? I was transfixed by this [Infinite City](https://www.reddit.com/r/proceduralgeneration/comments/f2psa1/infinite_procedurally_generated_city/) technically it was [this video](https://youtu.be/-W7zt8181Zo) and then here is the [source code](https://github.com/marian42/wavefunctioncollapse).  Here's a [playable build](https://marian42.itch.io/wfc) and [an article about it](https://marian42.de/article/wfc/) and [a second version with trees](https://www.youtube.com/watch?v=7ffT_8wViBA)

To get this original bitmap based algorithm working on Mac I had to do kind of a lot.  Heres [the original version of the function](https://github.com/mxgmn/WaveFunctionCollapse) Its in dotnet so I needed to download the runtime even though I already had a runtime.  I had to install [dotnetcore](https://dotnet.microsoft.com/download/dotnet-core/3.1) You have to be able to type 'dotnet'.  I had to brew install mono-libgdi or something like that (it suggested the right package).  I had to install several versions of [system.drawing](https://www.nuget.org/packages/runtime.osx.10.10-x64.CoreCompat.System.Drawing)
[and this system.drawing] https://www.nuget.org/packages/System.Drawing.Common/5.0.0-preview.4.20251.6) finally I had to run `dotnet run WaveFunctionCollapse.csproj` and then it worked really well.  You have to change samples.xml to point to the images you want to run.  Some of them like "summer" have their own folder and their own special XML which defines the compatibility for each tile (N S E W)

I had [tried it in python](https://github.com/ikarth/wfc_python) but I couldn't get any of those running [even the one from 2019](https://github.com/ikarth/wfc_2019f).  Probably user error but neither of them ran and they seemed to have simple problems I tried it in virtualenv and python 2 and 3 and nothing worked.  

To work further with this there are several options: 

* Heres an asset [Tessera](https://assetstore.unity.com/packages/tools/modeling/tessera-procedural-tile-based-generator-155425) which lets you do this WFC for just $5 and has great reviews. Also theres a $50 with source code
* Heres the [source code for the infinite city](https://github.com/marian42/wavefunctioncollapse)
* Work with the [original dotnet version](https://github.com/mxgmn/WaveFunctionCollapse) that I got working above
* And heres a [Unity Adaptation](https://selfsame.itch.io/unitywfc) of the algorithm that works in 3d and has some instructions for how to get it working. Updated Nov 2019




<!--
 __     ___      _               _   ____            _ _ _         
 \ \   / (_)_ __| |_ _   _  __ _| | |  _ \ ___  __ _| (_) |_ _   _ 
  \ \ / /| | '__| __| | | |/ _` | | | |_) / _ \/ _` | | | __| | | |
   \ V / | | |  | |_| |_| | (_| | | |  _ <  __/ (_| | | | |_| |_| |
    \_/  |_|_|   \__|\__,_|\__,_|_| |_| \_\___|\__,_|_|_|\__|\__, |
                                                             |___/ 

-->


# Virtual Reality #
* VR Shooter Kit - This was released recently and has been getting lots of support and I'm glad because we needed something up to date like this.
	* Comments: The SteamVR Installation manual doesn't mention what to do with the SteamVR_UnitySettingsWindow. I  selected Accept All and I hope that was right.  At least Steam VR suggested "You made the right choice!" with a popup haha.  
	* Immediately after installing when I open the Example_SteamVR it says Missing Prefab.  
	* There was an error when I selected Create Input Bindings and hit overwrite but hitting it again and the error doesnt reappear.  later: Interesting that when I did the final step in the installation manual (Save and generate) the error happened again (almost the same error anyway)
	* The SteamVR Installation manual in step 8 should say something like "Now turn on Steam VR (from inside Steam), Open the example secene hit run and put on your headset to see some of what can be done with VR Shooter Kit"
	* Manual: The path in step 2 says VRShooterKit/Prefabs/SteamVR but there isn't a SteamVR folder there, in the photo it gives me a clue to look in the PlayerSetup/SteamVR so I used that.
	* VR Shooter Kit 
	* VR Shooter Kit Test 2 is 2018 (accidentally) but I did everything else right and theres still a json error and it doesn't recognize my controllers
	* VR Shooter Kit Test 3 is 2019 and latest kit and Steam 220.  Just installing steam I get that json error.  Create input bindings Overwrite and I get it again.  However one thing is different: When I clicked on Window SteamVR INput it said "looks like you are missing actions.json would you like me to generate"  I feel like it did more when I hit save and generate.  It didn't work either (the hands were behind me floating in the air instead of on the floor)
	* VRSK 2019 SteamVR245 is what the name says.

I followed the VRShooterKit authors video recorded instructions to make this binding.
VRSK132 Unity2019.2.8f1 SteamVR245


<!--
   ___  _   _               
  / _ \| |_| |__   ___ _ __ 
 | | | | __| '_ \ / _ \ '__|
 | |_| | |_| | | |  __/ |   
  \___/ \__|_| |_|\___|_|   
                            
-->

# Other #
- [Cinemachine Camera in 2D](https://github.com/akashenen/2d-platformer-controller)  This has great cinemachine camera controls

# ASCII Art #
[Ascii Art](http://patorjk.com/software/taag/#p=display&f=Standard&t=Virtual%20Reality)
[Ascii Art](http://patorjk.com/software/taag/#p=display&f=Standard&t=Virtual%20Reality)



<!--
   ___  _   _               
  / _ \| |_| |__   ___ _ __ 
 | | | | __| '_ \ / _ \ '__|
 | |_| | |_| | | |  __/ |   
  \___/ \__|_| |_|\___|_|   
                            
-->

# Other #
- [Cinemachine Camera in 2D](https://github.com/akashenen/2d-platformer-controller)  This has great cinemachine camera controls

# ASCII Art #
[Ascii Art](http://patorjk.com/software/taag/#p=display&f=Standard&t=Virtual%20Reality)
[Ascii Art](http://patorjk.com/software/taag/#p=display&f=Standard&t=Virtual%20Reality)


# Investigate #
## Humble Bundles ##
- Humble Bundle: Ultimate Game Music Collection
- uMMORPG
- UFPS: Ultimate FPS
- Modern Day Music Mini pack
- RPG Maker 10 Tileset Packs
	- Adventurers Journey
	- Tyler Warren's First 50 battler pack dlc
	- Royal Tileset Pack DLC
	- High Fantasy Resource Pack DLC
	- High Fantasy Main Party Pack DLC
	- Futuristic Tiles Resource Pack DLC
	- Inspirational Music pack DLC
	- Tyler Warrens Second 50 Battler pack DLC
	- Zombie Survival Graphic Pack DLC
	- Rural Farm Tiles Resource Pack DLC
- Heroic Fantasy Creatures full pack 
- Exclusive RPG Maker Resource Pack
- Best of Member Resources Samples
- Inventory Pro
- FlowCanvas
- GameFlow
- Realistic Effects Pack 4
- Universal Sound FX
- Gaia
- Heroic Fantasy Creatures Full Pack Volume 1

## Interested May 2020 ##

- $45 Probably would like the $45 Super Level Optimizer

For Characters:

- $10 for 8 Beautifully cute characters '8 Cute Low Poly Animals'
- $5 for 6 Cute Adventure Characters
- $free the kenney.nl enemies
- $10 for 23 PERFECT Cute little candy characters - these seem perfect and like just the right amount
- Really I'm looking for Low Poly Polygonal Enemies to match mine, like just some super simple creatures made out of basic shapes.  Preferably Vertex Shaded in a way that I can easily change several of their colors in scripts and in such a way that I can swap parts to give them different characteristics.
- Hactually I can use the Simple Gems Ultimate to possibly make my own enemies!
- Eventually the Meshtint enemies seem best by far.  A pack of those might go a long way.