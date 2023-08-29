# Amazon Product Scraping 

This is designed to scrape product details from Amazon product pages using the Selenium and BeautifulSoup libraries in Python. It reads a CSV file containing Amazon product URLs, visits each URL, extracts relevant information, and saves the scraped data in a JSON format.
# Getting Started
## Prerequisites
Python 3.x<br>
Selenium: Install using pip install selenium<br>
BeautifulSoup: Install using pip install beautifulsoup4<br>
Chrome WebDriver: Make sure you have the Chrome WebDriver installed and its path added to your system's PATH variable.
## How code works 
1.Imports: The script imports necessary libraries such as time, json, pandas, selenium, BeautifulSoup, and os for web scraping, data manipulation, and file handling.
<br><br>
2.CSV Data Reading: The script reads the CSV data from the file path specified in csv_file_path using Pandas' read_csv function.
<br><br>
3.Web Driver Initialization: A Chrome web driver instance is initialized using webdriver.Chrome() from the Selenium library.
<br><br>
4.Scraping Function: The function scrape_product_details(url) is defined to scrape product details from a given URL. It navigates to the URL, parses the HTML using BeautifulSoup, and extracts relevant product details like title, image URL, price, and details.
<br><br>
5.Scraping Loop: The script iterates through each row in the CSV data and constructs the Amazon product URL using the country code and ASIN. It then calls the scrape_product_details function to extract product details. If the details are extracted successfully, they are added to the scraped_data list.
<br><br>
6.Batch Processing and Timing: The script processes the data in batches of size batch_size and prints progress information after each batch. It measures the time taken for each batch to provide an indication of progress.
<br><br>
7.JSON Output: The scraped data is saved to a JSON file named scraped_data.json on the desktop. The script constructs the output file path using the expanduser and join methods from the os module.
<br><br>
8.Web Driver Cleanup: After scraping is complete, the web driver is closed using driver.quit() to release the resources.
<br><br>
9.Output and Completion Message: A message is printed indicating the completion of scraping and the location where the scraped data is saved.
