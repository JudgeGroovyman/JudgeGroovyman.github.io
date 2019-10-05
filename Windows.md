# Windows



### Custom Context Menu Items
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


### Launching powershell or command.exe ###
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