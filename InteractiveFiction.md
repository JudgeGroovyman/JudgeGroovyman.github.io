PASTE THIS IN TERMINAL `grip  --user-content --user= --pass= . 2626)`
[TO VIEW THIS CLICK HERE](http://localhost:2626/InteractiveFiction.md)


# IF Comp 2019 #
Spoilers abound here

* Girth Loinhammer and the Quest for The Unsee Potion - "Beaureaumancer" HAHA!  This is really cool I got an adventure sheet and several online dice and am playing along.  "The worldbuilding in this place is a little heavy-handed" classic!  I didnt get the elixir but it was a really cool game! it says 15 minutes but it took me 30 and it was great.
* Turandot - "your prison cell did not incommode me in the least.  ... Four stars out of five.  Would recommend."  haha!  OMG I just finished it - I played it all the way through and have a feeling that you can't actually die in the game but what a wonderful tale.  I played it over 2 days and enjoyed it thoroughly and feel lucky to have found it.  Theres even some deep insights about human connection in there.  
* The Surprise - This is good.  I love how it times the process and doesnt let you proceed.  I loved it.  Its a short exciting emotional experience by Candy Meldromon.  I liked how it kept you in suspense.  
* The Island - This is really good.  I dont know how I could have convinced anyone else to come with me but I wish I could have

# Writing Interactive Fiction #




Note to self: Read This Over and Over.  Edit it.  Work with it.

## Descriptions ##

### Special Responses to Ordinary Actions ###
It is remarkable how much richer one can make a game feel just by writing special responses to ordinary actions.

Descriptions: action responses
One option, if true puzzles seem out of place in a work, is to offer the player some easy but rewarding physical interaction. Make it obvious what to do, but make the doing of it interesting — that is, write in interesting sensations as a result; 

Example: or have NPCs around comment on the activity 
Lost Pig gets enormous mileage out of letting Grunk do obvious things while the gnome and the pig react); 

Example: or have a seemingly straightforward action reveal some rather unexpected outcome. (Act of Misdirection is a great one for this: it leads and prods the player through performing a magic act, getting him largely to perform actions that the game has more or less laid out, but the outcomes are fascinating.) 

It is remarkable how much richer one can make a game feel just by writing special responses to ordinary actions. How does the bar of platinum feel when you pick it up? How does the player character feel about taking it? Can we come up with something better than “Taken”?

Attention to these details can make even fairly standard puzzle-game kinds of interaction into something with a fair amount of narrative content.

### Verbs ###
Verbs: use a small consistent set of verbs and actions 

I add the word “systematic” to indicate something more coherent and consistent than a mere mechanic, a design in which consistent verbs are used repeatedly across the course of the game, and the player is taught to interact with the model world in such a way as to gain in effective agency as they are able to anticipate more and more of the results of their actions.

### Never tell the player "you can't go that way" ###

The point of all this is to avoid having directions where there's no described barrier, no reason to assume the presence of a building, a cave wall, or an impenetrable forest, but where the game nonetheless tells the player only, "You can't go that way." This situation leaves a strange blank the imagined world -- as though the player had looked around and seen only an untraversable grey fog to the west, the wall at the end of the world.


### Creativity: writing room descriptions ###
Writing about space means thinking about the relationship of one place to another, the types of objects and people that would be in that space, the atmosphere and mood of it, the culture, the assumptions, the memories the protagonist might have there.

### Creativity: great examples of room descriptions ###
`Sun-sleeps-in-the-rock	Slickrock hillside, orange-red, a hot sun low in a cloudless sky, a hard dry heat. Far downhill, the rock gives way to thornveldt, the plain punctuated by distant outcrops.
Beneath a lone, broad-spreading shade-tree, people kick back on boulders and blankets and camp-chairs. There are meaty things sizzling over a fire, a couple of coolers.
And outwards, across the sun-baked rock, you can sense the Barren Way beckoning.
The tangle extends to the north, south to None Know The Hour, east to The Pleasant Month of May, west to No Place To Rest Your Head and Outside.`

``>x meat
There are some baked potatoes roasting in the embers, and a big pot of thick corn pap over to the side of the fire, but the focus is clearly on the meat. There are some slabs of lean beef on the campfire grill, but most of the real estate is taken up by thick, smoky, grease-dripping sausages. ``

``>x people
A conspicuously mixed-race group; maybe a third each of unambiguous white and black. Dressed for a hot climate that’s rough on clothes. There’s some low-key chatter and occasional trips to the cooler or the fire, but your general impression is of a pride of very well-fed lions taking naps.``

— Invisible Parties, Sam Kabo Ashwell

There’s an implacable landscape here, evoking color and temperature and scent and shape, but much more than that as well, a whole implicit cultural setting. Each object examined layers in new details. 

## Goals of Interactive Fiction ##


### Goal: ###
I want to make my game world feel deep and alive

### Goal: ###
 This is one of my favorite things about parser IF, both in writing and in reading: the sense of place and presence that invites exploration. I think it’s also theoretically possible to accomplish in choice-based stories, but most choice-based systems do not really encourage this; their mechanical prompts are different.

### Goal: ### in the ideal IF setting, the parts of the setting relate to each other in comprehensible ways. Things are located sensibly. 

## Story Flow ##

Story: a story is a sequence of scenes
When I plan plot-heavy IF, I think of it in terms of a sequence of scenes. 

This doesn’t mean that the gameplay needs to be rigidly linear: scenes can occur in varying orders, or there can be plot branches, or scenes that can be skipped depending on player action. But I nonetheless do the organization in terms of scenes.

------

Scenes: how to define a scene
A scene has a definite beginning and a definite end. It usually has to take place in a specific area of the game map (which may mean that the player triggers it by entering that area [as in City of Secrets] or that I move the player myself when the scene is scheduled to start).

------

Story: end each scene with a clear hook
Following some writing advice I got long ago, I try to make most of the scenes end with some kind of clear hook. At the end of the scene, the player should ideally have a new take on what is happening, or a new problem to solve, or a new question about what is going to happen next. Exciting the player’s curiosity about something is especially powerful in getting the player to keep playing.

Am I giving the player enough to wonder about? Are there, in fact, hooks at the ends of the major scenes which give the player a reason to want to come back and find out more? 
Is the story best served by a single perspective? Or do I need the player to hear multiple versions of the same event?


------

Puzzles and story branching:
If you use numeric scores to delay branching, you’ll quickly find that the entire game is about these numbers. Every chapter should change the stats and test them to make earlier decisions meaningful.
The stats will embody the essential conflicts of your story—the main decisions that the players will make as they play your game—so it’s critical that you choose good ones.


## Story Gimmicks ## 

### Story how to portray real emotion ###

At any given point, who is moved by very strong feelings, especially grief or passion? Maybe that person should not be the viewpoint character for that scene — exactly because it is so hard to guarantee that the player will identify. Television shows often use a technique I mentally label “distance from grief”: when a character learns about a death or something similarly awful, the camera pulls away, letting us see a long shot, the body language of devastation, rather than a close-up of the face and the sounds of sobbing. That distance makes the grief universal and sympathetic rather than specific and voyeuristic. It lets us fill in our own experience of loss, without the accompanying embarrassment that we sometimes feel when we’re around crying people. Similarly in IF, I suspect (though I’m short on examples at the moment) that it’s more effective to (a) let the player know in advance how much a character will be devastated by the bad event to come but then (b) pull back a little and let the player be outside that character’s head when the storm hits.


### Descriptions: Gimmick: alter the description over time ###
Variety and Depth Changing existing locations is another way to keep a map entertaining. "A Change in the Weather" (Andrew Plotkin, 1995) alters descriptions of the locations as time passes, so that places that have been visited before take on a new atmosphere and new activities become possible; "Being Andrew Plotkin" (J. Robinson Wheeler, 2000) shows the same places from the perspectives of several different characters, and the differences in their viewpoints is the source of much of thef game's subtle richness.


### Description gimmick: talk about a central far away object from several different rooms ###
Seeing far away objects before you are able to reach them (the sinister tower at the top of the hill) builds a sense of anticipation. It also deepens the sense that the setting you're moving around in is not just a movie set.



### Descriptions of locations:  deter exploration by making it uninteresting ###

Describe the view of what lies in some direction, but in such a way that it's clear to the player that there's nothing interesting over there: a broad expanse of desert or wasteland, a thick forest, a trackless wilderness or a tangle of suburban streets will all discourage the intrepid adventurer. Or tell the player how the landscape continues on the far side of an uncrossable chasm or rushing river.

False Doors: Some games include barricades that look like they might one day be traversable, but aren't, or doors that are locked and can never be unlocked during the whole course of the game. Used very carefully, the false door makes it seem as though the game environment is larger than the area the player is actually allowed to walk through. Make the door too interesting, however, and the player may waste a lot of time trying to open it, to her frustration. It's worst of all if she feels cheated at the end of the game because she never found out what was behind that door: instead of impressing the player with the expanse of your game world, you've drawn attention to its limitations and wasted her time.

It's the boring door that works best in this situation. "Doors line the hallway on both sides; your own is E5, to the north." Now the author has created an environment that suggests adjoining locations, as complex as the real world, but where there isn't much temptation to try the non-descript doors, which do not even have compass directions explicitly associated with them. In descriptions it helps to be as explicit as possible about the nouns and verbs to be used with the interactive, implemented parts of the game world; being vague is a sign to the player that the vaguely-described thing is only scenery. (Not handling this distinction well -- by encouraging too much interaction with unimplemented items, or not giving enough information to use critical ones -- is one of the hallmarks of an inexperienced author. As always, beta-testing helps turn up trouble areas.)
# The Rest #

------

* Authors can minimise this by automating obvious actions, or action sequences which the player has already 'learned' and which don't vary. (In the above example, a command to enter the door might automatically perform unlock, open, enter, close, and lock actions). This is sometimes called autopilot.
* Some games automate this with a GO TO command, allowing players to return to places they have already visited with a single command.

------


Descriptions: address everything the player might try with a consistent narrative voice
Doing a full set of library message replacements, meanwhile, is a more of an exercise in narrative voice, practice thinking through how a specific protagonist would describe all these ways of interacting:
>touch wall		 That feel just like wall.
>jump	 Grunk jump and jump, but moon still too high to reach.
>get all	There not any here!
>undo	Outside	[OK, Grunk not do that.]	— Lost Pig, Admiral Jota
------

Puzzles:
This is a system that — by heavily advertising risk — gets consent from the player to make something bad happen to the protagonist, and encourages the author to write in setbacks, or at least non-progress, as a core part of the design process.

------

Creativity: generating an interesting setting
One usually starts somewhere. An image out of a memory, or a dream. Some interesting error of interpretation, a metaphor taken literally, a what-if possibility that lodged in the brain and is begging to have its implications explored. What if the world really were flat? What if numbers were characters you could meet on the street? What if there were a god who collected people's memories in a bottle? What if time flowed backwards, what if Napoleon had died in infancy, what if you woke up one morning and found yourself to be a giant cockroach?

------

Creativity: generating an interesting setting
These starting ideas can be about other things than the state of the game world. They can be ideas about genre ("I'd like to write a Western."). They can be ideas about presentation: the voice you're going to use to narrate the game, an attitude, a style, a programming trick that no one has tried yet. These are all valid seeds -- the kind of thing you can take and start writing with -- and they can come from anywhere or nowhere.

------

Creativity: generating an interesting setting
Here's the thing: in my experience the best games are generated when I start with more than one of these ideas, preferably ones that don't obviously go together.

------

Creativity: how to come up with an interesting setting
"I'm going to write a game set in the Wild West" is okay, but it doesn't generate any conflicts; it doesn't produce any story. "I'm going to write a game about a mute woman in the Wild West who is, unbeknownst to those around her, actually a correspondent for an important newspaper" suggests places to go. Why is the woman doing this? How did she get started? Whom does she meet? Who takes her for granted, and who sees her for what she is? What is her attitude to her handicap? How is this going to affect the gameplay?

ideally it should be combined with a couple of other ideas that have nothing (at first glance) to do with that premise.  this can generate new and productive questions. It also decreases the risk that what you're about to come up with is a hopeless cliché.

------

Creativity: reinventing something cliche into something fresh
[A brief digression about clichés. The problem with them isn't that they present ideas that people have seen before, but that they allow the author to rely on a crutch -- the tried-and-obvious, the generic -- instead of inventing something afresh. You want to write a game with dragons and elves? Fine. But do the work of reinventing the dragons and elves yourself. Ask yourself the questions over again, and don't be satisfied with the prepackaged answers: What do they look like? What do they do? Where do they come from? People like to remark on the fact that Andrew Plotkin has written award-winning games using two of the settings (caves, one's apartment) that are considered most tedious and overdone; the point isn't that he possesses mystical Zarfian Powers, but that he understands the process of imagining something anew. Imagination is, perhaps counterintuitively, a discipline; the good news is that, like other disciplines, it can be cultivated actively.]

------

Creativity: questions to help you think of multi pronged ideas
There are a whole host of ways to get at these multi-pronged ideas. Take two unlike genres and ram them together to see what they produce (Elves in 1890s New York. Aliens land in Heian Japan. A cyberpunk comedy of manners.). Pull together thoughts you had intended to use in two different games. Take some obvious or easy assumption and warp it (the cute child you were going to have accost the PC asking for help now becomes menacing or threatening somehow instead.).
And sometimes things may come to you even when you're not looking, and demand to be admitted, which is why I am constantly scribbling IF-related notes into the notebook I supposedly use for schoolwork. 

------

Creativity Example: where all of the ideas came from
The bell on the darkened lake shore, in Metamorphoses, comes from a class I had on Japanese art; the gondolier's cloak is a reference to the dark cloaks of the assassins in Gene Wolfe's work; the faces on the side of the gondola are the upturned faces in hell in What Dreams May Come. The obsession with clockwork is partly a nod to Myst, partly a bow to the machinery in Umberto Eco's Island of the Day Before. The cistern is an actual cistern I saw in Greece, though the paintings on the walls I imported from elsewhere. And so on.

------

Sometimes I'm working on background and I'm trying to remind myself of the kinds of questions I should be asking. It's easy to write a room description that hasn't been thought out enough; it's easy not to do enough of the work of imagining. Looking at a book about, say, everyday life in ancient China makes me aware again of some of the relevant questions: what did the people here eat? what did they wear? what were the politics? Obviously the depth and complexity of the background you're building will determine what questions are useful ones to ask yourself.

And sometimes I don't even know what I'm looking for, exactly. Sometimes I just page through things: travel magazines; atlases; historical documents; illustrated books of antiques. Encyclopedia articles on costuming through the centuries. Web pages on 19th century railways, or out-of-fashion cars, or demonology, or the elements. I think of it as a kind of seeding process: random number generators need somewhere to start, and so does the image-generating part of my brain. Often some strange landscape will catch my eye, or some building, and even if that never makes it all the way into the game itself, there is a quality of it that informs my sense of what the feel of the game is about. For one of my works in progress I keep a collection of photographs of various objects that I consider in some way relevant: things that I imagine could exist in the game world even though they may not actually show up.
Sound like a lot of work? Perhaps it is, but it's largely fun work -- and, at least for me, corresponds with the kind of thing I tend to do by way of procrastination and relaxation. I like going in bookstores and wandering around pulling things off shelves, letting my imagination wander. It's not a lot of additional effort to take the interesting and curious things I run into that way and see whether they fit in anywhere with my work in progress.

-----

Maps: keep it small and don't overwhelm the player
Nonetheless, it helps the player if you don't give him too huge a landscape to wander through at once: too much freedom is overwhelming, and one is left without a sense of where to go. 

The idea of locked doors and keys may be a somewhat overused one, but there lurks an important issue there: in order to control the pacing of the game and give the player a comprehensible experience, you need to dole out the pieces at a reasonable pace. Not too much at a time.

-----
Descriptions: use details to make the world seem bigger
Correspondingly, the more detailed the environment is, the bigger it will feel, in terms of exploration-potential. Five rooms containing one item each will seem from a game-play point of view like less work than one room with several dozen items.

------

Map: use symmetry (3dimensional)
Another useful technique is to create obvious divisions or symmetries in the game world, something to give the player a handle on distinct sets of locations.  Metamorphoses has a very symmetrical map, because it suited the symbolism of the world to make it that way. One of my other works in progress is less symmetrical, but it has sections, what I think of as neighborhoods; each has distinct thematic features of its own.

------

Creativity Example: ask yourself questions

Then there was the business about the moon. The first location I wrote is the one that is still the first room of the game: the terrace, made of moon stone. I was trying to dodge the cliché of having a moonlit terrace, and it occurred to me instead to have a terrace that was glowing of its own accord, instead. That rapidly gave rise to a couple of questions: what kind of world was it in which you could casually travel to the moon and bring back rock from the quarries there? Especially given the other starting idea I had (that the game should be set in a 17th-18th century Western-style society), the answer couldn't have anything to do with space ships in the ordinary sense. Likewise, if the moon was truly glowing of itself, the cosmology had to be different from our own.

This in turn suggested an easy congress between earth and the moon by ship -- so that the moon would be like a colony of an early modern European empire. Correspondingly, it needed to play into the political system: hence, the Moon Minister.

Much of the finer-grained detail developed as I worked on the conversation system. What might one want to ask about? The player would have to have some way of coming to understand this bizarre cosmological system, so unlike our own, and so I created some mythology for it. What stories would people tell themselves about the relations of earth and moon? What boundaries could there be on the King's power? Did his Empire extend forever? Had it always? How was it founded? If there were any foreigners, how were they regarded, and how treated? (I put a few into the game for good measure.)

And then the physical environment. What did it look like? How did it symbolize and embody various aspects of the cosmology in question? (Since obviously this was going to be a symbolism-rich sort of world.) What was the history of the various rooms, and who had been there before, and what memories were associated with them?

------

Creativity: ask yourself questions 

The basic moral of the story is this: you can gather questions around just about any interesting idea you have. Why is this here? Who made it? When did it get here? What is it for? What does it mean? The more you prod at this sort of thing, the more fully the background will develop.

------

Creativity
Invention
The large concepts behind a work of IF may come partly from ideas you have going in, but (if your experience is anything like mine) they will also to a large extent develop from questions you ask yourself afterwards.
Most of the games I've written -- most of the short stories, as well, and the novel, too, for that matter (don't ask) -- have evolved in this way. I have my two or three strong, strange ideas. They don't seem as though they entirely go together, but they're not entirely at war, either. They seem as though they might work.
Then I ask myself questions.

-----

Puzzles: goal: 
The challenges, then, are to build a layout that is easy for the player to understand without extensive mapping; to control access to parts of the geography in a way that sets the desired pace for the game, through puzzles and other design techniques; and to disguise the edges of the map from the player so that he doesn't feel claustrophobic

-----

Goal:
The player's job is to explore the game world as fully and deeply as possible. The author's job is to make that experience easy, fun -- and unavoidable. Engineering a good map is one way to make sure the player will see all the sights and experience the game structure as it was intended.

------

Map: make it manageable
Even a well-designed map can confuse a player who has access to too much of it at a time. My own rule of thumb is that a maximum of six or seven new rooms should be made open at a time

------

Puzzles: Reward the player with abilities
What reward for solving a puzzle? One is obvious: the game state advances a little towards its completion. But the player at the keyboard needs a reward as well: that the game should offer something new to look at. The white cubes in `Spellbreaker', with the power to teleport the protagonist to new areas, are far more alluring than, say, the ``platinum pyramid'' of `Advent', which is only a noun with a few points attached and opens up no further map. -- Graham Nelson, Designer's Manual 4th Edition, 394.

------


Puzzles: Reward the player with plot detail
Plot as Reward I would go a step further than Graham has, and say that, in addition to new territory, a solved puzzle should reward the player with some new information about the plot or new backstory. As the game progresses, it becomes less and less feasible for the solved puzzle to open major new areas -- after all, things are drawing to a close, and the amount of new geography left to explore is diminishing. On the other hand, the closer one gets to the end of the game the more appropriate it is to offer the player major revelations and plot developments.


------

Descriptions of places: encourage exploration by hinting at hidden depth
Descriptions of places: evoke scale, depth, and extravagance by hinting at it with stone toes and ruby studded lace

Goal:
The evocative image suggests something beyond itself in the player's mind. It is a pointer to a hazy-but-fascinating reality that the player may only partly grasp.

Examples:
An enormous stone head, broken in the desert. The bridge built to span an impassible chasm, with technology long ago lost. The scaffolding around the partially-constructed space ship, blocking half the sky of stars. A fragmentary thing evokes its whole; an ancient one, the lost world that created it; an unfinished one, the thing that it is supposed to become. And often those entireties seem more magnificent when they are alluded to than they could possibly be if the player were able to perceive them fully.

Metaphor:
Think of it this way. A statue the size of a skyscraper is just... big. A single stone toe, lying on its side in the dunes, taller than you can reach with your arms extended -- it takes what is colossal about the first image and expresses it in accessible terms. 

Detail:
Saying that something is "stunning" or "immense" impresses less than some more mundane but tangible evidence of size or richness. Magnificent attire is less interesting than a bejeweled costume, which is in turn less colorful than a lace cuff studded with rubies.

People who play IF often have good imaginations, but their imaginings still work best in terms of lengths and sizes they can visualize easily.

------

Descriptions of places: use and abuse physics
Also striking are images that contravene our sense of how the world works, and make us wonder about the alternative reality that allows for it: changes of scale; processes that run more quickly than they do in life, or in the wrong direction, or that are frozen in the middle; doors that open on nothing, objects that hang in midair, inanimate things come to life.

------

Quote:
Particularity is your strongest tool.

------

------

Descriptions - to go deep describe all components and all sub components
It's important to implement your game world with some consistent degree of depth. Implementing deeply and thoroughly (so that everything has a description, and the parts of everything have descriptions, and so on) is perhaps the best way: from a player's perspective, it's excellent to be able to examine not only everything in the description of a room but the subcomponents of the object. It deepens the sense of reality; it suggests that all is not cut out of cardboard and pasted together in haste for our benefit.

------

Descriptions - to go shallow at least recognize all Important nouns
Perhaps instead of attaching subdescriptions to your objects, you have all the subparts pointing back to the same thing ... At least having the important nouns all be recognized is a nice touch, however. 

------

Descriptions - whether shallow or deep be consistent with your level of detail.

You can get away with doing either, but it's best if you do it consistently.  What gets confusing and draws attention is when some rooms are implemented in excruciating detail -- packed with multipartite objects, with all sorts of optional rugs and light switches and irrelevant ceiling panels thrown in -- and then other rooms are half-baked, with only a couple of carelessly constructed objects in them.

------

Creativity: give yourself the real world environment to be creative
The process of writing a game is, at least for me, a fairly intense and immersive one. I make bundles of notes and maps and diagrams. I keep around photographs, or webpages, or bits of poetry, or whatever I'm consulting for inspiration. I stick mood-appropriate music on infinite repeat. Gradually the process starts to feel less contrived and more automatic. Further embellishments volunteer themselves rather than having to be actively fished out of the ether.

------

Quote:
If I'm lucky, those parts add up, in the end, to a coherent whole: a structure that makes intuitive sense, with a consistent mood and no jarring discontinuities, solid and habitable. A world that is no longer an extension of me, but belongs to itself.

Quote:
Between the discipline of creation and the chance of discovery, the world I'm building takes on the qualities of autonomous reality. It feels like a place I've visited.  Sometimes -- most often on the verge of sleep -- I return to one of them as a tourist. I ring the bell; and then I stand, waiting, at the edge of the darkened water.

------


------

------

------

------

San Francisco

1. The temple is a temple of the wisdom of the trees
2. The temple is under construction so there is a huge tarp obscuring most of your view.
3. This allows for puzzles to reveal road signs with arrows that first hint at the existence of one of the the two trees with a sign and then later to reveal an enormous root and then as sign hinting at the existence of the other
4. 
5. As soon as you start the game: an enormous tarp with a tiny sign which requires solving a puzzle to get to it and then you have to wipe the construction dust off of that is anti climactic and says 'under construction' but then as you climb down from your perch on the scaffolding you freeze as the tarp ruffles in a gust of wind (an anemic gust which given the 15lb fabric weight of the tarp had no business being able to ruffle anything) you catch a momentary glimpse of the majesty of the room you are in.  You saw the two trees, one enormous pane of stained glass, and the ceiling which reminded you a bit of the inside of an enormous lego block 
6. At the end of one of the scenes you find out you are actually 150ft below ground (a hook into the next scene)
7. When you finally make it outside (the endgame here) you look back toward the temple and find that it is not there.  You see only a blackened door in a shabbily painted nondescript shack in chinatown.  You walk in and out several times to confirm that you came from the right place.
8. As you step through the first time into the city you are almost hit by a bicycle and smell funny things
9. The reason the ceiling reminded you of Legos is that the ceiling is a Chinatown city block of hollow buildings.
10. There are skylights running down to the stained glass to give the illusion that the temple is

------
