# CNNnewsDateTime
This Python code is designed to scrape the dates and times of news updates from the CNN website.
import requests
from bs4 import BeautifulSoup

# Send a GET request to the CNN website
url = 'https://www.cnn.com/'
response = requests.get(url)

# Create a BeautifulSoup object to parse the HTML content
soup = BeautifulSoup(response.content, 'html.parser')

# Find the news update elements on the page
news_updates = soup.find_all('span', class_='cd__headline-text')

# Iterate over the news updates and extract the date and time
for update in news_updates:
    headline = update.text.strip()
    timestamp = update.find_previous('span', class_='cd__timestamp').text.strip()
    print(f"Headline: {headline}")
    print(f"Timestamp: {timestamp}")
    print('-' * 50)
