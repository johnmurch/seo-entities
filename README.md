# seo-entities

>Update 6/24/2018 - Beta Launch at [https://www.urlrecover.com/seo-entities/](https://www.urlrecover.com/seo-entities/)

Built as a Proof of Concept - based on https://twitter.com/wilreynolds/status/1010243672179388418

>Hey folks, need help. I'm looking for a tool where I can drop in 200k URLs and >get entities for each URL, easily exportable in a CSV, I know Google and IBM >watson do this, but I don't they don't have easy interfaces for me to pull >this quickly w/o writing some code / scripts. TY!

### Overview

Build a system that will take a URLs and generate entities from the content.

Input: Import CSV file of URLs

Output: Generate CVS export of URL and entities

## Current Status

I took 3 sample URLs from [Seer Interactive blog](http://www.seerinteractive.com/blog/), process entities using Google's Natural Language API and generate a CSV.

**I could easily throw togther a UI for the CSV upload, but will need a credit card as Google Pricing for NLP entities processing is a bit much for 200k URLs, especially if they are content heavy.**

To give some context - [Google Pricing](https://cloud.google.com/natural-language/pricing) charges a call per 1000 characters, I listed out the character counts I had for each article below, even with some preprocessing to just focus on the article.   

So if the URLs contain 1000 characters or less, it's still **$200 in API costs** to run these 200k URLs let alone the crawling of the site.

## Files
1. [entities1.json](entities1.json) - Response from Google NLP for [http://www.seerinteractive.com/blog/facebooks-custom-audience-lists-oh-people-youll-reach/
](http://www.seerinteractive.com/blog/facebooks-custom-audience-lists-oh-people-youll-reach/) - *7051 characters so really it's 8 NLP calls!*
2. [entities2.json](entities2.json) - Response from Google NLP for [http://www.seerinteractive.com/blog/target-cpa-work/
](http://www.seerinteractive.com/blog/target-cpa-work/) - *4405 characters so really its 5 NLP calls!*
3. [entities3.json](entities3.json) - Response from Google NLP for [http://www.seerinteractive.com/blog/organize-sites-navigation-based-audience-insights/](http://www.seerinteractive.com/blog/organize-sites-navigation-based-audience-insights/) - *7589 characters so really its 8 NLP calls!*
4. [sample.csv](sample.csv) - Example output of URL + entities


## Next Steps

I am happy to run these 200k URLs this weekend, but as mention it does cost a bit to run the API, so lets chat :).

Also would like a bit more input around the data Google provides as I just pulled the name, but their is other value in the type that is not included.



## Donations

![Buy me a coffee](https://www.buymeacoffee.com/assets/img/BMC-btn-logo.svg)[Buy me a coffee](https://www.buymeacoffee.com/johnmurch)
