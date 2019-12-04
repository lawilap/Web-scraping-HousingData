# OFF-CAMPUS APARTMENT HUNT!

This is a python code to scrape housing data from craigslist website and can be customized to scrape area based on pincode

## Objective

In this project we are scraping craiglist website to extract apartment rental details and listings aimed at international students. The reason to choose this website is because it is open, one of the widely used websites by international students and it is open to perform operations. There are few sites like "Hotpads" where we require authentication to extract its web informations. Hence we were not able to scrape hotpads. 
This result dataset can be used for various purposes like building a recommender system based on factors like pricing, crime index, etc. using Machine Learning and other EDA approaches. 

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

## Packages required
* BeautifulSoup
* UrlLib
* Pandas

### Assumptions

* The students using our dataset are incoming Drexel/Upenn/Temple students looking for apartments in and around philadelphia area.
* Students will be looking at rental posts which has the price and images mentioned.
* No more than 1 million pages in the search result.


### Code Usage

* You can download Craiglist.ipynb notebook and follow along the steps to recreate the data.
* For the initial input you're required to pass a valid pin-code for Philadelphia region.
* The final dataset will be generated in the folder called 'data' being created in the same folder as the parent code.


## Program Flow

* Get Pin code from user and check if its valid. 
* Create a variable (url) and get assign the url for the first page of the search result containing the pin from step 1 
* Assuming the no of pages in a search result is less than 1 million, we are using loop to iterate over the pages. 
* Creating a new variable (s) and incrementing it by 120 (no of posts per page), to generate URL's for page 2 till the last page of search. 
* Also creating multiple empty lists to store price(Rent_amount), date posted(Date_posted), link(Link), title(Description), room type(Bedroom) and location of the place(Location). 
* Utilizing get module to scrap the URL and BeautifulSoup to parse it into HTML content and store it into a variable (k). 
* Since k will be greater than 0 when there is a content in the page, we use this parameter to break the loop. 
* to perform processes on the posts, we use the length of k variable to figure out number of posts. 
* Extract necessary information from the post (which is within k) using appropriate tags ("span", "class", "time", "a") and classes ( 
* Appending the extracted values to the variables created in step 5. 
* Exporting the final results to a CSV file.

## Distribution

The entire or a part of this code is free to be used by any individual for their personal or research purpose.


## Authors

* **Parag Paliwal** 
* **Yagna Ganesh Easwaran** 
