
# BootBasic #


## Installation ##
The repo is easy to [clone from github](https://github.com/nanochess/bootBASIC).   

## Running it in QEMU ##
See [QEMU in Classic Computing](ClassicComputing.md#QEMU) for info on getting the emulator setup.  

I followed all the instructions (including getting nasm and running those commands) to run it with qemu but it wouldn't boot from the floppy image. They say it will run in dosbox so lets try that.  
 
See Update in the next section.

## Running it in DOSBox ##
UPDATE: I got it working in DOSBox and then I realized something, it was working in qemu all along!  Its just a no holding your hand kind of program so I just saw a prompt and thought it was broken.  It probably worked the first time I tried it and I could have been using it for the last half hour :) 

To actually get it running in dosbox you first have to mount a local drive in dosbox to be able to get to it
` mount f f:\Unity\bootBASIC` then execute the com file.

For mac use [Boxer](http://dosbox.com) because trying to run dosbox on mac there are a few problems (primarily that theres no paste and or because I cant trigger the insert key) but 


## Doing useful things with it ##
well hello world is just `print "Hello, World!"

heres a program that shows some of the unique syntax
```
5 i=5
10 print "Hello, World!"
20 i=i-1
30 if i-0 goto 10
```
What do you think that does?


# AMOS
Given the computer I had and the skills I had as a kid this was the second most important programming language for me starting in 1992.  Heres a [short history of AMOS](http://www.powerprograms.nl/amiga/amiga-all-about-amos.html)

* Archive.org has the manuals to [all versions of AMOS](https://archive.org/search.php?query=AMOS%20Manual) can be found.
* A book called [Amiga Game Maker's Manual](https://computerarchive.org/files/comp/applications/amiga/manual/Amiga%20Game%20Makers%20Manual%20-%20With%20AMOS%20Basic%20-%20Manual-ENG.pdf) is all about programming with AMOS. 
* A book called [Ultimate AMOS](https://amigasourcecodepreservation.gitlab.io/ultimate-amos/) from 1994 is on gitlab now
* A [forum about AMOS Development](https://www.ultimateamiga.com/index.php?PHPSESSID=s1rjf9gaoi5el4c6c4ed0egt6h&board=312.0) has trickles of activity and even an AMOS Pro v2.10 alpha release
* A [github](https://github.com/AMOSFactory/AMOSProfessional) last updated in 2017 with very few commits but which was being worked on by someone at that forum at ultimate amiga
* A very old packaged [AMOSPro installer for windows](http://eab.abime.net/showthread.php?t=60144) where the idea was to distribute AMOS with AROS and therefore have a completely free development environment that could be installed on windows.
* [AMOSTools](https://github.com/kyz/amostools) Tools that let you extract the contents of .amos files
* A [Wiki about AMOS](http://www.amigacoding.com/index.php/Main_Page) (and other Amiga languages) Development 
## Modern AMOS

* The [AMOS Facebook group](https://www.facebook.com/groups/AmosPro/) is quite active in 2019
* There was an [AMOS Professional Showdown](https://datastorm.party/2019/05/26/gerps-professional-amos-showdown/) earlier this year!  


One distant descendent of AMOS BASIC by the same author is called [Clickteam Fusion](https://www.clickteam.com/clickteam-fusion-2-5-free-edition) and is not a dialect of BASIC in any way but fulfills many of the same goals that AMOS did back in the day.

Another distant descendant of AMOS BASIC by other members of the AMOS team are [GameGuru and AppGameKit at The Game Creators](https://www.thegamecreators.com)

The third (and this is only a descendant by rumor) is called [livecode](https://livecode.com)


There is an open source reimplementation of AMOS in C++ which even supports AMOS sprite banks. Its called [XAMOS](https://sourceforge.net/projects/xamos/)

## Running AMOSPro in 2019 ##
It seems to run perfectly from the latest github master branch files (there are already built binaries in there in an AMOS directory)

### Tips ###
If you want to switch back to workbench hit the WB at the top right, then when in the workbench to switch back to AMOSPro press amiga+a (windows key in winUAE)

## Building AMOS Pro from Source in 2019 ##



### Adventures in OS3.1 ###
Trying to compile in OS3 I had much more luck and it compiled through many sections but failed on clib.  It said Loading LEqu.s, loading +CLib.s, c/Check_CLib failed returncode 20.  this happens on my A1200 and A4000 configuration

#### Releases didnt work ####
The source release version didnt work because none of the scripts are executable.  I retried the source version but only unzip on the amiga side instead of unzipping on windows but this didn't change anything (scripts still not executable)

The core release version didn't work because it expected volume AP2 in any drive.  

### Figuring out Git Problem ###
I noticed that the git zip file compiled but the git clone didnt.  Why not?  Well after several diff tools I found out it is indeed line endings where the unix versions of the files worked and the windows did not.  

1. How to use git on windows but extract the unix versions of the text files or
2. How to convert them and then 
3. Try the original source release again because with this fix it might actually work just fine.  

### Next Steps ###


Now on to several things
1. DONE Cloning the latest git and executing it with that 
2. DONE With the properly configured repo I did a checkout on the ref id of the source release and it didn't work because nothing was executable but not because of line endings but because Make_Labels failed returncode 20 or File not found.  I presume their protections were different but I tried protect +e on everything.
3. DONE With the properly configured repo I did a checkout on the ref id of the core release but then it demanded AP2 so `assign AP2: /AMOSProfessional` and then it built successfully!
2. DONE Delete the AMOS executables before building and see if it makes new ones.  Result: AMOSPro is there but compiler shell disappears
3. DONE Try protect +s instead of -se 
3. DONE Try protect +e instead of -se
3. DONE Try protect +se instead of -se
3. Get OS3.1.4


### I FIXED IT!!! ###
I feel like a genius!  I did some digging through the code and figured out where it was dying it was looking for `+CLib.s` so I went and looked for that file to be in the same folders that the other files it was looking for were located and it wasnt there!  I hoped I had come upon a solution and when I found it and copied it in then it started working!   YES `execute aall` totally works now!!!  Also it explains why it would have worked for him because in his folder this file was undoubtedly already copied over.



#### How to fix ####

Two ways to fix it:
1. Copy (not move) `compiler/+CLib.s` to the main build directory
2. Move `compiler/+CLib.s` to the main build directory and then update the two paths in `compiler/aclib`

to test whether your fix worked type `execute compiler/aclib`

If you want to dig deeper and try to fix the `c/Check_CLib` then open it in AMOSPro (theres a working version in the latest master branch in the AMOS folder before you even compile)
to compile `c/Check_CLib` type `execute atools`


### I fixed the scripts not executable problem too!!! ###
It was a unix windows line ending problem and it seems that if we were to add a .gitattributes to the AMOSProfessional folder that had just one line it in then no matter how the users git client is configured (which mine wasn't configured) it will override and use only unix line endings throughout.  


```
* text=auto eol=lf
```

Adding something like these lines would just help it figure things out
```
*.iff binary
*.o binary
*.AMOS binary
*.Bin binary
*.bin binary
*.Lib binary
*.lib binary
*.Abk binary
*.anim binary
*.Anim binary
*.info binary
*.prefs binary
bin/* binary
c/* binary
*.s text=auto eol=lf

```



### New email ###
I know its been a while since our last correspondence but yesterday I was finally ready to sink my teeth into AMOSPro and hooray! I got it built but there was a problem and I had to use a workaround so I wanted to get your input about next steps.

Problem and workaround:
Using the master branch zip file and typing `execute aall` it built for a while but died when the scripts were trying to `execute acomp` with this error: `c/Check_CLib failed returncode 20`.  

My workaround: I finally figured out that if the file `+CLib.s` is in the top level build directory everything builds!  

What should we do?
Option 1: We could move this file to be permanently in the top level directory and change two lines in `compiler/aclib` to point back to that top level directory.  I have gotten this approach working consistently.
Option 2: (this is over my head) We could somehow change the `c/Check_CLib.AMOS` to work with the location of the file `compiler/+CLib.s`, however this is over my head.  I did attempt this in the AMOS source for `c/Check_CLib.AMOS` but couldn't get it to work.
Option 3: Other Options?

What do you recommend and how can I help?  Thanks for doing all of this.  Its really cool.

Thanks,
John

P.S. I'm also going to try Francois Lionet's new AMOS 2 soon to see what its like.  I did become a patreon patron of that project last night because it looks really cool. 



P.S. Some history of what I tried in case you're interested:
* I accidentally (long story) got legacy OS3.1 installed rather than OS3.1.4 and it is working well but I will probably get OS3.1.4 installed sometime soon.
* I couldn't get either of the releases to even begin building on OS3.1
	* My success above came using a zip of the latest files from the master branch.  
	* the `sources release` as it is has windows CRLF settings so none of the scripts will execute on the Amiga side.  This initially happened for me with the latest master branch too and I think if we added just one line to a .gitattributes file we wouldn't have this problem.
	* the `core release` immediately demanded volume AP2 but when I assigned that to the AMOSProfessional directory it built just fine.
	
### For my debugging ###
Its dying on execute 

 recompiles the c/check_clib

### Misadventures in OS4 ###
 
Big Update (10/8/19): I don't think I was ever supposed to (or able to) get it compiling in OS4.1.  I think that was a mistake in how I read his emails.  Oops.  

(10/7/19)

AMOS Professional has been updated somewhat recently (2017/18) as an [open source project](https://github.com/marc365/AMOSProfessional) and I contacted the dev and am going to try to build it.  First I have to get it into my AmigaOS4.1 environment (since thats what the email that I got from the maintainer said to do) and I'm using local FTP for that.  I might try building it on the RAM disk to speed up the process, the disadvantage is if anything goes wrong and I have to restart I lose it all :(  No I dont think disk access is going to be the bottleneck here so I'm not going to risk it.

I did what his instructions said in an email: download the releases and then go into the directory and type execute aall but the first thing it said was "ALib: file is not executable" and when I looked through the scripts I found that they were nested and none of the scripts had been marked executable.  I'm not sure if thats even possible to maintain the executable status in a zip file so maybe this is normal.  Anyway I had to just type `protect <file> -se` s for script e for executable.  for all of the things in all of the scripts.  Wait maybe tar.gz will work better?  let me try that before I go much further.  Update: The tar did not work better.

Once I finished making a bunch of them executable, execute aall ran but it also finished almost instantly making me think it didnt do anything at all.  It would be hard for me to believe that it had done all of the compiling and linking in an instant like that.  

Ok it looks like there have been a lot of changes in the last few years since the releases so I'm going to grab the latest and see what happens.  Ok from that I got just a few lines of execution and then a guru meditation in OS4 which locked up the terminal. 

I tried the core release in OS4 (immediate shell GURU Meditation).  I tried to build the latest master in OS4 in some kind of 68k compatibility mode but couldn't figure out how.

I even built the latest github master branch on OS3.1 then transferred them to OS4 and they didnt execute then transferred them back to OS3.1 and they built and then tried them again on OS4 and this time got a guru meditation.


# BASIC
Fun Trivia: BASIC stands for Beginner's All-purpose Symbolic Instruction Code

[A modern video about the basics of BASIC](https://www.youtube.com/watch?v=seM9SqTsRG4) on one of my favorite classic computing channels: [The8-BitGuy](https://www.youtube.com/channel/UC8uT9cgJorJPWu7ITLGo9Ww)
[101 Basic Computer Games](http://www.vintage-basic.net/games.html)

## Boot Basic ##
 This is an 'integer basic' interpreter that runs in the boot sector of an old pc.  

## QBasic
Back in the day (the 80s and 90s) QBasic was included as a part of MS-DOS and/or Windows so a lot of people had automatic access to it so for a lot of people it was how they first cut their teeth on programming, or how they made their computer do something simple.
(or how they played  [gorillas](https://gist.github.com/caffo/1326838) or nibbles)

QBasic was based on Quickbasic which only run in dos (or [dosbox](https://www.dosbox.com), and [here's how to do that](https://www.qbasic.net/en/qbasic-tutorials/dosbox/qbasic-dosbox-1.htm)) but can be acquired at [qbasic.net](https://www.qbasic.net/en/qbasic-downloads/compiler/qbasic-compiler.htm).

There are a number of programs available online for Quickbasic [Games ](https://www.qbasic.net/en/qbasic-downloads/games/action-1.htm), 
[Tools](https://www.qbasic.net/en/qbasic-downloads/tools/graphical-effects.htm), and many more at the top of the page.

### Modern QBasic
[This is QB64](https://www.qb64.org) a cross platform, modern, open source, and extended BASIC (which even has OpenGL) which retains [high compatibility](http://qb64.wikia.com/wiki/Differences_from_QBasic_and_QB4.5) with classic QBasic software and even compiles QBasic programs into native binaries.  It apparently even has a [WYSIWYG GUI Toolkit called Inform](https://www.qb64.org/inform/) and a [Debugger called vWatch64](https://www.qb64.org/vwatch/)

Another option is [Freebasic](https://www.freebasic.net)

### QBasic Related
[QB45](https://qb45.org) is a site full of QBasic resources.  It's named after the version number of the last version of Quickbasic which was released in 1988.  There is loads of QBasic software here such as [these action games](https://qb45.org/files.php?cat=3), [these graphics demos](https://qb45.org/files.php?cat=8), and [these platform games](https://qb45.org/files.php?cat=4)

## GW-Basic
QBasic was based on Quickbasic which was based on GW-Basic which was based on MBasic which was based on Altair BASIC.

There are a bunch of programs compatible with GW-Basic at this [blogspot site](http://gwbasicprograms.blogspot.com/p/gw-basic-programs.html), and at the [Back To Basics page](http://peyre.x10.mx/GWBASIC/index.htm), 

A 1987 version of the [GW-Basic users manual](https://hwiegman.home.xs4all.nl/gw-man/index.html)

### Modern GW-Basic
There is a modern verison of GWBasic called [PC-Basic](https://robhagemans.github.io/pcbasic/) which runs on any platform which runs python.  Among many other notable features it has support for reading programs from wav files made from PC casettes!  There are a bunch of reportedly compatible programs at [oldskool.org](http://www.oldskool.org/guides/tvdog/basic.html), since they are Tandy 1000 programs and PC-Basic is compatible with Tandy 1000 basic.

## Altair BASIC
Going even further back Microsoft had a history with BASIC since they were one of the original popularizers of BASIC.  An implementation of BASIC that was their [first commercial application](https://en.wikipedia.org/wiki/Altair_BASIC) (for the MITS Altair) was their first commercial product.

#### Paul Allens Airplane panic
When Bill Gates and Paul Allen wrote Altair Basic they didnt have an Altair machine to test it on all they had was a simulator (which they wrote) but they wanted to show the MITS company (who made the Altair) what they had done so they could start selling it.  Paul Allen took the tape to MITS but realized as the plane was landing that they didnt have any way to load it from the tape.  Back then you had to have a program to load any other program and without that 'bootstrapper' there would have been no way to run their software.  He wrote it by hand in assembly language on as the plane was landing. I believe it was 70 instructions.  The miracle is that it all worked!?!

[How that famous demo might have gone down](https://www.youtube.com/watch?v=2wEyqJnhec8)

#### Further History
[How the MITS Altair bootstrapper worked](https://www.reddit.com/r/learnprogramming/comments/4oarlf/eli5_how_did_bill_gates_and_paul_allen_create_the/)


## Small Basic ##

[Small Basic](https://smallbasic-publicwebsite.azurewebsites.net/) is a pretty cool microsoft developed (although not heavily marketed or supported) basic thats made for kids.  There is a notable [tetris game](http://smallbasic.com/program/?Tetris), a [cute sokoban](http://smallbasic.com/program/?Soko) game with great graphics, and a [cool blinking eyes example](http://smallbasic.com/program/?GHR094-0), and [many more](https://smallbasic-publicwebsite.azurewebsites.net/resources), and all of the source is included and generally seems quite readable.  The tetris game was really good imho.


# C
Derivatives of C are modern languages but C was invented in 1972 so I think its legit to consider it 'classic' or 'modern'.

[A set of simple C Programs](https://www.studytonight.com/c/programs/)
[A second set of simple C Programs](http://blog.kodegod.com/learn-programming/101-programs-to-build-your-programming-logic-using-c-programming/)

# Assembly
(also see Programming.md Assembly On Modern Mac)

## Assembly on C64 ##
The [8 bit show and tell channel](https://www.youtube.com/channel/UC3gRBswFkuteshdwMZAQafQ) has a lot of videos about commodore 64 assembly and it is pretty amazing what he got the hardware to do back then.  


## Assembly on Dos ##
I got this great book called [Programming Boot Sector Games](https://nanochess.org/store.html) and its certainly the clearest and most accessible assembly language tutorial Ive ever seen.  It also explains exactly how to get your programs running on any computer (hint: use dosbox or boxerapp) and all of the programs work really well. 






# Classic Games


# Magazines
## AMOS Newsletter
This was a newsletter about the Amiga programming language AMOS.  

[One source of AMOS Newsletter](https://www.amigacoding.com/images/d/da/Official_Amos_Newsletter_Issue_1.pdf)
### '10 liners'
One of the most interesting aspects of this newsletter was a feature which naturally highlighted the strengths of AMOS.  The 10 liners were short programs which could be typed in from the newsletter.  I haven't tried typing any in but it kind of blows my mind!?!

I believe to get most of these to work you will have to know something about Bobs which on the Amiga are analogous to sprites.  You can learn more about those using the 

[Example of a 10 liner](https://archive.org/details/TheOfficialAMOSClubNewsletter/page/n13)

[Here's the full text of a different 10 liner](https://archive.org/stream/TheOfficialAMOSClubNewsletter/The%20Official%20AMOS%20Club%20Newsletter%20Vol%202%20Issue%204_djvu.txt)


# Type In Programs
## AMOS Newsletter '10 liners'
See above
## 101 Basic Computer Games
I remember getting this book around 1993 and loving the idea of it so much.  It was actually a relatively mature book by that time.

[A March 1975 version of 101 BASIC Computer Games](http://www.ccapitalia.net/descarga/docs/1975-101-basic-computer-games.pdf)

[A set of scans of the book and source code downloads](http://www.vintage-basic.net/games.html)

[QBasic Compatible source code along with some history of BASIC](http://www.classicbasicgames.org)

[Heres the whole PDF](https://annarchive.com/files/Basic_Computer_Games_Microcomputer_Edition.pdf)

## Books full of BASIC programs
In addition to 101 Basic Computer Games above there are dozens of other books full of BASIC computer programs.  One way to find these is to search for BASIC programs at [Archive.org](https://archive.org/search.php?query=basic%20programs).  

Additionally if you make the search computer specific you get even better results.  For example: [Search for C64 BASIC Games](https://archive.org/search.php?query=c64%20basic%20programs)

## Compute's Gazette

