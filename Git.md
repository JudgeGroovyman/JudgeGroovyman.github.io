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

