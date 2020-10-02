---
title: "Introduction"
teaching: 15
exercises: 0
questions:
- "What are the basic principles for using spreadsheets for good data organisation?"
objectives:
- "Describe best practices for organising data so that computers can make the best use of it 
for data analysis."
keypoints:
- "Good data organisation is the foundation of any research project."
---

Most researchers have data or do data entry in
spreadsheets. Spreadsheet programs are good for data entry and provide very useful graphical
interfaces for handling very basic data quality control functions. 
Good data organisation is the foundation of your research project that relies on data analysis - it is of paramount
importance to get this first step right in order to avoid loads of "data wrangling" and "data cleaning" 
further down the line. After this lesson, you will be able to:
- Implement best practices in organising tabular data (that is, data organised in rows and columns) 
- Identify and address common formatting mistakes
- Understand approaches for handling dates in spreadsheets
- Utilise basic quality control features and data manipulation practices
- Effectively export data from spreadsheet programs
- Overall good data practices

Why are we not teaching data analysis in spreadsheets? 

- Data analysis in spreadsheets usually requires a lot of manual
  work. If you want to change a parameter or run an analysis with a
  new dataset, you usually have to redo everything by hand or copy all the formulas to a new dataset. 
  This is 
  labourious and error prone. We do know that you can create macros in spreadsheets, but see the next point.
- There is no natural "starting point" for an analysis in a spreadsheet as it can happen in any cell. Some formulas 
depend on formulas in other cells being evaluated and values calculated prior to execution.
  This makes it difficult to follow, track or reproduce statistical or plotting
  analyses done in spreadsheet programs when you want to go back to
  your work or someone asks for details of your analysis or you inherit someone else's spreadsheet containing formulas.
- There are better tools for doing data analyses - e.g. writing a Python or R script. While these are 
also not 
error proof (there is always the human factor), they are much more readable and easier to analyse, test and 
verify by yourself and others.   

## Spreadsheet programs

Many spreadsheet programs are available. Since most participants utilise Excel as their primary spreadsheet program, this lesson will make use of Excel examples. A free spreadsheet program that can also be used is LibreOffice. Commands may differ a bit between programs, but the general idea
is the same.

Spreadsheets encompass a lot of the things we need
to be able to do as researchers. We can use them for:

- Data entry
- Organising data
- Subsetting and sorting data
- Statistics
- Plotting

We do a lot of different operations in spreadsheets. What kind of operations do you do in spreadsheets? Which ones do you think spreadsheets are good for? How many time have you accidentally done 
something in a spreadsheet that made you frustrated?

## Problems with spreadsheets

Spreadsheets are good for data entry, but in reality we tend to
use spreadsheet programs for much more than data entry. We use them
to create data tables for publications, to generate summary
statistics and make figures.

Generating tables for publications in a spreadsheet is not
optimal - often, when formatting a data table for publication, we’re
reporting key summary statistics in a way that is not really meant to
be read as data, and often involves special formatting
(merging cells, creating borders, making it pretty). We advise you to
do this sort of operation within your document editing software.

The latter two applications, generating statistics and figures, should 
be used with caution. Due to the graphical, drag and drop nature of 
spreadsheet programs, it can be very difficult, if not impossible, to 
replicate your steps (much less retrace anyone else's). In particular, if your 
stats or figures require you to do more complex calculations. Furthermore, 
in doing calculations in a spreadsheet, it is easy to accidentally apply a 
slightly different formula to multiple adjacent cells. When using a 
command-line based statistics program like R or Python, it’s practically 
impossible to apply a calculation to one observation in your 
dataset but not another unless you are doing it on purpose. 

## Using spreadsheets for data entry and cleaning

However, there are circumstances where you might want to use a spreadsheet 
program to produce “quick and dirty” calculations or figures, and data 
cleaning will help you use some of these features. Data cleaning also
puts your data in a better format prior to importation into a 
statistical analysis program. We will show you how to use some features of 
spreadsheet programs to check your data quality along the way and produce 
preliminary summary statistics.

In this lesson, we will assume that you are most likely using Excel as
your primary spreadsheet program - there are others, but Excel seems
to be the program most used by researchers and scientists.

In this lesson we are going to talk about:

1. [Formatting data in spreadsheets](../01-format-data/)
2. [Common spreadsheet errors](../02-common-mistakes/)
3. [Dates as data](../03-dates-as-data/)
4. [Quality control](../04-quality-control/)
5. [Exporting data](../05-exporting-data/)
