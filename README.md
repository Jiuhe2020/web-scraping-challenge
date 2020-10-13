# Mission to Mars
![Mars](https://wonderfest.org/wp-content/uploads/2018/01/mission-mars-e1528241593215.jpg)

## Challenge Instructions
Flask web application that scrapes various websites for data related to the Mars Mission and displays the information in a single HTML page.

## Scrapping
The scraping script was completed by using Jupyter Notebook, BeautifulSoup, Pandas and Requests/Splinter.
- NASA Mars News  
Script visits the [NASA Mars News Site](https://mars.nasa.gov/news/page=0&per_page=40&order=publish_date+desc%2Ccreated_at+desc&search=&category=19%2C165%2C184%2C204&blank_scope=Latest) and collect the latest News Title and Paragraph Text (as of 8/27/2020).
<p align="center">
  <img src="https://github.com/Jiuhe2020/web-scraping-challenge/blob/master/images/Mars%20News.png">
</p>

- JPL Mars Space Images - Featured Image  
Script visits the url for [JPL Featured Space Image](https://www.jpl.nasa.gov/spaceimages/?search=&category=Mars). Use splinter to navigate the site and find the image url for the current Featured Mars Image and assigns the url string of the full size image.
- Mars Facts  
Script visits the [Mars Facts](https://space-facts.com/mars/) webpage and uses Pandas to scrape the table containing facts about the planet including Diameter, Mass, etc.
<p align="center">
  <img src="https://github.com/Jiuhe2020/web-scraping-challenge/blob/master/images/Mars%20Facts.png" height="40%" width="40%">
</p>

- Mars Hemispheres  
Script visits the [USGS Astrogeology Site](https://astrogeology.usgs.gov/search/results?q=hemisphere+enhanced&k1=target&v1=Mars) and obtains the full resolution images for each of Mar's hemispheres.

## MongoDB and Flask Application
MongoDB with Flask templating was used to create a new HTML page that displays all of the information that was scraped from above.
- Convert the Jupyter notebook into a Python script called `scrape_mars.py` with a function called `scrape` that will execute all of the scraping code from above and return one Python dictionary containing all of the scraped data
- Create a route called `/scrape` that will import the `scrape_mars.py` script and call the `scrape` function
  - Store the return value in Mongo as a Python dictionary
- Create a root route `/` that will query the Mongo database and pass the mars data into an HTML template to display the data
- Create a template HTML file called `index.html` that will take the mars data dictionary and display all of the data in the appropriate HTML elements
<p align="center">
  <img src="https://github.com/Jiuhe2020/web-scraping-challenge/blob/master/mission_to_mars_screenshot.png">
</p>

## List of Files
1. mission_to_mars.ipynb: a Jupyter Notebook containing the scraping code
2. scrape_mars.py: a Python script with a function called scrape that will execute all scraping code and return one Python dictionary containing all of the scraped data
3. templates/index.html: a template HTML file that takes the mars data dictionary and displays all of the data in the appropriate HTML elements
4. mission_to_mars_screenshot.png: a screenshot of the final application

---
### Copyright
Jiuhe Zhu © 2020. All Rights Reserved.
