# Fetching Data Using Web Scraping

## What is Web Scraping?

Web scraping is a method of collecting data from a website by sending a request to the webpage and reading the HTML response.

The HTML is then parsed and the required information is extracted using tags, classes, and other HTML attributes.

## Why Web Scraping?

Web scraping is useful when the required data is available on a webpage but there is no suitable public API to directly fetch it.

In this practice, I collected company information such as:

- Company Name
- Rating
- Reviews
- Salaries
- Interviews
- Jobs
- Benefits

## Approach

The basic workflow followed in this project:

```text
Website URL
     ↓
Send HTTP Request using Requests
     ↓
Server sends HTTP Response
     ↓
Response contains HTML
     ↓
Pass HTML to BeautifulSoup
     ↓
Parse the HTML
     ↓
Find required HTML tags/classes
     ↓
Extract required data
     ↓
Store data in Python lists
    * - Used as the HTML parser with BeautifulSoup.
- **Pandas** - Stores and combines the scraped data in DataFrame format.
- **re** - extracts the number and its k/L suffix in one pattern match, avoiding manual string slicing.
## What I Learned ↓
Create dictionary
     ↓
Convert into Pandas DataFrame
     ↓
Repeat for multiple pages
     ↓
Combine all pages
     ↓
Final Dataset
```

## Libraries Used

- **Requests** - Sends HTTP requests and receives webpage responses.
- **BeautifulSoup** - Parses HTML and helps extract required elements.
- **lxml** - Used as the HTML parser with BeautifulSoup.
- **Pandas** - Stores and combines the scraped data in DataFrame format.
- **re** - Extracts the numeric part and its k/L suffix so the value can be converted correctly.
## What I Learned

This project helped me understand the basic web scraping and data collection workflow:

**Request → Response → HTML → Parse → Find Elements → Extract Data → Store Data → Combine Pages**

I also practiced working with HTML tags, classes, `find()`, `find_all()`, indexing, loops, dictionaries and Pandas DataFrames.

## Note

This is a practice project created to understand web scraping and data collection. The data collected depends on the information available on the webpage at the time of scraping.
