#Data journalism class #5

## Review of last week's work
* Scraping, and the power of looking behind the hood. Example story: [Cash Drops and Keystrokes](http://www.nytimes.com/interactive/2015/10/15/us/sports-betting-daily-fantasy-games-fanduel-draftkings.html)
* Some of you asked if we'd get in the detail about the $21 equivalent of a $300,000 donation for a billionaire. Yes.
* Practice, practice practice: Go over any work you've done that would have lent itself to trying to work in a spreadsheet. 


## Review of final memos	
We'll discuss each of the proposals with an eye toward newsworthiness, the data you have identified, and possible data sources you may not have thought of. 

## Skills: Basic visualization with google fusion tables
* Have to log in with a non-Columbia gmail account. 
* Why Google Fusion tables? Only reason: They're free and able to be used almost anywhere without any software or permissions issues. Google Fusion Tables give you a way to make simple maps and charts that can be published on your website. But they're terrible for anything of any size, and they are particularly difficult to style.
*  Alternatives for viz:
	* Tableau : You can sign up for Tableau Public for small, public visualizations. If you're a member of IRE, you can get Tableau desktop -- usually about $2,000 -- for free. 
	* R graphics, particularly ggplot2 and shiny for interactivity. 
	* Python pandas does about the same thing.
	* Except when it's really not important, forget about Excel graphics with one exception: it makes great ["sparklines"](https://en.wikipedia.org/wiki/Sparkline).
	* There are several online visualization products that advertiste to journalists, including Highcharts and  silk.co, which are free for personal or small-scale use.  


### Our first exercise

Sometimes, you simply can't see any patterns without visualizing data. This happens most frequently with geographic information -- seeing a list of addresses means nothing until they are put on a map. 

We're going to do some simple mapping with Google Fusion Tables, even though it's not ideal.

* The first exercise involves making a simple map of restaurant inspections in the Morningside Heights neighborhood. You can either download the [morningside\_heights\_restaurants.csv](morningside_heights_restaurants.csv) in this folder. 

* The second example is zip code data, with a little more sophistication. 
