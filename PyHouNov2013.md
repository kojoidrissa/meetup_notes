#PyHouNov2013

##In our last episode...

-  ~12K rows & 22 columns of data
-  Pivot tables used to summarize, cut/paste into 14 different spreadsheets 
-  Two pieces of code eliminates most of that
    -  One piece compresses the 12K rows into the ~500 we need
    -  Had I shown you guys the code that made the 13 spreadsheets? If not, that's **TODAY'S** focus.

##functionalSheets.py
-  Sorts ~500 employees by cost center
-  Distributes ~500 employees into 13 different departments, based on their cost center

##Pseudo-functions, Functions & Modules! The road to OO code? Maybe?

###Pseudo-function: 'fullTable'
Takes the headcount summary file, computes the TOTAL hours and utilziation percentages (% of time on projects, % of time *on bench*)

###Functions
####`makeSubseaTable` and `makeNoSubseaTable`
Takes the data from the headcount summary file and creates a "table" (a nested list) based on certain rules that differ if the company is Subsea or Not

-  Subsea behaves as a a Company **and** a department. As such it may contain Cost Centers that are ALSO in other departments
-  The code in these two functions is nearly identical and it's based on the 'fullTable' code
-  There's PROBABLY a way for me to combine these two functions into one. Haven't given it much thought yet.
-  results of these two functions stored in `sheet_dict`, seen later

####`createTabs`
Creates a workbook, takes in  `sheet_dict`, creates a work**sheet** for each key, with the value being the contents  

###Modules or, "How I Learned to love Git and Branching"
This is where I started adding features, but didn't want to break my existing code. Git topic branches to the rescue!

-  `costCenterFooter`: generates totals for each Cost Center
    -  DOE, Project & Total Hours; Util %
-  `deptTotal`: does the same thing, for an entire department (spreadsheet tab)
-  `format`: currently only makes Headers bold. USED to work on Footers :-(
    -  This will be the home of future formatting code

##Main Loop
###Section 1: Dictionaries Abound!!
-  JSON config file (aka, a Python dictionary), run through `makeXXTable` functions
-  Results of stored in `sheet_dict` with Department name as key

###Section 2: Create Spreadsheets
1. run `sheet_dict` through `createTabs`
2. create *Headcount Summary Sorted*, a combined summary

###Section 3
Formatting and writing the file
