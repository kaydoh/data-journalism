# Tidy data #

Lecture notes, August 25, 2014<br>
Stabile Investigative Reporting Program<br>
Sarah Cohen / sarah.cohen@nytimes.com / 212.556.8027

How to use excel in an investigations:

* Make yourself. Track a case, or log events.
* Do calculations and analysis on other peoples' database.
* Share your data

Use the court salary database as an example of tidy data. The big problem is in the titles, and I took out some other problems.

1. Save as a copy (version, initials)
2. Add a unique id. (1, 2, doubleclick)
3. Freeze panes

Why is it good to repeat, say, the jurisdiction? Repetitive?
Last, First is a good way to do it.  
Later will talk about other ways you might be tempted to do it.

The term "Tidy data" comes from Hadley Wickham, a statistician who has been involved in developing products and add-ons for the R programming language. He uses Leo Tolstoy as a way to introduce untidy data: "Tidy datasets are alike, but every messy dataset is messy in its own way." 


He's defined some ways of thinking about data that let us use it in its most efficient form. You'll find that if you follow this, your data set will often have many *rows*, but not few *columns*.  I call this a tall and skinny dataset, as opposed to a short and fat one.

* Each row represents one item: a test, an inspection, a person, or an event.
* Each column represents one attribute or variable about each item. 
* Each worksheet or table represents one type of observational unit. For example, an inspection might include many fines -- one table would be information about the inspection, the other about the fines. This is what is called database "normalization"

We often ignore this last element when working with smallish datasets, and just repeat any information we need. 

You will rarely get tidy data. I'll give you some examples of real-world datasets we get all the time. But for now, we'll go through the exercise of thinking about what you might want to record and how you might want to record information about the court case you are going to follow. 

This will be different depending on the larger theme. But having a good handle on the basic facts of your case are useful. 

Talk about how this works - what can and can't you do with each of the columns? Why is it done this way? 

Types of data: Illustrated on [this spreadsheet](data-types.xlsx) for examples 

 * Words / text. These can be free-form, or they can be relatively consistent, like tags on a blog.
 * Numbers: Things you will add together or do math on. 
 * Dates: A special kind of number you can look at in a lot of ways. 
 
Use the [first100days.xlsx](first100days.xlsx) spreadsheet as an example of logging events. 
  
Still from Hadley, some common problems:
 
* Column headings are values, not labels. Examples include years, income ranges, etc. These can be OK to work with, but they will become tedious, because each formula or each operation has to be done exactly the same on each column. If you have 10 years, you have to do 10 percent changes. Other tools might work better
* Multiple kinds of information stored in one column. Example, one column for men 20-25 years old. Instead, have age column and sex column. (similar to above)
* The same information in columns and rows
* Different types of information (levels of analysis) in the same table. 
* Its companion -- multiple tables for the same information. See the example of the Medicaid managed care.

Hadley doesn't mention the most common problem in the data we get and sometimes create -- that the records are provided as a printout of a report, not as a dataset. Even when we get them in Excel. note the gambling records [here](https://dl.dropboxusercontent.com/u/26514347/NYTTraining/gambling-arrests-orig.xlsx) and [here](https://dl.dropboxusercontent.com/u/26514347/NYTTraining/arrests_normalized.xlsx). Go through the original and explain what is wrong with it.

The bad examples spreadsheet will take a long time to open, because of the way California did its ACA data.  

* California rates - how to make it small, what to do with it?
* Sort the tarp? What happens to the formulas. Fill in the blanks.How would you tidy? Units of analysis.
* Disaster declarations. Opposite problem. Filter vs. sort and summarize. Regex. Could they do any analysis themselves? Writing  a release, not analyzing geographic disparities. Investigative oppporutunities.
* Vetpop - how to get data from pivot tables. (Forecasting, not going back in time).

Exercise:

1. Read the section on Bubba Harris in [Two Gunshots on a Summer Night] (http://www.nytimes.com/projects/2013/two-gunshots/). Notice the chronology.

2. Now look at one of the key documents, [the internal affairs report](https://www.dropbox.com/s/5clhgdmtfv3dt8z/internal-affairs-report.pdf?dl=0) obtained using Florida's public records laws.  Don't read the whole thing. Just enough to get a sense of where that started from. 

3. One thing you wouldn't know: We were most interested in whether or not this case followed what a trade association had said was best practice in suspected cases of domestic abuse among police officers.

4. Try to design a spreadsheet that would tell you what you need to know efficiently. There are lots of right ways to do this, but you'll want to know what each gives you. 

Once done, look at the [the actual spreadsheet](bubba_harris_protocol.xlsx) Sarah made.

Original videos are on [Youtube](https://www.youtube.com/playlist?list=PL-Je9dqyEF8YS7Cy8BppKg5zrhiQC__n6). The third one in this series is about how to to a spreadsheet on your own.  