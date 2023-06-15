# CNNnewsDateTime
This Python code is designed to scrape the dates and times of news updates from the CNN website.

Certainly! To scrape the dates and times of news updates on CNN, you can use the "[BeautifulSoup]","(https://pypi.org/project/beautifulsoup4/)"  library in combination with Python's requests module
This code first sends a GET request to the CNN website using the requests module. Then, it creates a BeautifulSoup object to parse the HTML content of the page. Next, it uses the find_all method to locate the news update elements on the page based on their HTML structure and class name.

The code then iterates over each news update, extracts the headline and timestamp information, and prints them to the console. Finally, a dashed line is printed to visually separate each news update.

Please note that website structures can change over time, so this code may need adjustments if the CNN website modifies its HTML structure or class names.
