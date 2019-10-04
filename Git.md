# Clients #

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

