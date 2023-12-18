# Stackshare Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Stackshare Scraper](https://oxylabs.io/products/scraper-api/web/stackshare?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Stackshare website effortlessly. This brief guide explains how an Stackshare Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Stackshare results by providing your own URLs to our service. We can return the HTML for any Stackshare page you like.

#### Python code example

The example below illustrates how you can get HTML of Stackshare page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://stackshare.io/tools/trending'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/stackshare-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html>\n<html lang='en'>\n<head>\n<script type=\"text/javascript\">window.NREUM||(NREUM={});NREU ... </html>",
      "created_at": "2023-12-18 11:14:15",
      "updated_at": "2023-12-18 11:14:19",
      "page": 1,
      "url": "https://stackshare.io/tools/trending",
      "job_id": "7142472126669288449",
      "status_code": 200
    }
  ]
}
```
Utilize our Stackshare Scraper to seamlessly extract public data from any Stackshare Web Page. Gather essential tool information, including their features, user reviews, or usage stats, to gain a competitive edge in the technology landscape. If you need assistance or have any queries, our dedicated support team is available round-the-clock on live chat or you can reach us via email at hello@oxylabs.io.