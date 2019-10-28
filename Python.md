# Python #

## On Win 10 ## 
Have to turn off settings->apps & features->app execution aliases for python to run from command line.  Otherwise it opens the windows app store (so annoying and deeply buried in windows settings)

### Installs ###
* Python 3.8 installs into C:\Users\John McGarey\AppData\Local\Programs\Python\Python38
* Python 2.7 installs into C:\Python27

just change the name of python.exe in python3.8 to python3.exe

## Simple Server ##



## Virtual Environments ##
1. pip install virtualenv
2. virtualenv any_name_you_want
3. virtualenv any_name_you_want
4. source venv/bin/activate
5. deactivate



https://www.alexkras.com/how-to-use-virtualenv-in-python-to-install-packages-locally/

## Pip ##
1. curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
2. sudo python get-pip.py
3. sudo easy_install pip

https://ahmadawais.com/install-pip-macos-os-x-python/

## Pipenv ##
https://opensource.com/article/18/2/why-python-devs-should-use-pipenv

## Scraping ##
I used this to scrape from ebay
https://www.scrapehero.com/how-to-scrape-competitor-prices-from-ebay-com-using-python-and-lxml/

I learned some things but the trickiest part seems to have been: xpaths can be printed as text with from lxml import etree and then print etree.tostring(product) if they are not empty

## Textmate ##
It is great but has something called softtabs which I had to turn off in the ~/.tm_properties softTabs = false_

# Game Engines #
* [Pyglet](https://github.com/pyglet/pyglet) looks amazing and has a really [impressive intro presentation](http://simeonfranklin.com/talk/pyglet/slides.html) and some [nice documentation](https://pyglet.readthedocs.io/en/stable/programming_guide/examplegame.html) and people have [high praise](https://www.reddit.com/r/Python/comments/5dgp20/if_the_pyglet_community_is_dead_and_pygame_is_not/) for it.
* [Pygame](https://www.pygame.org/news) is something I played with in like 2004 (iirc) and really wanted to make a tetris game with.  On the main pygame site there are tons of games listed but most of them are unfortunately over 10 years old and dont exist anymore or are unmaintained.