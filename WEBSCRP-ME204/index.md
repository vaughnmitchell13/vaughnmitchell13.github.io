---
layout: default
title: ME204 Webscraping Report
---

# Webscraper for edX Courses

## ℹ️ Introduction
This is a webscraper for all [edX](https://www.edx.org/search?tab=course) courses. It collects information on the course name, provider, time commitment, start date, price of certificate, current enrollment, and subject.

## 🔁 How to Replicate
1. Install Python and create a [venv environment](https://www.freecodecamp.org/news/how-to-setup-virtual-environments-in-python/).
2. If running on VScode, clone this repository and...
    - For `NB01-Data-Collection.ipynb` and `NB02-Build-Database.ipynb` use the .venv environment created in step 1.
    - For `NB03-EDA-and-Dataviz` use the base environment.
3. Install the required packages
```bash
pip install -r requirements.txt
```
3. Install the Chrome Webdriver from [Google](https://developer.chrome.com/docs/chromedriver/downloads) depending on your Chrome version and processor information.
4. Go through all the Jupyter notebooks from [this repo](https://github.com/vaughnmitchell13/edX-webscraper/tree/main/myproject/notebooks) and run them, step by step. There may be some path misalignments so you can change those in another Python cell accordingly.

## 📊 Results
![Figure 1](https://raw.githubusercontent.com/vaughnmitchell13/vaughnmitchell13.github.io/main/WEBSCRP-ME204/figures1.png)
***
![Figure 3](https://raw.githubusercontent.com/vaughnmitchell13/vaughnmitchell13.github.io/main/WEBSCRP-ME204/figures3.png)
***
![Figure 2](https://raw.githubusercontent.com/vaughnmitchell13/vaughnmitchell13.github.io/main/WEBSCRP-ME204/figures2.png)



## 🤖 AI Acknowledgement
This project was completed with the help of ChatGPT.

More specifically, I used it in the following ways:

- Correcting ggplot syntax and installing CairoSVG to save my visualizations.
- Finding setup information for the Chrome Webdriver/Selenium.
- When I scraped data from each course, I wrote a rough script but used ChatGPT to convert my code into separate functions.
- Using the 'driver' functions and passing correct tags from the edX website.






