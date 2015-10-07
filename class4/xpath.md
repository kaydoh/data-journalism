# More on scraping

## more tools
* Outwit hub (now about $90, but powerful)
* Kimono (a little creepy - they keep tabs of what you are doing and keep asking to help. I've also found it doesn't work a lot. I've had trouble with the simplest things.)
* import.io - said to be the easiest out there, but I've had trouble using it. 

By the time I get through trying to learn a tool, I might as well have learned to program it. Key parts of Python that will help with difficult sites:

* Scrapy - a whole library of scraping tools that has its own manual and syntax. I think this one uses XPath though, so it will be easier to incorporate that in.
* Selenium, for when you need to actually run a browser. 


Building on the [tutorial](scraping-chrome.pdf). Note that this tutorial has an outdated structure for craigslist, which no longer embeds the lat-long into the headers. (Boo) 

These examples came up recently and I needed to memorialize it for myself.  It's just to help me remember.

Start with Chrome inspection tool, right click on the element you want, then copy the XPath to give you a start. 

## Finding Text Between Tags


    <td nowrap="">
		<font face="arial" size="2">
			<b>ABRAMSON, JOEL ELIOT &nbsp; &nbsp; <br> </b>
			JOEL E. ABRAMSON, P.C. &nbsp; &nbsp; <br> 
			271 MADISON AVE FL 22 &nbsp; &nbsp; <br>
			NEW YORK, NY 10016 &nbsp; &nbsp; <br>
			(212)599-7700 &nbsp; &nbsp;
		</font>
	</td>

If the whole chunk is the 2nd column, it's [2] 

How can I get the name, which is outlined by the   < b >  (bold) tag? That text is the first text() element below the "font" tag, Any of these will work:  

     [2]/font/text()
		or
	 [2]//text()
		or
	 [2]/font/b/text()

A little less intuitively:

     *[2]font[1]/child::text()
		or
	 *[2]/node()/node()
		or
	 *[2]/font/node()[position=1]

The bold tag is the first child of the font tag. Technically, the "node" is everything between the font tags, then the second node is everything between the bold tags.

Here's how to get the city, state, zipcode from that chunk. (Use the last-1 because some firms had two-line addresses and others had only one. It would fail in cases where the city, state was the last row. 

		*[2]/font/text()[position()=last()-1]
				or
		*[2]//text()[count(following-sibling::br)=1]
		

What if you had a slightly different piece of code, this one a line from the [Florida State football roster](http://www.seminoles.com/SportSelect.dbml?SPID=157113&SPSID=917030)

	<tr class="odd">
		<td class="number">3</td>
		<td class="name">
			<span class="sortname" style="display:none;">Darby Ronald</span>
			<a title="Ronald Darby" href="/ViewArticle.dbml?ATCLID=209573037&amp;DB_OEM_ID=32900">Ronald Darby</a>
		</td>
		<td class="position">CB</td>
		<td class="height" nowrap="">5-11</td>
		<td class="weight">195</td>
		<td class="year">
			<span style="display:none;">3</span>
			Jr.
		</td>
		<td class="hometown ">Oxon Hill, Md. / Potomac</td>
	</tr>

I'll come back to this example later, so it's worth having the whole snippet here. But all I care about right now is to pick up the "Jr" separate from the "3" in the class year. 

The first part is obvious, assuming we're starting from the row.

	  *[6]/span
		 or
	  *[@class="year"]/span

How about getting just the word, without the number? 

	  *[6]/node()[position()=3]

or position()=last would work. It's the 3rd node, not the second, because there is a span element in between. If it were text(), it would be the second.

Recap:

* To get everything as text, without the tags in between, just use the position or name. 
* To get the first text element, use **text()** or **text()[position()=1]**. It's the same thing.
* To get the last text element, use **text()[position()=last]**
* To get a list of all of the elements, which has an entry for each tag and another for its text representation, use **node()** instead of **text()**. If for some reason you only want the list of tags without what they contain, use **element()**

## Finding elements ##

Key XPath selectors are:

* **descendant-or-self**, which refers to everything below as well as yourself. It helps when you don't know what level it might be. For example, in the html above, finding the "sortname" class wouldn't depend on you knowing that it was two levels below. 

		descendant-or-self::node()[@class="sortname"]

* **count(preceding-sibling::p)** would count how many < p > tags came before. The opposite is **following-sibling::tag**. Leave off the the tag if you want just the number of elements, but they will be at the same level. You can use the count as a test, so that if you want the first two paragraphs, it can be: 
* 
		text()[count(preceding-sibling::p)<3]

* **attributes of a tag, like onclick() action** This was an interesting one, from the NYC ACRIS real estate document database. In this case, we were looking in an exercise for a company called Prevezon. There were about 30 records, just enough to make clicking into them a pain. If you get fewer than 100 records, you can scrape all using Chrome scraper. The key, though, is the link to the detail page. That is under the input button as an onclick event. Here is how I made the XPATH to get to that. 

		substring(*[1]/div/font/input[1]/@onclick, 23,16))

	This says, for each of the 1st tds, look for div/font/input[1] -- he first input item (there are two). Then find the @click attribute, and take the 16 characters beginning at 23. To create the actual link, you can use concat("root html", your substring)

