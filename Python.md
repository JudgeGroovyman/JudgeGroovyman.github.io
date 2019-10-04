# Python #

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