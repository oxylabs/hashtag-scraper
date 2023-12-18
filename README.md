# Hashtag Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Hashtag Scraper](https://oxylabs.io/products/scraper-api/web/hashtag-scraper?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Hashtag website effortlessly. This brief guide explains how an Hashtag Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Hashtag results by providing your own URLs to our service. We can return the HTML for any Hashtag page you like.

#### Python code example

The example below illustrates how you can get HTML of Hashtag page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://hashtagify.me/hashtag/summer'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/hashtag-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!doctype html>\n<html lang=\"en\">\n<head>\n  <meta charset=\"UTF-8\">\n  <meta name=\"viewport\" content=\"wi ... </html>",
      "created_at": "2023-12-18 11:38:54",
      "updated_at": "2023-12-18 11:38:54",
      "page": 1,
      "url": "https://hashtagify.me/hashtag/summer",
      "job_id": "7142478328442726401",
      "status_code": 200
    }
  ]
}
```
With our Hashtag Scraper, you can effortlessly pull public data from any Hashtag social media post. Collect the necessary data such as likes, comments, shares, or post contents, to examine social media trends and get ahead of your competitors. If you need any assistance, our support team is readily available via live chat or you can email us at hello@oxylabs.io.