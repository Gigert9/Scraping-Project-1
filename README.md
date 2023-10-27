# Scraping-Project-1

An account of attempting to scrape first LinkedIn and then 10Times web pages in order to gain information surrounding events and attendees. All actions described or performed within were done so for research purposes only. Any data collected is publicly available and all techniques used relied on legitimate authentication.

## The Beginning

This project has gone through many iterations as its inceptions was directly linked to the timing of live events. I was originally commissioned to create a script that would scrape [LinkedIn](https://www.linkedin.com). The requirements called for the allowance of various parameters, such as identification of companies, personnel titles, and individual contact information. Simple at a glance, but naturally (being a commissioned project) the state of the input data was limiting. The expectation was to gather the required data given nothing more than a dataset of names. 

My immediate (perhaps foolish) reaction was to create a BASH script that would make use of **curl** requests. I figured it would be as easy as then using **grep** to parse the returned HTML code of the page for the specific values given for the various elements. Rinse and repeat per query, right? This is an embarrassingly amateur assumption. While it may be possible to create the script described, in order to completely fulfill the desired dataset with the most optimization, BASH is hardly the most efficient option.

## Snaking Our Way Towards Progress

After more rational thought, I attempted utilizing Python for a solution. In previous studies I had seen the capabilities of the language in the realm of web-based interactions, and it seemed like a perfect fit. I begin by reading various online sources, and eventually made my way to [GitHub](https://www.github.com) and located several handy repositories. The most helpful, beyond a shadow of a doubt, was [linkedin_scraper]( https://github.com/joeyism/linkedin_scraper) by “joeyjism”. I’m eternally grateful for the assistance and flawless code. It was very easy to understand and worked with little error. Sadly, it lacked a key desired piece of data. 

Still, by tweaking the provided code I was able to make great progress. Both while barely considering BASH and when initially approaching a Python environment, the action of logging in proved to be the first initial hurdle. However, once I implemented the libraries and tools provided by [joeyjism]( https://github.com/joeyism), this issue was immediately solved. 

As mentioned, this incredible utility was not natively designed to deliver a particular requested data element and was therefore not enough to satisfy the requirements of the project on its own. Additionally, the code required specific profile URLs to be scraped for data. While it was easy to provide a file to read as a variable to then supply said required URLs, we had no way of knowing the specific profile URLs. We only had the names.

This led to my next search through everyone’s favorite repository congregate, and the next major tool I located. 
