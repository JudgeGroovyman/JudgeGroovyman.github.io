
# Converting Videos #
Format Factory seems to work pretty well on Windows.

# Editing Videos #
VSDC Video Editor seems to work pretty well on Windows.

#Downloading Videos#

###youtube-dl###
youtube-dl really easily downloads videos from tons of different websites and is constantly updated

#####Commands#####
1. To get titles
	* `youtube-dl -e` 
1. To download everything in a huge file
	* `youtube-dl --batch-file#path/to/file.txt`
1. To ignore errors during playlist download
	* `youtube-dl -i`
1. Gets a file like the eventual filename
	* `youtube-dl --write-info-json --skip-download --output '%(title)s-%(duration)s.%(ext)s'`
1. Make the filenames better (includes duration and removes the id)
	* `youtube-dl --output '%(title)s-%(duration)s.%(ext)s'`
1. To download english subtitles
	* `youtube-dl --write-sub --sub-lang en --sub-lang en-GB --skip-download`
	* or if that doesn't work
	* `youtube-dl --all-subs --skip-download`
	

#####Best Command for Me:#####

` youtube-dl --output '%(title)s-%(duration)s.%(ext)s' -i `

###Other Options for Downloading Videos###
1. jdownloader
1. listentoyoutube.com (audio download)
1. there are some online sites that will let you download videos of a certain length
1. You can often do some tricks using the page source
1. Safaris activity monitor (sp?) makes it easy to find the video


# Youtube #

###How to get the image from a video###

To get the image for a youtube video:
http://img.youtube.com/vi/0D5bWfZDIgA/0.jpg

Thats the image for this video
https://www.youtube.com/watch?v=0D5bWfZDIgA


# Joining on Mac #

1. AVITools is trialware and doesnt seem to allow joining in the trial version.  It might work for $5.99 but I have no idea.  Its annoyances sure do work.  You have to wait a while to select a second file, and you cant drag files and drop without registering.  Ok I found the join feature on a separate tab and with a separate list and it onlyy works for avi files so worthless.
2. MergeSX Crashed a lot, free version puts a huge watermark, but seems to work for certain video formats, and totally crash for others.  I did get one video merged with a huge watermark.
3. https://www.mp4joiner.org/en/ is working pretty well for starters.  Does re encode but that should be ok.  It crashed after 5min of my first converstion.  The second one worked just fine but aspect ratio is a problem.

# Splitting Videos  on Mac #
1. movavi split movie 2 - super clumsy but totally works
2. mp4splitter you set split points and then turn parts on or off.  I like this one even though there is some clumsiness in it too.




