---
title: "Hands-on Web Scraping for Machine Learning"
header:
    teaser: /assets/images/blog/web_scraping/web_scraping.png


---
# Overview

- **Goal:** extract (some specific) data from website
- **Tools:** 
    - **Install chrome:** [Link](https://www.google.com/chrome/?brand=YTUH&gclid=Cj0KCQjwpcOTBhCZARIsAEAYLuWAFFS1tqyCapsGYcMEuHXkRYqcgAQon0RF8dAiL5c1BZSOi_bNGXoaArs5EALw_wcB&gclsrc=aw.ds)
    - **Install chrome driver:** [Link](https://sites.google.com/chromium.org/driver/) (download and put it in your path)
    - **Automating browsers**: `selenium` [Guide](https://selenium-python.readthedocs.io/installation.html) 
    - **Parse HTML**: `bs4`
    - **Lots of IPs:** public cloud (e.g., AWS EC2 t3.small)
- **Steps:**
    - **1) crawl HTML:** 
        - a) HTTP request: navigate to the target web
        - b) download the response from a, i.e., the source code of the web
    - **2) Parse:**
        - a) parse 1.b with beautiful soup
    - **3) Store:**
        - a) store 2.a
    - ***4) Repeat 1-3**

- **More details:** [Web scraping book](https://github.com/REMitchell/python-scraping)

# Steps

<i class="far fa-sticky-note"></i> **Note:** The idea of web scraping is to translate human browing process into code. Hence, we have to open a browser, e.g., Chrome, and a jupyter notebook, and work with both at the same time. The code is constructed based on what shows up in the browser.
  {: .notice--info}
  {: .text-justify}

## Step 1: Install tools and libraries 
Download chrome drive and put it in your path ("C://Users//path/to/chromedriver/chromedriver.exe"): [Link](https://sites.google.com/chromium.org/driver/) [Guide](https://www.selenium.dev/documentation/webdriver/getting_started/install_drivers/)

Install `selenium` and `bs4` in the command line, or open a jupyter notebook and run:
```python
import sys
!{sys.executable} -m pip install selenium
!{sys.executable} -m pip install beautifulsoup4
```
Load libaries:
```python
from selenium import webdriver
from selenium.webdriver.common.keys import Keys
from bs4 import BeautifulSoup
import re
```

## Step 2: Get HTML
This is like normal browsing but in python code. Here we need lots of IPs, which can get from public clouds, e.g., AWS, Azure, GCP. 

For example, we want to scrap the Zillow website for ML. We first open the website of interest (go to Zillow home page and search Orlando) and copy the URL.
```python
# set url
url = 'https://www.zillow.com/orlando_rb/sold/'

# backend allows you to drive the browser
chrome_options = webdriver.ChromeOptions()

# headless (only command line without GUI to fake human)
chrome_options.headless = True 
chrome = webdriver.Chrome("C://Users/Yi/WebDrivers/chromedriver.exe",
    options = chrome_options)

# get HTML page
page = chrome.get(url)
```
Once we get the page, we may interact with it using `selenium` functions ([for more information](https://selenium-python.readthedocs.io/navigating.html)):

- Locate element: `search = chrome.find_element_by_id("some_id")` where `some_id` can be found by right clicking the element of interest and choose inspect!
- Type in: `search.send_keys("Orlando apartment")`
- Click:  `search.send_keys(Keys.RETURN)`, `chrome.find_element_by_id("some_id").click()`

## Step 3: Parse HTML

```python
# parse HTML (create a beautifulsoup object)
page = BeautifulSoup(open(html_path,'r'))

# find all houses' url links
# find 'a's --- links belongs to 'list-card-link' class
links = [a['href'] for a in [page.find_all('a', 'list-card-link')]]

# get house ids from url
ids = [l.split('/')[-2].split('_')[0] 
      for l in links]
```
Then uses these IDs to create URLs that can return house detail pages. How? Click on any house and see how the ID appears in the URL template, e.g., [https://www.zillow.com/homedetails/46219913_zpid/](https://www.zillow.com/homedetails/46219913_zpid/).

## Step 4: Extract data 
Check the HTML of a house detail page and find its elements (variables for ML) through inspect. The elements can be a scalar (house price), a text (house summary), or an image (house image). We can then easily build an end-to-end model with neural network (NN) that ingests all these data.

### a) Get tabular features and texts.
Incorporate your findings in `bs4_object.find()` and `bs4_object.findall()` with regular expression. For example, we interested in sold price and sold date of a house:
```python
# find where 
sold_items = [a.text for a in page.find('p').findall('span')]
for item in sold_items:
    if 'Sold:' in item:
        result['Sold Price'] = item.split(' ')[1]
    if 'Sold on' in item:
        result['Sold on'] = item.split(' ')[-1]   
```
<i class="far fa-sticky-note"></i> **Note:** Repeat this process for more varibles like HOA, tax, lot, and texts for NLP, e.g., house summary.
  {: .notice--info}
  {: .text-justify}

### b) Get images.
We can find all Zillow images are stored in photos.zillowstatic.com, e.g., [https://photos.zillowstatic.com/fp/83d86052c1615f3b7eda334a90efed5f-uncropped_scaled_within_1536_1152.webp](https://photos.zillowstatic.com/fp/83d86052c1615f3b7eda334a90efed5f-uncropped_scaled_within_1536_1152.webp). We change the ids in this template to get the images we need.

```python
p = r'https:\\/\\/photos.zillowstatic.com\\/fp\\/([\d\w\-\_]+).jpd'

# get all the photo IDs in the HTML
ids = [a.split('-')[0] for a in re.findall(p, html)]

# Fitting the IDs to the template and get image URLs, which can be used to download the images.
urls = [f'https://photos.zillowstatic.com/fp/{id}-uncropped_scaled_within_1536_1152.webp' for id in ids]  
```
And we are done! 


{: .text-justify}