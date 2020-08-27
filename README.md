# web-scraping-challenge
## Mission to Mars
Flask web application that scrapes various websites for data related to the Mars Mission and displays the information in a single HTML page.
1. mission_to_mars.ipynb - A Jupyter Notebook containing the scraping code used
2. scrape_mars.py - A Python script with a function called scrape that will execute all scraping code and return one Python dictionary containing all of the scraped data
3. templates/index.html - A template HTML file that takes the mars data dictionary and displays all of the data in the appropriate HTML elements
4. mission_to_mars_screenshot.png - A screenshot of the final application.

### Scrapping
* NASA Mars News
Script collects the latest News Title and Paragraph Text.
* JPL Mars Space Images - Featured Image
Script finds the image url for the current Featured Mars Image and assigns the url string of the full size image.
* Mars Facts
Script visit the Mars Facts webpage and uses Pandas to scrape the table containing facts about the planet including Diameter, Mass, etc.
* Mars Hemispheres
Script visits the USGS Astrogeology site and obtains the full resolution images for each of Mar's hemispheres.

### MongoDB and Flask Application
Use MongoDB with Flask templating to create a new HTML page that displays all of the information that was scraped from above.

---
### Copyright
Jiuhe Zhu © 2020. All Rights Reserved.
