# Clients

## Kraken ##
As of August 2019 its about to become subscription based. It was free for individual use prior to this.  Its like $40 per year.

## Tower ##
Like Kraken its also subscription based.  Its like $70 per year.

## Fork ##
This looks like the best free client.

## GitUp ##
An instantaneous visualizer for a repo.  Apparently maps out 40k commits in 1s.  Free and Open Source.

# Renaming files on MacOSX #
Its no problem to do this in general but there is a specific issue with case.

If you rename the file from 
`name`
to 
`Name`

it won't stay renamed after you pull from git again.

If instead you use the command:
`git mv --force name Name`

it will rename it and it should also stick.

# Changing things deep in the repo #
To change things deep in the repo, use bfg
[BFG Repo Cleaner](https://rtyley.github.io/bfg-repo-cleaner/)

To execute it you just download the jar and then 
`java -jar bfg-1.13.0.jar`

I followed the instructions and used the following commands:
```
git clone --mirror https://github.com/JudgeGroovyman/HomeRun.git
java -jar bfg-1.13.0.jar --delete-files InteractiveFiction.md HomeRun.git
cd HomeRun.git
git reflog expire --expire=now --all && git gc --prune=now --aggressive
git push
```

# Line Endings #

## One opinionated approach for unix line endings ##
run these to make your instance of the repo default to lf (in fork that means opening the repo in console) 
```
 git config core.eol lf
 git config core.autocrlf input
```
This worked for me when I was using an Amiga repo from windows.  I had cloned it in windows without a .gitattributes (of course) and without any of those settings in my user folder.   I used fork's `open in console` menu option to get to the git console and from there ran those config commands.  Then I did the other thing it said to do in [this answer](https://stackoverflow.com/questions/2517190/how-do-i-force-git-to-use-lf-instead-of-crlf-under-windows/33424884#33424884) which fixed the files in my current directory:
```
git rm -rf --cached .
git reset --hard HEAD
```
and when I was done the files were all converted properly!

* Try pulling it again and then running these commands

More [autocrlf and how it works](https://stackoverflow.com/a/20653073)

## Forcing a repo to always use unix line endings ##

To force a repo to use unix line endings when the git user is in windows (regardless of how they have their git setup) you have to have a `.gitattributes` file in the root folder. 

```
* text=auto eol=lf
```


# Compression Project #
I had 1,371 versions of the same document in a folder.  It was the backup history from an app that I use and most of the versions were around 1MB.  So I used some clever python to analyze the files in that directory and generate a list of git commands that would let me store only the changes from file to file.  That python worked rather well and the whole process took me like 2h (which included installing python and figuring out how to use it to do what I wanted).  If I were to do it all again right now it would probably take me 30min.

Here are the results:
1,631,741,925B Folder with all versions of the file uncompressed
  489,723,490B That folder zipped
  602,313,404B The git repo with all versions of that file
  602,875,856B The git repo zipped
  
Result: The zip file is quite a bit smaller than the git repo.  This is unexpected.  My theory was that the git repo would be 100MB having stored only the changes to the files, but I was wrong about that.  Could it have been a problem with how I checked the files into the git repo or the file format of the files? I dont think so.  The files were legitimately just text files in an outline format (with tabs to indent).  

However I tried something else:  7z
  423,751,156B The git repo.7z (thats smaller than the zip of the text files so the smallest yet)
  
But then I tried 7z on the text files:
   13,612,876B Thats not a typo.  13MB!?!  what???
   
So I'm suspicious of that result and am going to check again and wow I unzipped the .7z and it blew up to 1.5GB and each of the text files was intact and had file date and size correct and I sampled a few files and they look great.
Holy Cow!  


# No Dropbox #
They're to some degree for the same purposes and they don't work together.  They will seem to work just fine (and will for a while) but then when you are least expecting it dropbox won't sync one of the tiny git files until after you make an update and then git is confused and or corrupted.  Similarly the quantity of files with huge strange names makes it difficult for dropbox to keep up and has caused my dropbox to endlessly sync certain files (and it wasn't able to tell me which ones).  Its hard on both git and dropbox and eventually fails.


This is [One of the Reasons Why](https://www.reddit.com/r/dropbox/comments/8rae7h/dropbox_stuck_on_indexing_syncing_in_windows_10/)
