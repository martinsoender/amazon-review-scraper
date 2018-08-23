# scraper

An Amazon review scraper built in python

## Installation

### Prerequisites

Create your virtual environment by running
`pipenv shell` within the repo.

### Install requirements

`pip install -r requirements`

### Execute program

`python amazon_reviews.py`

### Output

A `data.json` file will be created once the script is executed. The file is in JSON format and has the following structure:

```
[
  {
    "reviews": [
      "review_header": "",
      "review_text": "",
      "review_comment_count": "",
      "review_posted_date" "",
      "review_rating": "",
      "review_author" ""
    ],
    "ratings": {
      "2 star": "4%",
      "1 star": "10%",
      "4 star": "17%",
      "3 star": "5%",
      "5 star": "64%"
    },
    "price": "",
    "url": "",
    "name": ""
  },
  ...
]
```

Example of json file with scraped data:
```
[
  {
    "reviews": [
      "review_header": "Best phone I have owned ever",
      "review_text": "I love this iPhone X",
      "review_comment_count": "",
      "review_posted_date" "19 Jul 2017",
      "review_rating": "5.0",
      "review_author" "Mart"
    ],
    "ratings": {
      "2 star": "4%",
      "1 star": "10%",
      "4 star": "17%",
      "3 star": "5%",
      "5 star": "64%"
    },
    "price": "",
    "url": "http://www.amazon.com/dp/B01ETPUQ6E",
    "name": "iPhone X - No Contract Phone - White - (AT&T)(Carrier locked phone)"
  },
  ...
]
```

## How to find the ASIN product number

A url from Amazon might look something like below:

https://www.amazon.com/Apple-iPhone-Silver-Certified-Refurbished/dp/B07D6TQP6F/ref=sr_1_1_sspa?s=wireless&ie=UTF8&qid=1535029477&sr=1-1-spons&keywords=iphone+x&psc=1&smid=A1B2EE2P0I30OG

Where we want to grab the number after `dp/` as that's the product ASIN.
