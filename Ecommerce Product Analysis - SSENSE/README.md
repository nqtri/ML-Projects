# Ecommerce Product Analysis - SSENSE

SSENSE is one of my favorite e-commerce retailer, especially during sale season so personally I have a lot of interest in their product offerings. Together with the plan to scrape data from the web and create my own dataset for machine learning projects, I decided to try scraping product data from SSENSE. 

In this 1st run, to limit the amount of runtime and to priority the exploratory data analysis and machine learning model building process, only men's products were scraped. The next phase will be expanded to women's products and potentially their brand new cateogory for pets.




## Getting Started

There are several tasks involved in this project.

First, data need to be scraped from the webpage of the retailer to obtain information for each product offering

Secondly, there is potentially room to build a price monitoring tool for a group of products of interest

Lastly, based on product's features, especially product description and price, a similar product recommendation system is built to suggest other items in case a chosen product is sold out

Another expansion is to make use of the image URLs to train a neural network to recognize products of certain designers.

### Data Scraping

The following packages are used in the scraping process:

```
from bs4 import BeautifulSoup
import requests
import json
```

The job was divided into 2 stages: 

##### 1/ Getting brands, products names, prices, IDs, SKUs, product URLs, image URLs

This was done by looping through each category page, the through each sub-page to extract the JSON objects containing the information

##### 2/ Getting product descriptions (and sizes)

After product URLs were obtained, requests were sentt to access those URLs to obtain product description, also in a JSON object. Next iteration should include sizes that are currently a bit more tricky to extract and analyze as they are not contained in the JSON object, but rather under <option> tags and come in several different formats.





