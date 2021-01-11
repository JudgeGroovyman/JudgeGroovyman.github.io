# Catalina #
To get Unity games working on Mac Catalina

I setup a shortcut to replace 
macfix
with
1. `chmod +x Clone-Kitchen.app/Contents/MacOS/*` removes the "this application can’t be opened" problem
2. `Right click -> Open -> Cancel -> Right Click -> Open -> Open` to get around the security of the mac gatekeeper


What about "DungeonGenerator is damaged and cant be opened you should move it to the trash"?  The above ideas dont fix it.  I also had that problem with the mac version of aoz studio
## Perfect instructions on getting mac apps working ##

Update:
``Follow these simple steps to get AmigaLive with the "FS-UAE Launcher" properly running.

Click "OK" if you are prompted to give access to files for "AmigaLive" or "FS-UAE Launcher".
You can also enable this under "System Preferences", "Security & Privacy", "Privacy", "Files and Folder" and enable access to both "AmigaLive" and "FS-UAE Launcher"

-----------------------------------App Translocation / Gatekeeper Path Randomization-----------------------------------
Starting with macOS Sierra (10.12), any application distributed outside the Mac App Store runs from a randomized path.
This causes AmigaLive and FS-UAE Launcher not to function properly until you perform either of the following solutions.

Solution 1 (Simple):
These steps can be performed only using "Finder" or your desktop environment without involving any other file-manager.
Use "Finder" to drag/move the "AmigaLive/AmigaLive.app" and "AmigaLive/FS-UAE/FS-UAE Launcher.app" to the desktop
Then use "Finder" once more to move them back in their original location.

Launch the AmigaLive.app and select "Open" when you get the prompt asking "Are you are sure to open it?" 
Once opened, go to the top menu-bar and select "Help" - "Check FS-UAE Launcher/Version" and click "Open" 
Once the "FS-UAE Launcher window" is opened, you can close it and you are ready to go.



Solution 2 (Advanced):
This solution requires your sudo admin password and performing the following commands through a terminal window:
sudo xattr -r -d com.apple.quarantine "/path-to-AmigaLive/AmigaLive.app"
sudo xattr -r -d com.apple.quarantine "/path-to-AmigaLive/FS-UAE/FS-UAE Launcher.app"

Solution 3 (Reported by user with Catalina):
sudo xattr -cr "/path-to-AmigaLive/AmigaLive.app"
sudo xattr -cr "/path-to-AmigaLive/FS-UAE/FS-UAE Launcher.app"``





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

# Editors #
1. TextMate So Great
	- Markdown mode seems to catch up slowly (maybe thats fixed). It kind of even seems to type slowly compared to bbedit.
	- Great Bookmark features
	- Great word wrap that automatically sticks to the window width.  (not as unique as I thought)
	- Great simple macro features
2. BBEdit (formerly TextWrangler)
	- more responsive markdown text editing than textmate with built in preview menu item
	- less inline markdown interpretation than textmate
	- Macros aren't easy to find if they are here
	- Big Feature: View different parts of the same file in two different windows with instant update.  Interesting note: In window one if you add a line window 2 scrolls down.  thats annoying because your view in one window shouldn't be affected by the changes in the other window.  You have chosen this view based on content not line number but the view is fixed to line number (or something like that) Emacs is amazing at this and doesn't have this problem.
	- Word wrap doesn't automatically respond to window width . nvm its a super obvious option that I missed but I missed because its only an option .
	- Slight concern that an evaluation feature which I care for will disappear in 30 days.  Textmate is totally free with all of those features.
	- Script editor is kindof a mess if thats the macro features.

	
	
# Making .commands #
 Start it with #!/bin/zsh
 then `` # name of this mod without spaces for save file
name=CK_SpaceHunter_V1.1
# location of the folder this is running from
here=${0%/*}

${here}/GZDoom.app/Contents/MacOS/gzdoom -iwad DOOM.wad  -file ${here}/DTWID.wad ${here}/${name}.pk3 -saveDir ${here}/Saves/${name} ``

# Enjoyable #
This software is GREAT.  Program your game to read from the keybaord and then your controller to write to the ekyboard 

just spent 30 minutes getting 'enjoyable' the controller mapping software for mac working to remap a ps4 controller button to my keyboard space bar!  It seemed to be working but then just never did shit.  looking in lots of forums where lots of people think its just totally broken, i found that you have to just delete it from accessibility and input monitoring in system prefs security tab and then re-add it and then un check and recheck it and then after like a minute or two of changed commands it started working.  now it works great to press space bar for the menu which is super convenient.  

Much more about this software in the Games note esp wrt C64 games but just search for enjoyable

