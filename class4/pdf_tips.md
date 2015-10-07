Dealing with PDFs
============

PDF's are the bane of a data journalist's existence. They come in all kinds of unfriendly formats.  

## Is it an image or is it text?
It doesn't matter if you just want to search a pdf or turn it into a data set -- if it starts as an image, you've got a big hurdle to jump called Optical Character Recognition, or OCR.

Learn to check for image vs. text as soon as you get a document. THe easiest way is to try to select some text in your pdf reader. If you can't, it's probably a picture of text. If you can, then try to select some more. If you can select most of it, it's probably text.

Government agencies will give you both kinds. The easiest to use are those that were created directly from Word, Excel, or some other form. The hardest are forms that have been scanned into a computer (often out of order).

OCR software can be expensive. If all you want to do is search, you can use [DocumentCloud](http://documentcloud.org). That service automates the use of the free Tesseract engine. But beyond that, you'll probably have to pay for a tool. See a list below.

##Searchable tables
PDFs are designed to preserve the format on the page. You shouldn't think of them as data files but as printed reports. Sometimes copying and pasting leaves you with unintelligible line breaks and smushed-together cells. You'll usually have to use some kind of tool to deal with this.

The key to trying to convert PDFs is to try every tool you can afford. You'll never know which one works. Again, these will only work with pdf's that are already searchable.

### Free tools
* [CometDocs](http://www.cometdocs.com) is a free service that lets you upload your pdf and will return to you an XL file in email. Your IRE membership gives you a paid version for free, which lets you keep all of your pdf's on their site and puts you in the front of the line.
* [Tabula](http://tabula.nerdpower.org/), a new alpha-level project from ProPublica and the Mozilla fellows (and also Jeremy Merrill now at the NYT). It lets you show the program where a table is, and it does a little more sophisticated work to figure out where the cells are. It's a little better with PDF's with lines between rows than CometDocs.
* [xpdf](http://www.foolabs.com/xpdf/) is an old but reliable command line tool that still works remarkably well. It's often best for very fixed-width and consistent pdfs. It's a bit of a pain to install on Unix-based (including Mac) systems, but once you have it it's easy. See [this tutorial](http://www.ire.org/resource-center/tipsheets/3440/) from IRE to use it. You'll have to log into IRE to get it.
* [PDF Tables](http://pdftables.com) from ScraperWiki is free for now. It may restrict large-scale conversions. It uses a different algorithm that might sometimes preserve the position of cells best.

There are also PDF plug-ins to Ruby and Python, which can sometimes work just fine.

###When free isn't good enough
Most of the pay products have two levels: one if you don't need to OCR, and another if you do. If you're going to pay, you might as well get the OCR. It's not that much more and you'll eventually need it.  Sometimes it's worth seeing if you can pay just a little more than that for what's called "batch" conversion, or "hot folders." That means that when you get 10,000 pdfs zipped up into one file, you won't have to individually convert them all.

Rob Barry created [this tutorial](extracting_image_pdfs.pdf) using ABBYY to extract information from even the most difficult forms. 

*[Able2Extract](http://www.investintech.com/order_main.htm): $99.95 for non-OCR/ $129.95 for OCR. Intuitive and reasonably accurate. It has some annoyances, but saving as a text file often overcomes them (rather than going directly to Excel).

*[ABBYY FineReader](http://finereader.abbyy.com/) Also $99.99 for personal use, available for Mac and Windows. Includes OCR.

*[OmniPage](http://www.nuance.com/for-individuals/by-product/omnipage/index.htm), $149.99 for individuals. This one is just slightly more powerful, but I've had better luck with it over time. The constant upgrades are really a pain.  (Windows only)

*[Cogniview](http://www.cogniview.com/) has PDF2XL, which has been a treat for very difficult pdfs. It has a hard learning curve and is only really useful on tables, unlike OmniPage and ABBYY. ($129.97). (Windows only)

 
