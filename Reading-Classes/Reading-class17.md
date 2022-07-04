# Web Scraping
Web scraping is a technique to automatically access and extract large amounts of information from a website, 
which can save a huge amount of time and effort. 
In this article, we will go through an easy example of how to automate downloading hundreds of files from the New York 
MTA. This is a great exercise for web scraping beginners who are looking to understand how to web scrape. 
Web scraping can be slightly intimidating, so this tutorial will break down the process of how to go about the process.

## Important notes about web scraping:
Read through the website’s Terms and Conditions to understand how you can legally use the data. 
Most sites prohibit you from using the data for commercial purposes.
Make sure you are not downloading data at too rapid a rate because this may break the website. 
You may potentially be blocked from the site as well.

### Here are a few easy giveaways that you are bot/scraper/crawler –

- Scraping too fast and too many pages, faster than a human ever can
- Following the same pattern while crawling. For example – go through all pages of search results, and go to each result only after grabbing links to them. No human ever does that.
- Too many requests from the same IP address in a very short time
- Not identifying as a popular browser. You can do this by specifying a ‘User-Agent’.
- using a user agent string of a very old browser

The points below should get you past most of the basic to intermediate anti-scraping mechanisms used by websites 
to block web scraping.

- Make the crawling slower, do not slam the server, treat websites nicely
- Do not follow the same crawling pattern
- Make requests through Proxies and rotate them as needed
- Rotate User Agents and corresponding HTTP Request Headers between requests
- Use a headless browser like Puppeteer, Selenium or Playwright
- Beware of Honey Pot Traps
- Check if Website is Changing Layouts
- Avoid scraping data behind a login
- Use Captcha Solving Services

