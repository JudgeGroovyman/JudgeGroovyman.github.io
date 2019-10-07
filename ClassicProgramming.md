
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

## Modern AMOS

* The [AMOS Facebook group](https://www.facebook.com/groups/AmosPro/) is quite active in 2019
* There was an [AMOS Professional Showdown](https://datastorm.party/2019/05/26/gerps-professional-amos-showdown/) earlier this year!  


One distant descendent of AMOS BASIC by the same author is called [Clickteam Fusion](https://www.clickteam.com/clickteam-fusion-2-5-free-edition) and is not a dialect of BASIC in any way but fulfills many of the same goals that AMOS did back in the day.

Another distant descendant of AMOS BASIC by other members of the AMOS team are [GameGuru and AppGameKit at The Game Creators](https://www.thegamecreators.com)

The third (and this is only a descendant by rumor) is called [livecode](https://livecode.com)

AMOS Professional has been updated somewhat recently as an [open source project](https://github.com/marc365/AMOSProfessional).

There is an open source reimplementation of AMOS in C++ which even supports AMOS sprite banks. Its called [XAMOS](https://sourceforge.net/projects/xamos/)

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
I got this great book called [Programming Boot Sector Games](https://nanochess.org/store.html) and its certainly the clearest and most accessible assembly language tutorial Ive ever seen.  It also explains exactly how to get your programs running on any computer (hint: use dosbox or boxerapp).  

### Comments about Programming Boot Sector Games ###
I can send these to biyubi@gmail.com when I'm done.
* In section 1.6 the batch file has an error.  It needs '=='
* Example logical1.asm doesn't mention what the output of the program is supposed to be so we dont know if we did it right.
* The commas in the code throughout the book are too small and they look like periods.  My eyes confuse them but can figure it out, but I don't think everyones eyes could and thats such an important punctuation in code I think the font should have been (or should be) slightly modified to have the commas be clearer.  Its not a show stopper and an experienced assembly programmer wouldn't get tripped up by this because they would know 'no one every puts periods there', or something like that, but as a beginner its tripping me up a little bit every 30 minutes or so, in fact most of my errors end up being because I typed a . instead of a , and even on second inspection my eyes dont always see that distinction.









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

