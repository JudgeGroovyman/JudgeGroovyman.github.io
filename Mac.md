# Catalina #
To get Unity games working on Mac Catalina

I setup a shortcut to replace 
macfix
with
1. `chmod +x Clone-Kitchen.app/Contents/MacOS/*` removes the "this application can’t be opened" problem
2. `Right click -> Open -> Cancel -> Right Click -> Open -> Open` to get around the security of the mac gatekeeper


## Cannot Open ##
I just had to run this command:

chmod +x loopfieldMacOS.app/Contents/MacOS/*​

​and then it worked like a charm.


## Gatekeeper ##
Also theres the Normal Mac Gatekeeper Workaround

Just like with every other game like this on MacOSX I had to do the usual: rightclick->open->open to get around the MacOS Gatekeeper.

Protracker2 clone says "To be able to actually run the program, you need to right click the .app/program and click "Open".
This is only needed once, you can open it like normal after this."




## Translocated ##

Also https://16-bits.org/pt2.php this program when you get it running says "Critical Error - the program was translocated to a random sandbox environment for security reasons and thus it cant find and load protracker.ini.  Dont worry this is normal.  To fix the issue you need to move the program/.app somewhre to clear its QTN_FLAG_TRANSLOCATE flag." Then it tells you to move it somewhere else and back. "This is not my fault its a security concept introduced in macos 10.12 for unsigned programs downloaded and unzipped from the internet."

# External Keyboard
### Home and End buttons
A [Five minute fix](https://www.maketecheasier.com/fix-home-end-button-for-external-keyboard-mac/) for the home and end buttons

# Sidecar #
Lots of reports of it freezing after 30min. Mine freezes after 1-5min.
Possible workarounds:
1. reset it by Hide and unhide sidebar
2. Possibly fixed (Cross fingies) by either leaving the sidebar on and or turning off screen rotation Update: 1h later this is still going strong.  Ok after like 90 min it locked up again
3. Rumors say usign cable is more reliable it wasnt for me
4. Rumors say you can do some kind of underlying data reset in your mac account to help. 

Next Steps: Try using a brand new account with it for a little while. if it works perfeclty for hours wiht a brand new account then I know its something in my account.

Interesting side effect: Netflix wont run if you have sidecar enabled.  its black even on your main screen.  Theory: It detects something like some kind of screen copy software that streams the display over and goes black to prevent piracy.  Workaround: Chrome works.  Safari doesnt work.  Chrome must sense those things differently.


# Software #
1. [Paintbrush](Paintbrush.sourceforge.io) is like MSPaint for the mac

# Diff Tools #
1. Meld
2. Filemerge (included with mac)

# Audacity #
Well it works but recording is a problem but there are a bunch of threads showing that in Catalina you have to run it  from the terminal

1. https://forum.audacityteam.org/viewtopic.php?f=47&t=107162
2. https://forum.audacityteam.org/viewtopic.php?f=47&t=105586&start=60

I was able to record with it when I launched it from the terminal.  It sure seems like its running slowly tho

Perhaps its not an issue with the latest version when using the [provided instructions](https://www.audacityteam.org/download/mac/)


# Video #
I've been using Smart Converter for video compression for a long time but ... 
Handbrake lets you also change the resolution which makes the videos WAY Smaller

# Terminal #
Need a way to get between the folder you are in right now in the terminal and in the finder and vice versa

actually you need a way to open a new finder window in the same folder instantly too but thats not a terminal issue
