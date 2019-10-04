# Markdown
Markdown is pretty awesome.  It is a simple plain text markup system which means it is intended to be created in a text editor and doesn't make much sense any other way.

Github was designed specifically around using it for readme files so it is excellent at rendering markdown and is really the gold standard of how github should work.

# How to use Markdown
Here's what I've learned so far:

### How to make a link
`[Name](link)`

### H3 Header##
`### H3 Header##`
#### H4 Header##
`#### H4 Header##`
____
1. Lists Start the line with a 1 or *
* `1. Lists Start the line with a 1 or *`
* Sub-bullets with tab
* `* Sub-bullets with tab`
5. Don't try to number them correctly
* `5. Don't try to number them correctly`
1. *emphasis* **emphasis** **_emphasis_**
* `*emphasis* **emphasis** **_emphasis_**`

____
horizontal rule 
`___`
____


### Other Things you Can Do with Markdown ###
Images
Syntax Highlighting
Tables

# Cheatsheet
This is a good cheatsheet and is exhaustive, however I prefer my own cheatsheet (the file you are reading right now) because its more to the point of what I need for my purposes.

[Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

# Previewing Markdown
Some (many?) text editors support some level of preview.
* Textmate for mac displays some elements properly
* Atom and Visual Studio Code have full previews

[Other Options](https://stackoverflow.com/questions/9843609/view-markdown-files-offline)

## Previewing in Browser
There are apparently some Chrome browser plugins which let you drag your markdown into the browser to preview it.

### Copy and Paste
Copy your markdown into the left pane of this website and see the preview of the right pane

[Markdown Live Preview](https://markdownlivepreview.com)

### Previewing in Quicklook on Mac
[QLMarkdown](https://github.com/toland/qlmarkdown) lets you hit spacebar from the finder on your markdown file to preview it using Quicklook.  This works pretty well

### Localhost Markdown Server

One disadvantage with the other options is they dont render the markdown perfectly like github would.  With these two options you aren't tied to any editor or the MacOS Finder.

These are little local servers that you fire up in the directory with your markdown and then you point a browser to a localhost port and it will preview it.

#### Markserv
[Markserv seems to be the best option](https://www.npmjs.com/package/markserv)
Update: As of Jan 23 2019  I had numerous apparent npm install problems, but it ended up working just fine.
Then I just type markserv in your markdown folder and it opened a browser to that folder to let me browse.

#### Grip
1. Download [grip](http://stackoverflow.com/questions/9843609/view-markdown-files-offline)
* Here are some notes about [grip at github](https://github.com/joeyespo/grip)
1. then type `grip <filename> <port>`
1. then open the site it puts out and it will auto-update as you save your file
1. Update: After 60 requests you will need to use the `--user= --pass=` which require -user-content

Example that works:
` grip --user-content --user=judgegroovyman --context=judgegroovyman/shiny-fortnight --pass= . 2627`

# Converting #
Converting to/from Markdown (or dozens of other formats)
[Pandoc](http://pandoc.org)

# Delineating Sections #
Sometimes its nice in a large markdown file to be able to clearly see what sections are what.  One way to do that is to put a big text header in comments:

## What it should look like ##
This is what it would look like in the comments
```text
  _______        _     _    _                _           
 |__   __|      | |   | |  | |              | |          
    | | _____  _| |_  | |__| | ___  __ _  __| | ___ _ __ 
    | |/ _ \ \/ / __| |  __  |/ _ \/ _` |/ _` |/ _ \ '__|
    | |  __/>  <| |_  | |  | |  __/ (_| | (_| |  __/ |   
    |_|\___/_/\_\\__| |_|  |_|\___|\__,_|\__,_|\___|_|  
```	
	
## HTML Comment ##
This is the same thing in an HTML comment (Ideally you won't see this)
	
<!-- 
  _______        _     _    _                _           
 |__   __|      | |   | |  | |              | |          
    | | _____  _| |_  | |__| | ___  __ _  __| | ___ _ __ 
    | |/ _ \ \/ / __| |  __  |/ _ \/ _` |/ _` |/ _ \ '__|
    | |  __/>  <| |_  | |  | |  __/ (_| | (_| |  __/ |   
    |_|\___/_/\_\\__| |_|  |_|\___|\__,_|\__,_|\___|_|  
	In HTML Comment
	
-->

## Tricky Markdown Comment

This is the same thing in a tricky markdown comment (Ideally you won't see this either)

[//]: # (  _______        _     _    _                _           )
[//]: # ( |__   __|      | |   | |  | |              | |          )
[//]: # (    | | _____  _| |_  | |__| | ___  __ _  __| | ___ _ __ )
[//]: # (    | |/ _ \ \/ / __| |  __  |/ _ \/ _` |/ _` |/ _ \ '__|)
[//]: # (    | |  __/>  <| |_  | |  | |  __/ (_| | (_| |  __/ |   )
[//]: # (    |_|\___/_/\_\\__| |_|  |_|\___|\__,_|\__,_|\___|_|   )

If you put something like this in your markdown source it will be easily scanned by a human reader.

## How to make ##

http://patorjk.com/software/taag/#p=display&f=Big&t=Meshes