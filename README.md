# seo-entities
Proof of Concept - based on https://twitter.com/wilreynolds/status/1010243672179388418

>
Hey folks, need help. I'm looking for a tool where I can drop in 200k URLs and get entities for each URL, easily exportable in a CSV, I know Google and IBM watson do this, but I don't they don't have easy interfaces for me to pull this quickly w/o writing some code / scripts. TY!

### Proof of Concept

Build a system that will take a URLs and generate entities from the content.

Input: Import CSV file of URLs

Output: Generate CVS export of URL and entities


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
4. sample.csv - Example output of URL + entities


## Next Steps

I am happy to run these 200k URLs this weekend, but as mention it does cost a bit to run the API, so lets chat :).

Also would like a bit more input around the data Google provides as I just pulled the name, but their is other value in the type that is not included.



## Donations

<style>.bmc-button img{width: 27px !important;margin-bottom: 1px !important;box-shadow: none !important;border: none !important;vertical-align: middle !important;}.bmc-button{line-height: 36px !important;height:37px !important;text-decoration: none !important;display:inline-flex !important;color:#FFFFFF !important;background-color:#FF813F !important;border-radius: 3px !important;border: 1px solid transparent !important;padding: 1px 9px !important;font-size: 23px !important;letter-spacing: 0.6px !important;box-shadow: 0px 1px 2px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 1px 2px 2px rgba(190, 190, 190, 0.5) !important;margin: 0 auto !important;font-family:'Cookie', cursive !important;-webkit-box-sizing: border-box !important;box-sizing: border-box !important;-o-transition: 0.3s all linear !important;-webkit-transition: 0.3s all linear !important;-moz-transition: 0.3s all linear !important;-ms-transition: 0.3s all linear !important;transition: 0.3s all linear !important;}.bmc-button:hover, .bmc-button:active, .bmc-button:focus {-webkit-box-shadow: 0px 1px 2px 2px rgba(190, 190, 190, 0.5) !important;text-decoration: none !important;box-shadow: 0px 1px 2px 2px rgba(190, 190, 190, 0.5) !important;opacity: 0.85 !important;color:#FFFFFF !important;}</style><link href="https://fonts.googleapis.com/css?family=Cookie" rel="stylesheet"><a class="bmc-button" target="_blank" href="https://www.buymeacoffee.com/johnmurch"><img src="https://www.buymeacoffee.com/assets/img/BMC-btn-logo.svg" alt="Buy me a coffee"><span style="margin-left:5px">Buy me a coffee</span></a>
