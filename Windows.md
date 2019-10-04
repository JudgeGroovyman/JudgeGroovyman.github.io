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