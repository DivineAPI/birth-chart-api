# Birth Chart API - DivineAPI

> Free **Birth Chart API** for developers. 21+ REST endpoints for Western natal astrology: render natal wheel chart SVGs, compute planetary positions, aspects, houses, moon phases, fixed stars and more. Plain JSON over HTTPS, 25 languages, no SDK required.

[![Get API Key](https://img.shields.io/badge/Get%20API%20Key-cb22e6?style=for-the-badge&logoColor=white)](https://divineapi.com/register)
[![Live Docs](https://img.shields.io/badge/Live%20Docs-4F46E5?style=for-the-badge&logoColor=white)](https://developers.divineapi.com/western-api/natal-astrology)
[![API Status](https://img.shields.io/badge/API%20Status-10b981?style=for-the-badge&logoColor=white)](https://status.divineapi.com)
[![14-Day Free Trial](https://img.shields.io/badge/14--Day%20Free%20Trial-039BE5?style=for-the-badge&logoColor=white)](https://divineapi.com/register)
[![Postman](https://img.shields.io/badge/Run%20in%20Postman-FF6C37?style=for-the-badge&logoColor=white)](https://documenter.getpostman.com/view/26759678/2sBXitCnDX)

<p align="center">
  <img src="https://developers.divineapi.com/public/assets/web/images/divineIcon.svg" alt="DivineAPI, Birth Chart API for developers" width="120" />
</p>

---

## What is the Birth Chart API?

The **Birth Chart API** by DivineAPI is a suite of 21+ REST endpoints for Western natal astrology: complete birth-chart analysis and rendering. Give a birth date, time and location, get back a ready-to-display natal wheel chart (as SVG), plus every underlying calculation: planetary positions, house cusps, aspects, moon phases, fixed stars, asteroids, Arabic lots and more. Plain JSON over HTTPS, 25 languages, no SDK required.

Part of the broader [DivineAPI platform](https://github.com/DivineAPI/astrology-api) (300+ astrology, horoscope, tarot and numerology endpoints).

## Why choose DivineAPI's Birth Chart API?

- **21+ REST endpoints** covering every major Western natal astrology calculation
- **Render-ready SVG charts** from a single call, no client-side math required
- **Accurate computations** using authoritative ephemeris, multiple house systems (Placidus, Koch, Whole Sign, etc.)
- **Global coverage**: any city, any latitude/longitude, any timezone
- **25-language output**: English, Hindi, Spanish, French, Arabic, Chinese, and more
- **No SDK lock-in**: plain JSON over HTTPS, works with every language
- **Live status page**: uptime monitored at [status.divineapi.com](https://status.divineapi.com)
- **Postman collection** included: import and run in seconds

## All endpoints in the Birth Chart API

### Core Chart & Positions

| Endpoint | Docs |
|---|---|
| Natal Wheel Chart | [link](https://developers.divineapi.com/western-api/natal-astrology/natal-wheel-chart) |
| Planetary Positions | [link](https://developers.divineapi.com/western-api/natal-astrology/planetary-positions) |
| House Cusps | [link](https://developers.divineapi.com/western-api/natal-astrology/house-cusps) |
| Ascendant Report | [link](https://developers.divineapi.com/western-api/natal-astrology/ascendant-report) |
| Natal Insights | [link](https://developers.divineapi.com/western-api/natal-astrology/natal-insights) |
| Chart Shape | [link](https://developers.divineapi.com/western-api/natal-astrology/chart-shape) |

### Aspects & Patterns

| Endpoint | Docs |
|---|---|
| Aspect Table | [link](https://developers.divineapi.com/western-api/natal-astrology/aspect-table) |
| Aspect Patterns | [link](https://developers.divineapi.com/western-api/natal-astrology/aspect-patterns) |
| Declinations & Parallels | [link](https://developers.divineapi.com/western-api/natal-astrology/declinations-parallels) |
| Planetary Midpoints | [link](https://developers.divineapi.com/western-api/natal-astrology/planetary-midpoints) |

### Reports

| Endpoint | Docs |
|---|---|
| General Sign Report | [link](https://developers.divineapi.com/western-api/natal-astrology/general-sign-report) |
| General House Report | [link](https://developers.divineapi.com/western-api/natal-astrology/general-house-report) |
| Dominants | [link](https://developers.divineapi.com/western-api/natal-astrology/dominants) |

### Moon & Eclipses

| Endpoint | Docs |
|---|---|
| Moon Phases | [link](https://developers.divineapi.com/western-api/natal-astrology/moon-phases) |
| Moon Phase Calendar | [link](https://developers.divineapi.com/western-api/natal-astrology/moon-phase-calendar) |
| Eclipse | [link](https://developers.divineapi.com/western-api/natal-astrology/eclipse) |

### Advanced Points & Bodies

| Endpoint | Docs |
|---|---|
| Arabic Lots | [link](https://developers.divineapi.com/western-api/natal-astrology/arabic-lots) |
| Asteroid Positions | [link](https://developers.divineapi.com/western-api/natal-astrology/asteroid-positions) |
| Fixed Stars List | [link](https://developers.divineapi.com/western-api/natal-astrology/fixed-stars-list) |
| Fixed Stars Details | [link](https://developers.divineapi.com/western-api/natal-astrology/fixed-stars-details) |
| Other Minor Bodies | [link](https://developers.divineapi.com/western-api/natal-astrology/other-minor-bodies) |

Full reference, request/response samples, and live "try-it" console → **[developers.divineapi.com/western-api/natal-astrology](https://developers.divineapi.com/western-api/natal-astrology)**

---

## Quick start

1. **Get your API key** → [divineapi.com/register](https://divineapi.com/register) (14-day free trial, no credit card)
2. **Make your first call** - see the walkthrough below
3. **Browse all endpoints** → [developers.divineapi.com/western-api/natal-astrology](https://developers.divineapi.com/western-api/natal-astrology)

---

## Walkthrough: Natal Wheel Chart

The flagship endpoint. Submit birth details, get back a complete natal wheel chart as SVG, ready to drop into a webpage or save to disk.

```http
POST https://astroapi-8.divineapi.com/western-api/v2/natal-wheel-chart
```

Authenticate with a Bearer token in the `Authorization` header **and** pass `api_key` in the request body (both required).

### Request body (required)

| Parameter | Type | Required | Description | Example |
|---|---|:---:|---|---|
| `api_key` | string | ✓ | Your DivineAPI key | `YOUR_API_KEY` |
| `full_name` | string | ✓ | Person's full name | `Rahul Kumar` |
| `day` | integer | ✓ | Date of birth (day) | `24` |
| `month` | integer | ✓ | Month of birth | `5` |
| `year` | integer | ✓ | Year of birth | `2023` |
| `hour` | integer | ✓ | Birth hour (24-h clock) | `14` |
| `min` | integer | ✓ | Birth minute | `40` |
| `sec` | integer | ✓ | Birth second | `43` |
| `gender` | string | ✓ | Gender | `male` |
| `place` | string | ✓ | Place of birth | `New Delhi` |
| `lat` | float | ✓ | Latitude | `28.7041` |
| `lon` | float | ✓ | Longitude | `77.1025` |
| `tzone` | float | ✓ | Timezone offset from UTC | `5.5` |
| `lan` | string | - | Language code (default `en`) | `en` |

### Optional styling parameters

The chart renderer accepts 10+ optional parameters to customize the output: `house_system`, `aspect_orbs_type`, `aspect_orbs_value`, `aspects_type`, `planet_aspects`, `graphic_layout`, `degrees_color`, `planet_glyphs`, `main_background`, and more. See the **[full reference](https://developers.divineapi.com/western-api/natal-astrology/natal-wheel-chart)** for the complete catalog.

### Sample response

```json
{
  "status": "success",
  "code": 200,
  "message": "Request successful",
  "data": {
    "svg": "<svg xmlns=\"http://www.w3.org/2000/svg\" version=\"1.1\" width=\"705\" height=\"705\"><circle r=\"350\" cx=\"352.5\" cy=\"352.5\" fill=\"#f0f0f0\" stroke-width=\"2\" stroke=\"#000000\"></circle>...(full birth chart SVG, ~650 KB)...</svg>"
  }
}
```

The `svg` field is a complete, standalone SVG document. Save it to a `.svg` file, embed it directly in HTML, or rasterize to PNG with any SVG renderer.

---

## Code examples

### cURL

```bash
curl -X POST "https://astroapi-8.divineapi.com/western-api/v2/natal-wheel-chart" \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/x-www-form-urlencoded" \
  --data-urlencode "api_key=YOUR_API_KEY" \
  --data-urlencode "full_name=Rahul Kumar" \
  --data-urlencode "day=24" \
  --data-urlencode "month=5" \
  --data-urlencode "year=2023" \
  --data-urlencode "hour=14" \
  --data-urlencode "min=40" \
  --data-urlencode "sec=43" \
  --data-urlencode "gender=male" \
  --data-urlencode "place=New Delhi" \
  --data-urlencode "lat=28.7041" \
  --data-urlencode "lon=77.1025" \
  --data-urlencode "tzone=5.5"
```

### Python (requests)

```python
import requests

url = "https://astroapi-8.divineapi.com/western-api/v2/natal-wheel-chart"

headers = {
    "Authorization": "Bearer YOUR_API_KEY",
    "Content-Type": "application/x-www-form-urlencoded",
}

payload = {
    "api_key":   "YOUR_API_KEY",
    "full_name": "Rahul Kumar",
    "day":       24,
    "month":     5,
    "year":      2023,
    "hour":      14,
    "min":       40,
    "sec":       43,
    "gender":    "male",
    "place":     "New Delhi",
    "lat":       28.7041,
    "lon":       77.1025,
    "tzone":     5.5,
}

response = requests.post(url, headers=headers, data=payload)
svg = response.json()["data"]["svg"]

with open("natal-chart.svg", "w") as f:
    f.write(svg)
```

### JavaScript (browser, fetch)

```javascript
const url = "https://astroapi-8.divineapi.com/western-api/v2/natal-wheel-chart";

const body = new URLSearchParams({
  api_key:   "YOUR_API_KEY",
  full_name: "Rahul Kumar",
  day:   24, month: 5,  year:  2023,
  hour:  14, min:   40, sec:   43,
  gender: "male", place: "New Delhi",
  lat:  28.7041, lon: 77.1025, tzone: 5.5,
});

const response = await fetch(url, {
  method: "POST",
  headers: {
    "Authorization": "Bearer YOUR_API_KEY",
    "Content-Type":  "application/x-www-form-urlencoded",
  },
  body,
});

const { data } = await response.json();
document.getElementById("chart").innerHTML = data.svg;
```

### Node.js (fetch, Node 18+)

```javascript
// Node.js 18+ ships with fetch built-in, no dependencies needed.
import { writeFile } from "node:fs/promises";

async function getNatalChart() {
  const url = "https://astroapi-8.divineapi.com/western-api/v2/natal-wheel-chart";

  const body = new URLSearchParams({
    api_key:   "YOUR_API_KEY",
    full_name: "Rahul Kumar",
    day:   24, month: 5,  year:  2023,
    hour:  14, min:   40, sec:   43,
    gender: "male", place: "New Delhi",
    lat:  28.7041, lon: 77.1025, tzone: 5.5,
  });

  const res = await fetch(url, {
    method: "POST",
    headers: {
      "Authorization": "Bearer YOUR_API_KEY",
      "Content-Type":  "application/x-www-form-urlencoded",
    },
    body,
  });

  const { data } = await res.json();
  await writeFile("natal-chart.svg", data.svg);
  console.log("Saved natal-chart.svg");
}

getNatalChart();
```

### PHP (curl)

```php
<?php
$url = "https://astroapi-8.divineapi.com/western-api/v2/natal-wheel-chart";

$payload = http_build_query([
    "api_key"   => "YOUR_API_KEY",
    "full_name" => "Rahul Kumar",
    "day"       => 24,
    "month"     => 5,
    "year"      => 2023,
    "hour"      => 14,
    "min"       => 40,
    "sec"       => 43,
    "gender"    => "male",
    "place"     => "New Delhi",
    "lat"       => 28.7041,
    "lon"       => 77.1025,
    "tzone"     => 5.5,
]);

$ch = curl_init($url);
curl_setopt($ch, CURLOPT_POST, true);
curl_setopt($ch, CURLOPT_POSTFIELDS, $payload);
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
curl_setopt($ch, CURLOPT_HTTPHEADER, [
    "Authorization: Bearer YOUR_API_KEY",
    "Content-Type: application/x-www-form-urlencoded",
]);

$response = json_decode(curl_exec($ch), true);
curl_close($ch);

file_put_contents("natal-chart.svg", $response["data"]["svg"]);
echo "Saved natal-chart.svg\n";
```

### Go (net/http)

```go
package main

import (
    "encoding/json"
    "fmt"
    "io"
    "net/http"
    "net/url"
    "os"
    "strings"
)

type Response struct {
    Status string `json:"status"`
    Data   struct {
        SVG string `json:"svg"`
    } `json:"data"`
}

func main() {
    endpoint := "https://astroapi-8.divineapi.com/western-api/v2/natal-wheel-chart"

    form := url.Values{}
    form.Set("api_key",   "YOUR_API_KEY")
    form.Set("full_name", "Rahul Kumar")
    form.Set("day",       "24")
    form.Set("month",     "5")
    form.Set("year",      "2023")
    form.Set("hour",      "14")
    form.Set("min",       "40")
    form.Set("sec",       "43")
    form.Set("gender",    "male")
    form.Set("place",     "New Delhi")
    form.Set("lat",       "28.7041")
    form.Set("lon",       "77.1025")
    form.Set("tzone",     "5.5")

    req, _ := http.NewRequest("POST", endpoint, strings.NewReader(form.Encode()))
    req.Header.Set("Authorization", "Bearer YOUR_API_KEY")
    req.Header.Set("Content-Type",  "application/x-www-form-urlencoded")

    resp, err := http.DefaultClient.Do(req)
    if err != nil {
        panic(err)
    }
    defer resp.Body.Close()

    body, _ := io.ReadAll(resp.Body)
    var r Response
    json.Unmarshal(body, &r)
    os.WriteFile("natal-chart.svg", []byte(r.Data.SVG), 0644)
    fmt.Println("Saved natal-chart.svg")
}
```

---

## Other APIs by DivineAPI

[![Astrology API (hub)](https://img.shields.io/badge/Astrology%20API%20(hub)-cb22e6?style=for-the-badge&logoColor=white)](https://github.com/DivineAPI/astrology-api)
[![Kundali API](https://img.shields.io/badge/Kundali%20API-cb22e6?style=for-the-badge&logoColor=white)](https://github.com/DivineAPI/kundali-api)
[![Horoscope API](https://img.shields.io/badge/Horoscope%20API-cb22e6?style=for-the-badge&logoColor=white)](https://github.com/DivineAPI/horoscope-api)
[![Daily Tarot](https://img.shields.io/badge/Daily%20Tarot-cb22e6?style=for-the-badge&logoColor=white)](https://github.com/DivineAPI/daily-tarot)
[![Yes or No Tarot](https://img.shields.io/badge/Yes%20or%20No%20Tarot-cb22e6?style=for-the-badge&logoColor=white)](https://github.com/DivineAPI/yes-or-no-tarot)
[![Fortune Cookie](https://img.shields.io/badge/Fortune%20Cookie-cb22e6?style=for-the-badge&logoColor=white)](https://github.com/DivineAPI/fortune-cookie)
[![Coffee Cup Reading](https://img.shields.io/badge/Coffee%20Cup%20Reading-cb22e6?style=for-the-badge&logoColor=white)](https://github.com/DivineAPI/coffee-cup-reading)

---

## Resources

- **Full documentation** → [developers.divineapi.com/western-api/natal-astrology](https://developers.divineapi.com/western-api/natal-astrology)
- **Parent platform README** → [github.com/DivineAPI/astrology-api](https://github.com/DivineAPI/astrology-api)
- **API status** → [status.divineapi.com](https://status.divineapi.com)
- **Postman collection** → [Run in Postman](https://documenter.getpostman.com/view/26759678/2sBXitCnDX)
- **Changelog** → [developers.divineapi.com/changelog](https://developers.divineapi.com/changelog)
- **Support** → [admin@divineapi.com](mailto:admin@divineapi.com)

---

## License & Usage

Code samples on this page are free to copy into your own projects, no attribution required. Marketing copy, logos, and the **DivineAPI** name are © 2026 DivineAPI, all rights reserved.

For the terms that govern the API service itself, see [divineapi.com/terms](https://divineapi.com/terms-service).

## Contact

Questions, feature requests or partnership enquiries → **[admin@divineapi.com](mailto:admin@divineapi.com)**
