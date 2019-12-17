# Windows #

# Dropbox #
* If the client gets stuck cyncing files heres an [advanced possible workaround](https://www.reddit.com/r/dropbox/comments/8rae7h/dropbox_stuck_on_indexing_syncing_in_windows_10/)


# Diff and Merge #
* WinMerge seems to be the best option but theres something critical you have to do after you install:  Edit->Options->Compare->Folder->Include Subfolders  and then (immediately above that checkbox) Include Unique Subfolders Contents.  If you don't and you compare a directory tree it will happily tell you that they are identical when everything below the current level could be completely different.  In the last 24 hours I've done 5 or 6 diffs without that checked and I shudder to think what I might have missed.  

# Office Suites#
Microsoft Office is the king but is somewhat expensive.  $150 for non-commercial use $250 for commercial use. or $439 for Professional (dont know the differences).  Office 365 is subscription based but lets you install on all of your computers (the one time is only on one pc or mac) but costs $70/yr for one person or $100 for 6 people on all of their devices.  Something like that.  its still really good though.



## Free Office Suites ##
Fortunately we have access to some really nice office suites for free.

* WPS Office is my favorite free office suite.  Advantages? 
	* Advantages?  Win/Mac/Lin/iOS/Android/Web its fast (at least on Windows).  In my tests editing a large powerpoint file (well a powerpoint slide with lots of text on it) is snappier in this than in the other free suites and that matters to me a lot.  The interface is nice too.   It doesnt let you simply remove background when printing a powerpoint slide like mac or windows do but it does let you swithc to 'black and white only' which accomplishes much of the same.  its got a nice print preview feature.
	* Disadvantages? 1.  It didnt open a .pptx file that I had.  To be fair it was originally made on keynote on the mac, then converted to SoftMaker Freeoffice then saved as .pptx.  Even opening it as a .ppt file it lost some formatting but that is somewhat to be expected.  2. Copying and pasting doesnt always maintain formatting: If you copy a line with several point-sizes of text when you paste it all of the text will be the same point-size.  every time I open this one file that I have it gives me a warning "some fonts are not available on this system" then when I replace them 'permanently' the warning still comes up next time.  Every time you save it suggests you upload your document to their cloud service with a distracting and unappealing yellow warning in the top left.  They want you to create an account and it could be that if I did they wouldn't bother me with this anymore.  It seems to chop a bit off of the left side of the border when printing.  its weird its like its offset a few pixels.  Theres probably a way to work around that with different margins but there is substantial margins in this document already and I guess the real problem is that the print preview does not look like the printout since there are even substantial margins in the print preview!
* Only Office - Win/Mac/Lin Open source and regularly updated.  I didnt spend much time with it but the interface was just slightly less familiar to me than the other two.  I liked the crispness of the resizing of text boxes in this one better than the other two.  It was slower to edit powerpoint slides with lots of text on them than WPS office.  That mattered to me.
* SoftMaker Freeoffice - Win/Mac/Lin I like the features and interface here very much.  It looks exactly like MS Office.  A few advanced things are less than ideal: When you are editing a text box in a presentation it lets you know which text box is being edited by making the background of that textbox a bright red color which is hard to read and unappealing.  Perhaps this can be changed in the settings?  I can't find it.  I like that they have an option to make the interface more like office 2003 instead of the ribbons of 2007.   You can save in many formats from this program.    It was slower to edit powerpoint slides with lots of text on them than WPS office.  That mattered to me.  It also doesnt use keyboard combinations much (or I cant figure out what they are).  WPS office seems to use MS Office keyboard combinations.  One of the most important disadvantages is you can't print a powerpoint slide without also printing its background.  Keynote and Powerpoint let you do remove the background and just print the text.  Thats a really nice feature and a disadvantage for me for this software.
* Apples office suite is perhaps the most polished of all and comes free with MacOS.  


# Custom Context Menu Items #
create a .reg file and paste some commands in there then right click and 'merge' to merge it into your registry.
UPDATE: This may only work on Win7 not Win10

~~~~
REGEDIT4

[HKEY_CLASSES_ROOT\Folder\shell\Open Parent]
@="Open &Parent"
[HKEY_CLASSES_ROOT\Folder\shell\Open Parent\Command]
@="Explorer.exe \"%L\\..\""
~~~~

https://superuser.com/questions/98717/get-the-parent-of-a-folder-from-search-results


# Launching powershell or command.exe #
shift right click on a folder and select `open powershell window here` 

if you want to use the command.exe features instead of powershell just type cmd at the powershell prompt

# Unix on Windows #
Linux, Unix and GNU are and have some amazing toolsets.  The [gnuwin32](http://gnuwin32.sourceforge.net/packages.html) lets you use some of those tools on windows. 
* make
* lha
* bc
* less
* grep
* nawk
* sed
* tree
* wget
* rpl
* [tons more](http://gnuwin32.sourceforge.net/packages.html)

Also
* tar
* pdcurses
* jpg, tiff, gif, png image libraries
* gd for image creation
* libart library for high performance 2d graphics


# Windows Path #
Adding a folder to windows path environment variables is easy.  
Once you're in the environment variables gui then just select path, hit edit, hit new, and paste the path.
To get to the environment variables gui type `sysdm.cpl` then click the advanced tab then alt-n or environment variables at the bottom.  
You'll probably have to open a new powershell otherwise theres no easy built in way to reload the environment variables (although there are ways)