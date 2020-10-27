---
title: "Introduction"
teaching: 10
exercises: 0
questions:
- "What are the basic principles for using spreadsheets for good data organisation?"
objectives:
- "Describe best practices for organising data so that computers can make the best use of it
for data analysis."
keypoints:
- "Good data organisation is the foundation of any research project."
---

Most researchers have data in spreadsheets or use them for data entry. Spreadsheet programs are good for data entry
and provide very useful graphical interfaces for handling basic data quality control functions.
and provide very useful graphical interfaces for handling basic data quality control functions.
Good data organisation is the foundation of any research project that relies on data analysis - it is of paramount
importance to get this first step right in order to avoid time-consuming "data wrangling" and "data cleaning"
further down the line. After this lesson, you will be able to:
* Implement best practices in organising tabular data (that is, data organised in rows and columns)
* Identify and address common formatting mistakes
* Understand approaches for handling dates in spreadsheets
* Utilise basic quality control to validate data on input and limit incorrect data entry
* Effectively export data from spreadsheet programs
* Know overall good data practices

In this lesson, however, you will *not* learn:
- How to use statistics and formulas in spreadsheets, or
- How to plot graphs using spreadsheets

There are many good tutorials available online on the topic of data analysis in spreadsheets. If you are looking
to learn any of the above, a good reference is [Head First Excel](https://www.amazon.com/Head-First-Excel-learners-spreadsheets/dp/0596807694/ref=sr_1_1?ie=UTF8&qid=1491594584&sr=8-1&keywords=head+first+excel), published by O'Reilly.

## Why do we not recommend using spreadsheets for data analysis?

- Data analysis in spreadsheets requires a lot of manual work. If you change a parameter or want to use a new dataset,
you have to reproduce every action by hand or meticulously copy all the formulas to a new spreadsheet.
This is laborious and error-prone. (You can shortcut some of this work with macros... but see the next point.)
- There is no natural “starting point” for an analysis in a spreadsheet as it can happen in any cell. Some formulas
depend on formulas in other cells being evaluated and values calculated prior to execution. This makes it difficult to
follow, track or reproduce statistical or plotting analyses done in spreadsheet programs when you want to go back to
your work or someone asks for details of your analysis or you inherit someone else’s spreadsheet containing formulas.
- There are better tools for doing data analysis - e.g. writing a Python or an R script. While these are also not
error-proof (nothing is!), they are much more readable and easier to analyse, test and verify by yourself and others.

## Spreadsheet programs

Spreadsheets encompass a lot of the activities researchers need. We can use them for:

- Data entry
- Organising data
- Subsetting and sorting data
- Statistics
- Plotting

The intricacies of spreadsheets often make it hard to reproduce analyses done in spreadsheets, or to
spot and correct errors. Sometimes this is due to human errors (you will learn how to avoid some of them);
at other times it is due to the spreadsheet programme itself (e.g. [20% of genetics papers contain errors due to Excel converting gene names to calendar dates](https://www.theverge.com/2020/8/6/21355674/human-genes-rename-microsoft-excel-misreading-dates)).
Have you event accidentally done something in a spreadsheet that made you frustrated?

Many spreadsheet programs are available. Most researchers utilise Excel as their primary spreadsheet program (this
lesson will make use of Excel examples), but free spreadsheet programs exist, including LibreOffice,
Gnumeric, OpenOffice.org or Google Spreadsheets. Commands may differ a bit between programs, but the general idea
is the same.

## Problems with spreadsheets

Spreadsheets are good for data entry, but in reality we tend to
use spreadsheet programs for much more than data entry. We use them
to create data tables for publications, to generate summary
statistics and make figures.

Generating tables for publications in a spreadsheet is not
optimal - often, when formatting a data table for publication, we are
reporting key summary statistics in a way that is not really meant to
be read as data, and often involves special formatting
(merging cells, creating borders, making it pretty for the human eye). We advise you to
do this sort of operation within your document editing software and not within your data.

The latter two applications, generating statistics and figures, should
be used with caution. Due to the graphical, drag and drop nature of
spreadsheet programs, it can be very difficult, if not impossible, to
replicate your steps (much less retrace anyone else's). In particular if your
stats or figures require you to do more complex calculations. Furthermore,
in doing calculations in a spreadsheet, it is easy to accidentally apply a
slightly different formula to multiple adjacent cells. When using a
command-line based statistics program like R or Python, it is practically
impossible to apply a calculation to one observation in your
dataset but not another unless you are doing it on purpose.

## Using spreadsheets for data entry and cleaning

However, there are circumstances where you might want to use a spreadsheet
program to produce “quick and dirty” calculations or figures, and data
cleaning will help you use some of these features. Data cleaning also
puts your data in a better format prior to importation into a different
statistical analysis program. We will show you how to use some features of
spreadsheet programs to check your data quality and produce
preliminary summary statistics.

In this lesson we are going to talk about:

1. [Formatting data in spreadsheets](../01-format-data/)
2. [Common spreadsheet errors](../02-common-mistakes/)
3. [Dates as data](../03-dates-as-data/)
4. [Quality assurance and control](../04-quality-control/)
5. [Exporting data](../05-exporting-data/)
