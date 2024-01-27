Task: Template for a web scraping script designed to extract product information from an e-commerce website.

Overview: TTP Request: The script sends an HTTP request to the target URL of the e-commerce website to retrieve the HTML content of the page. It includes a User-Agent header to mimic a browser, which helps in avoiding potential blocks by the website for non-browser traffic.

HTML Parsing: Upon receiving the HTML content, the script uses BeautifulSoup, a Python library for parsing HTML and XML documents. This library creates a parse tree from page source code, which can be used to extract data in a more readable and accessible format.

Data Extraction: The script looks for HTML elements that contain product information. It uses find_all to search for div tags with a class of product (the class name is hypothetical and should be replaced with the actual class used by the website). Within each product div, it further extracts the product's name, price, and rating by searching for the respective HTML elements and classes that contain this information.

Data Storage: Extracted data for each product is stored in a list. Each product's details (name, price, rating) are stored as a sublist within the main list.

CSV Output: The script writes the extracted data into a CSV file named products.csv. It first writes a header row with the column names, followed by rows of product data.

Completion Message: Once all the data has been written to the CSV file, the script prints a message indicating that the scraping has been completed and the data has been saved.
