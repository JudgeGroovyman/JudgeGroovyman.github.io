# Apps #
- [Making an event app ](https://apptooltester.com/how-to-create-an-event-app/)

# Projects #
1. Assembly Boot Sector Book
2. C64 programming from that guys assembly tutorials on YT
3. Make a tetris game in Python (Pygame and then with Pyglet)
4. Make a tetris game in C with SMFL (then in pure C# in Visual Studio)
5. Make a synthesizer using the simple fluid synth API in C
6. Write a game directly for [linux framebuffer](http://betteros.org/tut/graphics1.php)
7. Write a game direclty on video hardware for [raspberry pi] (http://raspberrycompote.blogspot.com/2012/12/low-level-graphics-on-raspberry-pi-part_9509.html)
8. Write a [game for DOS in C](https://nullprogram.com/blog/2014/12/09/)
9. [Invent your own computer games with Python](http://inventwithpython.com/invent4thed/)
10. [Cracking Codes with Python](https://inventwithpython.com/cracking/)
11. [Making games with Python and Pygame](https://inventwithpython.com/pygame/)
12. Unity Virtual Reality Projects - humble bundle book
14. Unity Game Development Blueprints - Humble bundle Book
15. Discover Unity Game Development - From Zero to 12 Games Humble Bundle Book


# Smalltalk #
I met Alan Kay once.  It changed my life. 

1. [Pharo](https://github.com/pharo-project/pharo) Modern Smalltalk.  Updated 17hrs ago.
2. [Amber.js](https://amber-lang.net) A language and live environment built for the javascript runtime.  Updated in the last few weeks.
3. [Seaside](http://www.seaside.st) For sophisticated Web applications in Smalltalk.  Updated in the last few months.  


# Assembly #
## Assembly onModern Mac ##
This is actually pretty tricky to do assembly on modern systems unless you really know what you're doing.  

* I got a hello world going from [James Fishers tutorial])
https://jameshfisher.com/2017/02/20/macos-assembly-hello-world/) but then I saw this [nasm tutorial](https://cs.lmu.edu/~ray/notes/nasmtutorial/) and was intrigued by the slight differences in the hello world code.  
* I think you could get a lot of information from these commands and operands lower down a bit in [this nasm tutorial](https://cs.lmu.edu/~ray/notes/nasmtutorial/) it focuses on the details of the hardware and the most basic assembly commands and also has some mac specific details and a mac specific averaging program at the bottom that takes input and makes output.
* I heard earlier today that really assembly is about the details of the hardware as much as the language.  
* Samuel Evans-Powell figured out some things about [learning NASM on macOS](http://sevanspowell.net/posts/learning-nasm-on-macos.html) like about syscalls and the differences on mac and linux and also in that article he talks about linking c and assembly, and he talks about not absolute addressing on mac osx, and also about padding the stack frame.  It suggests using gcc to link instead of ld which lets you use the c standard library.  
* Here is a [Brainfuck Interpreter](https://www.kylem.net/programming/bf_interp.html) in x86-64 assembly
* Here are some 8086 programs that I can probably get running like I did with nasm on the mac above or with the boot sector approach

### Linking with a C Library ###
I wanted a super simple C Library so I'm going to [write one myself](https://www.quora.com/How-do-you-make-your-own-libraries-in-C-programming).  I got it working and was able to call a super simple C library that I made (that just printfs the input number) from assembly.  It sends a number as a parameter but I dont understand the assembly enough yet to decide how to tell it to send an integer.  I got it sending a string (char *) through to the C code though and it worked great!


## Assembly on Modern Linux ##
* This [nasm tutorial](https://cs.lmu.edu/~ray/notes/nasmtutorial/) seems really good and also has some mac and win specifics but is mostly linux specific.
* Running 

# Bare Metal #
* This guy [runs some programs on bare metal](https://stackoverflow.com/questions/22054578/how-to-run-a-program-without-an-operating-system/32483545#32483545)


# C #
* [Freestanding C programs](https://nullprogram.com/blog/2016/01/31/) on windows.  this guy wrote some C programs for windows on linux with no external libraries or dependencies except operating System DLLs.  He also wrote some opengl style programs in tiny sizes for DOS (and he wrote those in linux too)

# C++ #
* To make SDL style grpahics with C++ (bindings for C and C# and others) use [SFML](https://www.sfml-dev.org/faq.php#grl-whatis)

# Javascript

[A set of simple Javascript programs](https://github.com/NishiGaba/100-Basic-Javascript-Programs)

# Programming Training
Programming training comes in 1000 varieties so this section is for sites that are relatively general:

* [Study Tonight](https://www.studytonight.com/) offers study resources on a number of languages including tutorials & explanations, hundreds of [example programs](https://www.studytonight.com/c/programs/), [tests you can take](https://www.studytonight.com/tests/?/?subject=c) and [Interview Questions](https://www.studytonight.com/flashcards/Cpp/) to help you sharpen your skills.

# Game Development #
Unity, Unreal are the two big engines. Here are a few more intriguing ones:
1. [Raylib](https://www.raylib.com/examples.html) (Straightforward C and OpenGL library with tons of language bindings and lots of capability)

# Makefiles #
[Super simple makefile](https://spin.atomicobject.com/2016/08/26/makefile-c-projects/)
