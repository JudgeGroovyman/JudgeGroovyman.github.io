

# Emulating old systems #

## QEMU ##
One way is with QEMU.  Install it and then add the path to windows environment variables and you can boot up linux isos or whatever.

This video [Installing and setting up qemu on windows 10](https://www.youtube.com/watch?v=al1cnTjeayk) describes how to install it and get linux running in it.

### Linux Iso ###
To get it running with a linux iso
``` 
qemu-system-x86_64.exe -boot d -cdrom .\alpine-standard-3.10.2-x86_64.iso -m 512
```

## Dosbox ##
[Dosbox](http://dosbox.com) works great on windows.
[Boxer](http://boxerapp.com) is the mac version which works great on mac.  


## VirtualBox ##
This is faster and better for x86 virtualization.  Qemu has way more architectures.

# Magazines #
There is so much commodore magazines and reference material at the life of kenneth its insane.  Commodore 64 c64 technical stuff and fun popular stuff too.
* [The Life Of Kenneth](https://mirror.thelifeofkenneth.com/sites/)
* [DLHs commodore archive](https://mirror.thelifeofkenneth.com/sites/commodore.bombjack.org/) which is related to the life of kenneth
* [Amazing archive of Amiga Magazines](https://mirror.thelifeofkenneth.com/sites/commodore.bombjack.org/amiga/amiga-magazines.htm)
* [Archive.org](archive.org) has lots of the old magazines
* Many issues of Amiga World are available [here at archive.org](https://archive.org/search.php?query=amiga%20world)


# For More #
Also see ./Amiga.md


# Classic Computing Channels #
* [8 Bit Show and Tell](https://www.youtube.com/channel/UC3gRBswFkuteshdwMZAQafQ) he has a great style where he shows everything with his hands and always has some cool retro props in the frame.  Hes really savvy about 8 bit commodores and shows some great assembly and cool hardware cartridges and stuff.  One of my favorites was when he had a guest on and they [showed the C64 game Invader](https://youtu.be/SJ81YD9Ebec) that they made in assembly and went through how the code worked. 


# C64 Assembler #
After giving up trying to run the C64 emulator on AmigaOS4 (which was a fun idea and shouldn't have been that big of a deal tbh) (see Amiga.md for more) I am doing it on winVice now and its going smooth.  it types fast, loads decently fast, etc.  The keys are mapped intelligently (Although I dont know how petscii would work on here).  Ok it was really hard to find the back arrow key which is top left of c64 keyboard.  I didnt find anything on the web telling me (not saying its not out there somewhere) but I got a clue and tried some of the insert block of keys and it was the end key.  Then to kill the program I hit run/stop and Restore at the same time (which was esc and pgup) then I typed sys 32768 again and it opened the assembler with my program still loaded!
After giving up trying to run the C64 emulator on AmigaOS4 (which was a fun idea and shouldn't have been that big of a deal tbh) (see Amiga.md for more) I am doing it on winVice now and its going smooth.  it types fast, loads decently fast, etc.  The keys are mapped intelligently (Although I dont know how petscii would work on here).  Ok it was really hard to find the back arrow key which is top left of c64 keyboard.  I didnt find anything on the web telling me (not saying its not out there somewhere) but I got a clue and tried some of the insert block of keys and it was the end key.  Then to kill the program I hit run/stop and Restore at the same time (which was esc and pgup) then I typed sys 32768 again and it opened the assembler with my program still loaded!
