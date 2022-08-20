# Mission to Mars

## Overview

We used Python's BeautifulSoup and Splinter to automatically scrape four websites for data and images relating to Mars.  This information was stored in a NoSQL database using Mongo, then presented in a website created using Flask, incorporating several Bootstrap elements to make a nicer page.  

## Scraping

Our scraping was first done using [Jupyter Notebook](Mission_to_Mars_Challenge.ipynb), then converted to a regular [Python script](Mission_to_Mars_Challenge.py).  This was then refactored to be [several functions](scraping.py) rather than a single script.  The created `scrape_all()` function is then callable in our [app.py](app.py) file to create our Flask site.  

The first data we collected comes from [Nasa](https://redplanetscience.com), where we scraped the title and the teaser for the first article on the page.  The next bit is CalTech's Jet Propulsion Lab's [Featured Mars Image](https://spaceimages-mars.com).  This is followed by a table of facts about Mars from [Galaxy Facts](https://galaxyfacts-mars.com).  Lastly, we collected high resolution images of Mars' hemispheres from [marshemispheres.com](https://marshemispheres.com/).  

The scraped data was stored in a Python dictionary that was then transmitted to a MongoDB database using PyMongo.  

## Creating a Webpage

Flask and Bootstrap enabled us to quickly and easily make a nice looking website.  Flask allows us to add our `scrape_all()` function directly to our site
