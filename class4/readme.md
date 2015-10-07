# Class #4 

## Part 1: Review work since last class	

* Did anyone go through the other exercises? 
* How did you do on the snow storm report? You would have had to have used the VLOOKUP function before you could make a pivot table. Go through it in class. 
* Anyone have a lede?

Review more of Excel, what you want to go over again. 

## Part 2: PDF's 
There are two documents here on PDF's. One is Rob's handout, called [pdf_wrangling.docx](pdf_wrangling.docx?raw=true). The other is my handout, called [pdf_tips.md](pdf_tips.md) . They have about the same things in them.

Two types of pdfs':

1.  Those that are born digital, as in many government reports and statistics. Many of the PDF's you find on the web are born digital, and can be read by many different programs with varying levels of success. 
2.  Those that are converted into digitial form -- scanned images of paper. These are often from FOIA requests, where agencies have censored some information and then re-copied. You might also have to scan paper yourself. You will likely have to pay for a product to deal with these. 

Example: 
Using cometdocs, a free service, on an old report we got from the DC housing agency on housing code violations. 

* The [original pdf](List_fy2006.pdf) was sent through [CometDocs](http://cometdocs.com). There are other options listed on the tip sheets mentioned above. 
* The [Excel workbook](List_fy2006.xlsx?raw=true) that I got back. 

Work through the workbook to start thinking about data cleaning: 

* What are the headers of each page and do we care?
* What should you do to make sure you can always get back to the place on the original page? 
* What other kinds of error checking can you build in? 

Tricks: 

* Filtering for certain rows.
* Select special - blanks, then =(cell above) then CTL-Enter.

Go back to some of the handouts from last week to see other Excel tricks for data cleaning. 

This is why PDFs are evil. Don't get them if you don't have to. Fight for something that is a data set, not a printout. 

## Part 3: Basic scraping

There are two parts to scraping a website -- first, getting the pages you want, then pulling them into a spreadsheet or a set of documents. You sometimes have to navigate through a site -- called "spidering" -- to get to each page. We won't be doing that in this class. Typically people use programming languages to script that job. There are two products that claim they will work for this, but I've found them to be very difficult to get right, when I can get them right at all: 

* [Outwit Hub](https://www.outwit.com/), $89 for a standalone copy. 
* [import.io](import.io), free service. 
* [kimono](https://www.kimonolabs.com/) another free service. I haven't been able to get it to work and it's creepy when they watch what you are doing and ask if you want help. 

There are also some tricks in Google Sheets that will get you part way there, but the number of entries allowed is so limited that it's not useful. For more tools and tricks, consider buying ["Scraping for Journalists"](https://leanpub.com/scrapingforjournalists) for $20. It's badly outdated, but the concepts still work.  (For example, ScraperWiki basically doesn't exist in any form resembling what it was when the book was written, so that whole chapter is no longer useful.)  IRE also has several pretty good handouts. 

The problem with scraping tools is that every site is different, and it's difficult to make a general tool that's both easy to use AND works on the crazy sites you find in real life. So most people start learning how to program.

### Looking under the hood
The key to scraping is looking at the code underneath your web page, not the page you see on your screen. We're going to use Chrome to do this, but Firebug in Firefox is many peoples' choice. 

#### Example 1:
Thanks to Prof. Susan McGregor, who has [a great video](https://www.youtube.com/watch?v=fRYdCwuacyg) on the subject of looking under the hood at data structures found in web pages. We're going to use her example of extracting XML from Trader Joe's store sites. We'll work on how to import it into Google Sheets after we've gone through some other exercises. 

Lesson: There is often structured data underneath a page, so you don't even have to scrape. (MS Excel imports some simple XML on Windows, not Mac. We'll look at OpenRefine in our last week, and that is another way to get it.)

#### More examples

Going through the tutorial on scraping using Google Chrome's Scraper add-in, and learning about how to look at a web page's structure. 

* [Tutorial](scraping-chrome.pdf), which has an outdated structure for Craigslist pages, but otherwise is still worth it. 
* [More on xpath](xpath.md) in this repo. 



