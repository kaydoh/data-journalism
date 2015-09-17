[Print](https://gitprint.com/sarahcnyt/data-journalism/blob/master/class1/lecturenotes-week1.md)

#Class #1 lecture notes 

These are Sarah's lecture notes for the first class. We may or may not follow them. 

## Introductions 
* You, me
* Ground rules for the class
* Introduction to data journalism, in particular the use of data and documents for reporting stories. 


## First steps with Excel

### Spreadsheet navigation, tricks.

* Reminder of how to move around a spreadsheet efficiently, including keyboard shortcuts and some best practices. 
* 
	* Keyboard shortcuts, wrapping text, freezing columns, ### and E formats.
	* Saving as you go.
	* The 1904 date problem.
	* The 65,536 problem.

### Data types
Types of data: Illustrated on [this spreadsheet](data-types.xlsx) for examples 

 * Words / text. These can be free-form, or they can be relatively consistent, like tags on a blog.
 * Numbers: Things you will add together or do math on. 
 * Dates: A special kind of number you can look at in a lot of ways. 

### Tidy data

Unteach you what you think you know about spreadsheets and Excel - not for printing or presentation, but for data.

Use the court salary database as an example of tidy data. The big problem is in the titles, and I took out some other problems.

1. Save as a copy (version, initials)
2. Add a unique id. (1, 2, doubleclick)
3. Freeze panes

Why is it good to repeat, say, the jurisdiction? Repetitive?
Last, First is a good way to do it.  
Later will talk about other ways you might be tempted to do it.

The term "Tidy data" comes from Hadley Wickham, a statistician who has been involved in developing products and add-ons for the R programming language. He uses Leo Tolstoy as a way to introduce untidy data: "Tidy datasets are alike, but every messy dataset is messy in its own way." 

He's defined some ways of thinking about data that let us use it in its most efficient form. You'll find that if you follow this, your data set will often have many *rows*, but only a few *columns*.  I call this a tall and skinny dataset, as opposed to a short and fat one.

* Each row represents one item: a test, an inspection, a person, or an event.
* Each column represents one attribute or variable about each item. 
* Each worksheet or table represents one type of observational unit. For example, an inspection might include many fines -- one table would be information about the inspection, the other about the fines. This is what is called database "normalization"

We often ignore this last element when working with smallish datasets, and just repeat any information we need. 

You will rarely get tidy data. I'll give you some examples of real-world datasets we get all the time. But for now, we'll go through the exercise of thinking about what you might want to record and how you might want to record information about the court case you are going to follow. 

This will be different depending on the larger theme. But having a good handle on the basic facts of your case are useful. 

Talk about how this works - what can and can't you do with each of the columns? Why is it done this way? 

* A couple of examples of [bad spreadsheets](bad-spreadsheet-examples.xlsx?raw=true) - why we care about tidy data. 

### Typical government spreadsheets 

Hadley doesn't mention the most common problem in the data we get and sometimes create -- that the records are provided as a printout of a report, not as a dataset. Even when we get them in Excel. note the gambling records [here](https://www.dropbox.com/s/qzhhypthkagk62i/gambling-arrests-orig.xlsx?dl=0) and [here](https://www.dropbox.com/s/vs62z7ixrfa9a56/arrests_normalized.xlsx?dl=0). Go through the original and explain what is wrong with it.

The bad examples spreadsheet will take a long time to open, because of the way California did its ACA data.  

* California rates - how to make it small, what to do with it? Imagine what you'd like.
* Sort the tarp? What happens to the formulas. Fill in the blanks.How would you tidy? Units of analysis.
* Disaster declarations. Opposite problem. Filter vs. sort and summarize. Regex. Could they do any analysis themselves? Writing  a release, not analyzing geographic disparities. Investigative opportunities are in the air when you get a dataset like this: it means they've never examined it themselves. 
* Vetpop - how to get data from pivot tables. (Forecasting, not going back in time).


### Followup resources

* A series of [YouTube videos](https://www.youtube.com/playlist?list=PL-Je9dqyEF8YS7Cy8BppKg5zrhiQC__n6) created by Sarah on spreadsheet design . The third one is on how to set up a spreadsheet yourself. There's a mistake in the veterans' description (it is forecast, not a bad date.)

* Handouts are in this folder. 


## Designing your first spreadsheet for reporting

* Numbering each entry. Why? 
* Balancing how hard it is to enter, and how you will want to use it. Example: What about approximate dates? How do you know? 
* Fact-checking built in in advance.
* What is your goal? 
* Who are you holding accountable? For what?

Work with Kevorkian together, then break into groups to look at the Internal Affairs report. Links on main readme.

