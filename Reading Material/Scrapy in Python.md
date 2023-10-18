# Scrapy in Python Cheat Sheet 🕷️🐍

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the Scrapy cheat sheet! Scrapy is a powerful web scraping framework for Python. With Scrapy, you can easily extract data from websites and save it for your data analysis or other projects. This cheat sheet will help you get started with web scraping using Scrapy.

## Installation

You can install Scrapy using pip:

```bash
pip install scrapy
```

## Code Examples

### Creating a Scrapy Project

To create a new Scrapy project, open your terminal and run:

```bash
scrapy startproject project_name
```

### Creating a Spider

Spiders are scripts that define how to scrape a website. To create a spider, run:

```bash
scrapy genspider spider_name website.com
```

### Defining Items

Define the data structure you want to scrape in `items.py`:

```python
import scrapy

class MyItem(scrapy.Item):
    title = scrapy.Field()
    link = scrapy.Field()
    description = scrapy.Field()
```

### Writing Spider

Create a spider to scrape data by yielding items:

```python
import scrapy
from myproject.items import MyItem

class MySpider(scrapy.Spider):
    name = "myspider"
    start_urls = ['http://example.com']

    def parse(self, response):
        item = MyItem()
        item['title'] = response.css('h1::text').get()
        item['link'] = response.url
        item['description'] = response.css('p::text').get()
        yield item
```

### Running Spider

To run your spider and save the data:

```bash
scrapy crawl myspider -o output.json
```

### Scrapy Shell

Use the Scrapy shell for interactive scraping:

```bash
scrapy shell "http://example.com"
```

### Pagination

Scrape paginated pages by following links:

```python
next_page = response.css('a.next::attr(href)').get()
if next_page:
    yield response.follow(next_page, self.parse)
```

### Following Links

Scrapy makes it easy to follow links to scrape more data:

```python
def parse(self, response):
    for href in response.css('a::attr(href)'):
        yield response.follow(href, self.parse)
```

Scrapy is a versatile web scraping framework with extensive documentation and a helpful community. This cheat sheet provides code examples to get you started.

📖 Scrapy Documentation: [Scrapy Documentation](https://docs.scrapy.org/en/latest/index.html)

Feel free to follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and web scraping-related content. Happy scraping! 🕷️🐍🌟

Made with :heart: by **Fardeen Ahmad Khan**
