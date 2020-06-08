
# BBSing #
I have fond memories of playing LORD on BBSs as a kid.  I remember never being able to get ANSI graphics working on my Amiga and always thought that it was because the Amiga was inferior. I found out recently that the Amiga had the best ANSI color support of any computer but I dont know why I didn't figure this out back then or how I could do it today.  

Clients

* [SyncTerm](https://syncterm.bbsdev.net) real clumsy but works really well with beautiful ANSI (rumored to be the best ansi support possible) interesting that I dont know how to paste into this program.  One nice feature is it will store your bbs passwords so assuming they aren't of great security importance to you (since they are sent unencrypted) this is convenient.
* [FTelnet](http://my.ftelnet.ca/#) This is a close second for best telnet support.  Its easier to setup too although syncterm is lightweight and not hard at all.  OMG When there are graphics bigger than one screen the scrolling is incredibly slow!
* Mac Terminal See near the end of [Pacbillys video](https://www.youtube.com/watch?v=Omets00iLWw) to see how to configure mac terminal.  It worked for me however some of the graphics at stab.net were pretty clunky and like showing many wrong characters so they only slightly resembled graphics.  The game functions were minimally playable (Like I did as a kid on my Amiga) but the graphics were not functional

Some BBSs
 
* bbs.Lunduke.com [See Pacbillys video on this LORD game](https://www.youtube.com/watch?v=Omets00iLWw) temporarily down as of May 16 2020
* lord.stabs.org [Stabs](https://lord.stabs.org) This one you can play at that website [on this page](https://lord.stabs.org/playlord.html) but you have to create your character using telnet.  It doesnt take ^H for delete.  It doesnt 'know' the terminal type of syncterm so its not showing me any graphics and wont actually run the game atm.
* towel.blinkenlights.nl Full star wars movie in simple ascii art.  Unbelievable
* [Mewbies](http://mewbies.com/acute_terminal_fun_telnet_public_servers_watch_star_wars_play_games_etc.htm) A bunch of BBSs MUDs and MUCKs 
* [telnetbbsguide](https://www.telnetbbsguide.com/bbs/vikis-bbs/) this is a really slow website with a bunch of telnet BBSs listed

LOTGD

Of course if you want to play LORD without the telnet and with a frankly better snappier and more reliable interface see The Legend of the Green Dragon
* [Original Legend of the Green Dragon Server](http://lotgd.net/home.php?)
* Many more are out there and its easy for servers to configure the game with more turns and many other interesting features




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
