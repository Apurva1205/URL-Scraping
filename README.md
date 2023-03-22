# URL-Scraping




TASK 1:

In this Python script that performs web scraping of Amazon India's website for bags. It uses the requests and BeautifulSoup libraries to retrieve and parse the HTML content of each page of search results.

The script iterates through the first 20 pages of search results, and for each page it constructs a URL with the appropriate query parameters for the search term "bags" and the page number.

For each page of search results, the script uses soup.find_all() to locate all the div elements with a class of "s-result-item". This corresponds to each individual product listing on the page.

For each product listing, the script extracts the following information:

Product URL: The URL of the product detail page.
Product Name: The name of the product.
Product Price: The price of the product.
Product Rating: The average rating of the product (on a scale of 1 to 5).
Number of Reviews: The number of customer reviews for the product.
The script uses a series of try/except blocks to handle cases where the required information is not present in the HTML of the page.

Finally, the script prints out the product information for each listing on each page of search results.



TASK 2:

This code scrapes product information from Amazon.in and saves it in a CSV file named "products.csv". The code uses the requests library and the BeautifulSoup library to scrape and parse the HTML content of Amazon.in.

The code first defines a function named "get_product_info" that takes a product URL as input and returns a list containing information about the product's description, ASIN, product description, and manufacturer.

Next, the code opens a file named "products.csv" in write mode and creates a CSV writer object. The writer writes the headers for the CSV file, which include "Product URL", "Product Name", "Product Price", "Product Rating", "Number of Reviews", "Description", "ASIN", "Product Description", and "Manufacturer".

The code then loops through 20 pages of search results for the query "bags" on Amazon.in. For each page, the code finds all the product items on the page and extracts their URLs, names, prices, ratings, and number of reviews. If the product URL is valid (i.e., starts with "https://www.amazon.in"), the code calls the "get_product_info" function to extract additional product information such as the product's description, ASIN, product description, and manufacturer. The code then writes all the product information to the CSV file and prints the product information to the console.

Finally, the code prints a message indicating that the scraping is completed and that the product information has been saved to the "products.csv" file.



