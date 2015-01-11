#dynamic report generation with R + 3D surfaces

##Gene's Presentation - Dynamic Reports with R, [kntr](http://yihui.name/knitr/) and [LaTex](http://www.latex-project.org)


###R's characteristics
-  Designed so it's objects are similar to object used by statisticians
-  Open Source
-  Not great for outputting the results of those computations
    -  Graphically
    -  books, documents, etc.

###Knitr
Ties your output dynamically to your source data. Changes in your source data (or how it's processed) are reflected in the output document.

Gene uses [R Studio](http://www.rstudio.com) to manipulate R and LaTex.

Knitr will let you embed Perl, Python, Ruby and Bash code chunks.

You can embed SQL code INTO your R. So, the SQL could pull data from a database, then R could process that data. THEN those results can get displayed in your output document.

I HAVE to learn more about this!! Start with 
[Gene's Github](https://github.com/genedan/meetup_presentations/tree/master/hdv_knitr) from this presentation

##Chris' Presentation: 3D Surfaces for Data Viz

Nevron Mesh Surface Charts

Better for analyzing large data sets with multiple interactive variables by small teams of people. Not meant for sharing the plots online or with large groups. Chris' application is for traders/risk analysts looking at complex situations.