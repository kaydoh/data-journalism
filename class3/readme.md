# Class 3: Advanced Excel

## The key handouts

Most of the formulas you'll need in your work come from two IRE handouts. I've provided them here, with IRE's permission,  but there are plenty more where this came from if you join IRE for $25. (http://ire.org/join)

* A review of [Excel formulas](Excelformulas.pdf), from Jaimi Dowdell.
* [My Favorite (Excel) Things](https://github.com/sarahcnyt/stabile/blob/master/xl/3346.pdf?raw=true), by Mary Jo Webster.
* A nearly [20-year-old set of handouts](xlhandouts.pdf) created by Sarah for IRE training. Your Excel will look different, but the ideas are all the same. 

## Review of last week's homework

Most people had a little trouble with the homework. FIrst, it's hard to deal with so many columns and to figure out what you might want to know. Second, you have to remember the formulas. 

To review, here are the files you needed:

* The original file that you have to import into Excel [2014popestimates.csv](../class2/2014popestimates.csv?raw=true) (You can copy and paste this raw text into Excel, then use Data-> Text to Columns to split it up.)
* An explanation of the column names, called the record layout at  [2014popestimates_layout.pdf](../class2/2014popestimates_layout.pdf)
* An exercise to walkyou through a suggested path at [population_exercise.docx](../class2/population_exercise.docx)
* Finally, a finished spreadsheet with an example of how it might look when you're done at [2014popestimates_analyzed.xlsx](../class2/2014popestimates_analyzed.xlsx?raw=true)

As a reminder, there are several formulas you will need to remember:

_Percent change_

	(New - Old) / Old.
	Example: 
 		=(D2-C2)/C2, 
	where D2 is the newer year and C2 is the older year.

_Percent of total_

Remember about anchoring your formulas, using the dollar signs. If your data runs from B2 through B100, then the percent of total would be:

	=B2/(B$2:B$100)

Use the same anchoring when you use the **rank** formula

## Class 3 materials
### First pivot tables and filters
We used the baseball salaries to look at sorting, median, mode, filtering and pivot tables. 
There is a step-by-step filter and pivot table example using the data [mlb2011.xls](MLB2011.xls?raw=true) data set, called ["Baseball_salaries_2011"](Baseball_salaries_2011.pdf)

###Other pivot tables

We looked at World Bank debarment list from Jamie Dowdell at IRE, in the exercise called ["PivotTablesJD.pdf"](PivotTablesJD.pdf). The data for this exercise is already downloaded as [worldbank.xlsx](worldbank.xlsx?raw=true)

Finally, we started working through the baseball stats from the Colorado Rockies. We had to download and import the data properly, using the import wizard. Then we had to clean up a few fields using Text-to-Columns as well as some text formulas. 

* The step-by-step exercise is called ["ThinAir.docx"](ThinAir.docx?raw=true)
* The data is called [rockies.txt](rockies.txt). 
* The final spreadsheet is in [rockies_analyzed.xlsx](rockies_analyzed.xlsx?raw=true)

### Try this at home
There are two additional data sets in this repository, one of which has an exercise associated with it, the other not. 

* Back in the day, cell phones were only in cars, and they were novel. Reporters began FOIAing the phone records of these cell phones. One exercise, called [xlphones.pdf](xlphones.pdf) walks through a lot of what we've done for the last three weeks: using formulas to clean up data and creating pivot tables. It also introduces a formula called "vlookup", which helps you match two datasets, or categorize your data.  The data is called [carphone.xlsx](carphone.xlsx?raw=true)

## Your exercise

Try to do this exercise on your own, and come up with a lede that you could write the day after a snowstorm. 

Look at the data set called [snowstorm.xlsx](snowstorm.xlsx?raw=true), which is the attendance reported by New York Public Schools for each school during a snow storm. The spreadsheet has three pages. The first is documentation and tips. The second is called "attendance", and it is the raw data provided by the schools. The last page is "population", which provides ethnic composition for each school. 


