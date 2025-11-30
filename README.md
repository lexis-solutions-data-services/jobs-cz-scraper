# Jobs.cz Scraper

![banner](https://i.ibb.co/qVKd58b/jobs-cz.png)

The **Jobs.cz Scraper** is an Apify actor that extracts job listings directly from [Jobs.cz](https://www.jobs.cz/), one of the most popular job portals in the Czech Republic. This tool allows you to search for jobs based on a **keyword query** and **specific location** (in Czech) and retrieve detailed job information easily.

<p align="center">
  <img src="https://apify-image-uploads-prod.s3.us-east-1.amazonaws.com/DevbkY3adMTBuoECt-actor-PMByQ1KSxOfat8KbR-rehgAV8XqU-svdptQm-_400x400.jpg" alt="Jobs.cz Scraper" style="height: 60px; margin-right: 15px;" /><a href="https://apify.com/lexis-solutions/jobs-cz-scraper" target="_blank">
    <img src="https://img.shields.io/badge/Try%20it%20on-Apify-0066FF?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNDA4IiBoZWlnaHQ9IjQwOCIgdmlld0JveD0iMCAwIDQwOCA0MDgiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxnIGNsaXAtcGF0aD0idXJsKCNjbGlwMF8zNDFfNDE1NykiPgo8cGF0aCBkPSJNMjE4LjY5NSAxMDRIMzAwLjk3QzMwMi42NDMgMTA0IDMwNCAxMDUuMzU3IDMwNCAxMDcuMDNWMjMyLjc2NkMzMDQgMjM1Ljc3OCAzMDAuMDgzIDIzNi45NDUgMjk4LjQzNCAyMzQuNDI1TDIxNi4xNTkgMTA4LjY5QzIxNC44NDEgMTA2LjY3NCAyMTYuMjg3IDEwNCAyMTguNjk1IDEwNFoiIGZpbGw9IndoaXRlIi8+CjxwYXRoIGQ9Ik0xODkuMzA1IDEwNEgxMDcuMDNDMTA1LjM1NyAxMDQgMTA0IDEwNS4zNTcgMTA0IDEwNy4wM1YyMzIuNzY2QzEwNCAyMzUuNzc4IDEwNy45MTcgMjM2Ljk0NSAxMDkuNTY2IDIzNC40MjVMMTkxLjg0IDEwOC42OUMxOTMuMTU5IDEwNi42NzQgMTkxLjcxMyAxMDQgMTg5LjMwNSAxMDRaIiBmaWxsPSJ3aGl0ZSIvPgo8cGF0aCBkPSJNMjAyLjU5MSAyMDQuNjY4TDEwOS4xMjcgMjk4LjgzNUMxMDcuMjI5IDMwMC43NDcgMTA4LjU4MyAzMDQgMTExLjI3OCAzMDRIMjk2LjhDMjk5LjQ4MyAzMDQgMzAwLjg0MiAzMDAuNzcgMjk4Ljk2NyAyOTguODUyTDIwNi45MDggMjA0LjY4NUMyMDUuNzI2IDIwMy40NzUgMjAzLjc4MiAyMDMuNDY4IDIwMi41OTEgMjA0LjY2OFoiIGZpbGw9IndoaXRlIi8+CjwvZz4KPGRlZnM+CjxjbGlwUGF0aCBpZD0iY2xpcDBfMzQxXzQxNTciPgo8cmVjdCB3aWR0aD0iMjAwIiBoZWlnaHQ9IjIwMCIgZmlsbD0id2hpdGUiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDEwNCAxMDQpIi8+CjwvY2xpcFBhdGg+CjwvZGVmcz4KPC9zdmc+Cg==&logoColor=white" alt="Try it on Apify" style="border-radius: 12px; height: 60px;" />
  </a>
</p>


---


## 📊 Actor Stats

| Stat | Value |
|------|-------|
| **Version** | `0.0.4` |
| **Last Update** | Nov 30, 2025 |

---


## ✨ Key Features

- 🔎 **Keyword Search**: Find jobs related to any profession, industry, or role.
- 🏙️ **Location Filtering**: Filter jobs based on the Czech city or region (e.g., "Praha", "Brno").
- 📑 **Detailed Job Information**: Extract job title, company, location, job description, and direct job URL.
- ⏳ **Control Result Limits**: Set how many jobs you want to retrieve.
- 🇨🇿 **Localized Scraping**: Designed specifically for the Czech market.

---

## 💡 Why This Actor Is Important

The Czech job market is thriving, but it's often challenging to gather structured job data for research, recruitment, or analytics.  
**Jobs.cz Scraper** makes it simple to collect up-to-date job listings in a fully automated, reliable, and scalable way — **without manual browsing**.

You can monitor new jobs, analyze hiring trends, or populate your own database of Czech job offers — in minutes.

---

## 👤 Who Is It Best Suitable For?

- 🧑‍💻 **Developers** building job aggregator platforms
- 🏢 **Recruitment Agencies** tracking opportunities
- 📊 **Market Researchers** analyzing the Czech labor market
- 📈 **Business Analysts** gathering competitive hiring data
- 🤖 **Automation Enthusiasts** connecting job data into workflows

---

## Input 📥

To use this actor, you need to provide the following input:

- Field: **query**
  - Type: string
  - Required: No
  - Description: Search query
- Field: **location**
  - Type: string
  - Required: No
  - Description: Location
- Field: **maxItems**
  - Type: integer
  - Required: No
  - Description: Maximum number of items to scrape
  - Default: 10

## 🛠 Input Schema

```json
{
  // query or location is not required, but at least one of them has to be filled
  "query": "Building Engineer",
  "location": "Praha",
  "maxItems": 10 // default
}
```

## Output 📤

An example output looks like this:

```json
{
  "id": "2000281890",
  "title": "Enterprise Network Engineer",
  "brand": "Vodafone Czech Republic a.s. 5411",
  "category": "JD/Telekomunikace/System Engineer",
  "dimension23": "badge",
  "url": "https://vodafone.jobs.cz/detail-pozice?r=detail&id=2000281890&rps=0&impressionId=",
  "isLocal": false,
  "provider": "Vodafone Czech Republic a.s.",
  "providerImage": "https://vodafone.jobs.cz/assets/components/share-icons/images/logo-share-1200x630.png?av=d586e2dcd347f334",
  "description": "Position characteristics We can offer this position as part time job in case of your interest. What will you do here?   Enterprise Technical Project Manager handles easing the delivery of value from Vodafone Networks towards Vodafone Business (Sales, VBTS (Vodafon……",
  "descriptionHTML": "<h2>Position characteristics</h2>\n<p>We can offer this position as part time job in case of your interest.</p>\n<h2>What will you do here?</h2>\n<ul>\n<li>...",
  "location": "náměstí Junkových 2808/2, 15500 Praha - Stodůlky, Česká republika",
  "bullets": [
    "Employment Types -> Full-time work,Part-time work",
    "Employment Durations -> Permanent",
    "Contract Types -> employment contract",
    "Required Education -> Bachelor's",
    "All Languages Required -> true",
    "Required Languages -> English"
  ],
  "benefits": [
    "13th monthly salary",
    "Cafeteria",
    "Cell phone",
    "Contribution to sport / culture / leisure",
    "Contributions to the pension / life insurance",
    "Discount on company products / services",
    "Education allowance",
    "Educational courses, training",
    "Flexible start/end of working hours",
    "Holidays 5 weeks",
    "Meal tickets / catering allowance",
    "Notebook",
    "Sick days",
    "The possibility of study leave",
    "Work mostly from home"
  ],
  "professions": ["System Engineer"],
  "fields": ["Telecommunications"],
  "applyLink": "https://vodafone.jobs.cz/detail-pozice/odpovedni-formular?r=reply&id=2000281890",
  "publishedAt": "2025-04-09T10:48:40+02:00"
}
```

## Need to scrape other job platforms?

Here are some other job platform scrapers you might find useful:

- Germany 🇩🇪

  - [Arbeitsagentur Scraper](https://apify.com/lexis-solutions/bundesagentur-fur-arbeit-arbeitsagentur-scraper)

- Netherlands 🇳🇱

  - [Werk.nl Scraper](https://apify.com/lexis-solutions/werk-nl-scraper)

- United Kingdom 🇬🇧

  - [Reed.co.uk Scraper](https://apify.com/lexis-solutions/reed-co-uk-scraper)
  - [TotalJobs Scraper](https://apify.com/lexis-solutions/totaljobs-scraper)

- France 🇫🇷

  - [HelloWork Scraper](https://apify.com/lexis-solutions/hellowork-scraper)

- Switzerland 🇨🇭

  -[Jobs.ch Scraper](https://apify.com/lexis-solutions/jobs-ch-scraper)

---

👀 p.s.

Got feedback or need an extension?

Lexis Solutions is a [certified Apify Partner](https://apify.com/partners/find). We can help you with custom solutions or data extraction projects.

Contact us over [Email](mailto:scraping@lexis.solutions) or [LinkedIn](https://www.linkedin.com/company/lexis-solutions)

## Support Our Work 💝

If you're happy with our work and scrapers, you're welcome to leave us a company review [here](https://apify.com/partners/find/lexis-solutions/review) and leave a review for the scrapers you're subscribed to. It will take you less than a minute but it will mean a lot to us!

Image Credit: https://www.jobs.cz/
