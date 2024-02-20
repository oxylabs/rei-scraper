# Rei Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Rei Scraper](https://oxylabs.io/products/scraper-api/ecommerce/rei?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Rei website effortlessly. This brief guide showcases how Rei Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Rei results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Rei page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.rei.com/b/columbia/f/scd-deals'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/rei-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html>\n<!-- If you are passionate about the outdoors and technology, visit https://rei.jobs ... </html>",
      "created_at": "2024-02-20 12:43:37",
      "updated_at": "2024-02-20 12:43:40",
      "page": 1,
      "url": "https://www.rei.com/b/columbia/f/scd-deals",
      "job_id": "7165687439246241793",
      "status_code": 200
    }
  ]
}
```
With our Rei Scraper, you can seamlessly retrieve public data from any Rei web page. Gather the indispensable book details including price, author, ratings, or summaries, to comprehensively understand the literary market and stay a step ahead of your competitors. If you require any assistance, feel free to reach out to our support team through live chat or drop us an email at hello@oxylabs.io.