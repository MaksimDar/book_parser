# Book Parser

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python&logoColor=white)
![BeautifulSoup4](https://img.shields.io/badge/BeautifulSoup4-web%20scraping-yellowgreen)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-ORM-red)
![Poetry](https://img.shields.io/badge/Poetry-dependency%20management-60A5FA?logo=poetry&logoColor=white)

## Description

A Python web scraper that collects book data from [books.toscrape.com](http://books.toscrape.com/) — a public sandbox site designed for scraping practice — and stores the extracted information in a local SQLite database using an SQLAlchemy ORM model.

## Tech Stack

- **Python 3.10**
- **Requests** — HTTP requests to the target site
- **BeautifulSoup4** — HTML parsing
- **SQLAlchemy** — ORM and database interaction
- **SQLite** — local data storage
- **Poetry** — dependency and environment management

## Functionality

- Fetches the homepage of `books.toscrape.com` and parses all listed books.
- Extracts, for each book: cover image URL, title, price, and star rating (converted from text, e.g. `"Three"`, to a numeric value from 1 to 5).
- Defines a `Book` ORM model (`model.py`) and persists all scraped records into a local SQLite database (`my_books.db`).
- Prints all stored records to the console after insertion, for verification.

## Installation & Usage

```bash
git clone https://github.com/MaksimDar/book_parser.git
cd book_parser

poetry install
poetry run python3 main.py
```

## Links

- Repository: [github.com/MaksimDar/book_parser](https://github.com/MaksimDar/book_parser)
- Data source: [books.toscrape.com](http://books.toscrape.com/)

## Author

**Maksym Dovhusha**
