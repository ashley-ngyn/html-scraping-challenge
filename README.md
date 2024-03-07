# html scraping challenge #

## instructions ##
* Deliverable 1: Scrape titles and preview text from Mars news articles.
* Deliverable 2: Scrape and analyze Mars weather data, which exists in a table.

* Part 1: Scrape Titles and Preview Text from Mars News
    * Use automated browsing to visit the Mars news site
    * Create a Beautiful Soup object and use it to extract text elements from the website.
    * Extract the titles and preview text of the news articles that you scraped. 
    * Optionally, store the scraped data in a file
* Part 2: Scrape and Analyze Mars Weather Data
    * Use automated browsing to visit the Mars Temperature Data Site
    * Create a Beautiful Soup object and use it to scrape the data in the HTML table
    * Assemble the scraped data into a Pandas DataFrame.
    * Examine the data types that are currently associated with each column. 
    * Analyze your dataset by using Pandas functions to answer questions
    * Export the DataFrame to a CSV file.


## sources ##
* 01: https://stackoverflow.com/questions/23377533/python-beautifulsoup-parsing-table
    * __to find text in the rows__
        * for r in rows_data:
            cols = r.find_all('td')
            cols = [c.text.strip() for c in cols]
            data_list.append([c for c in cols if c])

* 02: https://stackoverflow.com/questions/38309729/count-unique-values-per-groups-with-pandas
    * __finding value counts__
        * months = mars_df.month.value_counts()

* 03: https://stackoverflow.com/questions/43855474/changing-sort-in-value-counts
    * __to sort in value counts__
        * months = mars_df.month.value_counts().sort_index()
    
* 04: https://stackoverflow.com/questions/40568438/python-pandas-dataframe-find-max-for-each-unique-values-of-an-another-column
    * __finding unique values from another column__
        * warm_month = avg_low_temp.idxmax()


## websites used for data scraping ##
* https://static.bc-edx.com/data/web/mars_news/index.html
* https://static.bc-edx.com/data/web/mars_facts/temperature.html
