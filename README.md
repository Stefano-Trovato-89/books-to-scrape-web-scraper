# Books to Scrape Web Scraper

![Books to Scrape Web Scraper Banner](books-to-scrape-web-scraper-banner.png)

## Project Description
This project implements a **web scraping script** to extract information about books listed on the online bookstore **Books to Scrape**, supporting market analysis activities for BookSmart Solutions S.r.l.

The main activities include:
- **Data collection** from the pages of `https://books.toscrape.com/` using **Python**, **Requests**, and **BeautifulSoup**.  
- **Automatic extraction** of the following information for each book:
  - title (`Title`)
  - star rating (`Rating`, numeric value from 1 to 5)
  - price (`Price`, converted to a numeric value)
  - availability (`Availability`, e.g. *In stock* / *Out of stock*)  
- **Pagination handling** across all catalog pages (1,000 books in total).  
- **Robust handling of network errors** (retry with exponential backoff) and **polite rate limiting** via random delays.  
- **Construction of a structured dataset** and export to CSV for subsequent pricing analysis, competitive benchmarking, and identification of the most relevant titles.

## Project Files
- [books_to_scrape_web_scraper.ipynb](./books_to_scrape_web_scraper.ipynb) – Jupyter/Colab notebook containing:
  - description of the context and objectives,
  - full implementation of the scraper (Requests + BeautifulSoup + Pandas),
  - logic for cleaning/normalizing rating and price,
  - preview of the final dataset (first and last rows).

- [books.csv](./books.csv) – Exported final dataset, containing:
  - **1,000 rows** (one for each book in the catalog),
  - **4 columns**: `Title`, `Rating`, `Price`, `Availability`.  
  The file is ready to be used in analysis tools (e.g. Excel, BI platforms, other Data Science notebooks, or Data Engineering pipelines).

## Author
Stefano Trovato  
[GitHub Profile](https://github.com/Stefano-Trovato-89)  
[LinkedIn](https://www.linkedin.com/in/stefano-trovato)
