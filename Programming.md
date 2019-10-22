
# Music Programming #
* Sonic Pi is an application with a music synthesizer programming language with tons of great features in the IDE and built in tutorial and documentation.

# Assembly on Modern Mac #
This is actually pretty tricky to do assembly on modern systems unless you really know what you're doing.  

* I got a hello world going from [James Fishers tutorial])
https://jameshfisher.com/2017/02/20/macos-assembly-hello-world/) but then I saw this [nasm tutorial](https://cs.lmu.edu/~ray/notes/nasmtutorial/) and was intrigued by the slight differences in the hello world code.  
* I think you could get a lot of information from these commands and operands lower down a bit in [this nasm tutorial](https://cs.lmu.edu/~ray/notes/nasmtutorial/) it focuses on the details of the hardware and the most basic assembly commands.  
* I heard earlier today that really assembly is about the details of the hardware as much as the language.  
* Samuel Evans-Powell figured out some things about [nasm on the mac](http://sevanspowell.net/posts/learning-nasm-on-macos.html) like about syscalls and the differences on mac and linux and also in that article he talks about linking c and assembly, and he talks about not absolute addressing on mac osx, and also about padding the stack frame.  It suggests using gcc to link instead of ld which lets you use the c standard library.  

### Linking with a C Library ###
I wanted a super simple C Library so I'm going to [write one myself](https://www.quora.com/How-do-you-make-your-own-libraries-in-C-programming).  I got it working and was able to call a super simple C library that I made (that just printfs the input number) from assembly.  It sends a number as a parameter but I dont understand the assembly enough yet to decide how to tell it to send an integer.  I got it sending a string (char *) through to the C code though and it worked great!

# Javascript

[A set of simple Javascript programs](https://github.com/NishiGaba/100-Basic-Javascript-Programs)

# Programming Training
Programming training comes in 1000 varieties so this section is for sites that are relatively general:

* [Study Tonight](https://www.studytonight.com/) offers study resources on a number of languages including tutorials & explanations, hundreds of [example programs](https://www.studytonight.com/c/programs/), [tests you can take](https://www.studytonight.com/tests/?/?subject=c) and [Interview Questions](https://www.studytonight.com/flashcards/Cpp/) to help you sharpen your skills.

# Game Development #
Unity, Unreal are the two big engines. Here are a few more intriguing ones:
1. [Raylib](https://www.raylib.com/examples.html) (Straightforward C and OpenGL library with tons of language bindings and lots of capability)

Unity Versions Installed:
5.0.0f4
2019.2.8f1
Some 2018 version

# Makefiles #
[Super simple makefile](https://spin.atomicobject.com/2016/08/26/makefile-c-projects/)


# Merging #

## Windows ##
* WinMerge (FOSS) 3 way, directories, images
* Meld (FOSS) 3 way, directories, nice graphics to show the merges, written in python?  The file selector boxes are unfamiliar (though not problematic in any way)   it wont let you reload the diff that you did (like when you changed something which happens a lot) instead you have to start a new diff.  It didn't identify carriage return differences which winmerge did identify instantly.  This could be a blessing or a curse because some people dont want those to be identified, however I didn't see that in the options for this program.
