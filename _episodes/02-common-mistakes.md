---
title: "Common spreadsheet errors"
teaching: 10
exercises: 15
questions:
- "What are some common challenges with formatting data in spreadsheets and how can we avoid them?"
objectives:
- "Recognise and resolve common spreadsheet formatting problems."
keypoints:
- "Avoid using multiple tables within one spreadsheet."
- "Avoid spreading data across multiple tabs."
- "Record zeros as zeros."
- "Use an appropriate null value to record missing data."
- "Do not use formatting to convey information or to make your spreadsheet look pretty."
- "Place comments in a separate column."
- "Record units in column headers."
- "Include only one piece of information in a cell."
- "Avoid spaces, numbers and special characters in column headers."
- "Avoid special characters in your data."
- "Record metadata in a separate plain text file."
---

There are a few potential errors to be on the lookout for in your own data as well as data from collaborators or 
elsewhere. If you are aware of the errors and the possible negative effect on downstream data analysis and result 
interpretation, it might motivate yourself and your project members to try and avoid them. Making small changes 
to the way you organise your data in spreadsheets can have a great impact on efficiency and reliability when it 
comes to data cleaning and analysis. Here is the list 
of common spreadsheet errors; we will cover each of them in turn.

- [Using multiple tables](#tables)
- [Using multiple tabs](#tabs)
- [Not filling in zeros](#zeros)
- [Using problematic null values](#null)
- [Using formatting to convey information](#formatting)
- [Using formatting to make the data sheet look pretty](#formatting_pretty)
- [Placing comments or units in cells](#units)
- [Entering more than one piece of information in a cell](#info)
- [Using problematic field names](#field_name)
- [Using special characters in data](#special)
- [Inclusion of metadata in data table](#metadata)
- [Date formatting](../03-dates-as-data/)

> ## Exercise
> 1. Use the same [messy data spreadsheet](/data/messy_survey_data.xls) where you attempted to clean the data in the previous exercise.
> 2. Have a look at each of the spreadsheet errors described below and fix your spreadsheet (in a separate tab or a separate file), if you have not already.
> 3. When you finish, compare yours with [this version of the clean dataset](https://ndownloader.figshare.com/files/2292172). 
>They may not be identical, but they should have the same overall structure.
{: .challenge}

## Using multiple tables

A common mistake is creating multiple data tables within
one spreadsheet. This will confuse a data analysis programme, so do not do this!
When you create multiple tables within one
spreadsheet, you are making false associations between things for the computer,
which sees each row as one observation (even though, for a human observer, these 
are clearly separate observations). You are also potentially using the same
field name in multiple places, which will make it harder to clean your data up
into a usable form. The example below depicts the problem:

![multiple tabs](../fig/2_datasheet_example.jpg)

In the example above, the computer will see (for example) row 4 and assume that all columns A-AF 
refer to the same sample. This row actually represents four distinct samples 
(sample 1 for each of four different collection dates - May 29th, June 12th, June 19th, and June 26th), 
as well as some calculated summary statistics (an average (avr) and standard error of measurement (SEM)) for two of those samples. Such rows are similarly problematic and virtually unusable by any 
data analysis programme.

There is no reason why observations from different sites or different years should not go into a single table in the 
same spreadsheet. You just need to introduce new columns to keep track of site and year. Keeping data
pertaining to the same experiment in a single table will help you keep consistent data structure and avoid errors when 
looking up data from different tables.  

## <a name="tabs"></a> Using multiple tabs

But what about workbook tabs? That seems like an easy way to organise data, right? Well, yes and no. When you create extra tabs, you fail to allow the computer to see connections in the data that are there (you have to introduce spreadsheet application-specific functions or scripting to ensure this connection). Say, for instance, you make a separate tab for each day you take a measurement.

This is not good practice for two reasons:

1. you are more likely to accidentally add inconsistencies to your data if each time you take a measurement, you start 
recording data in a new tab, and

2. even if you manage to prevent all inconsistencies from creeping in, you will add an extra step for yourself before 
you analyse the
data because you will have to combine these data into a single datatable. You will have to explicitly tell the computer 
how to combine
tabs - and if the tabs are inconsistently formatted, you might even have to do it manually.

The next time you are entering data, and you go to create another tab or table, ask yourself if you could avoid adding 
this tab by adding another column to your original spreadsheet. We used multiple tabs in our example of a messy data 
file, but now you have seen how you can reorganise your data to consolidate across tabs.

> ## Note on bigger data and column headers 
>
> Your datasheet might get very long over the course of the experiment. This makes it harder to enter data if you cannot see your headers
> at the top of the spreadsheet. But do not be tempted to repeat your header row in the middle of your data - 
> these headers will get mixed into the data leading to problems down the road. Instead, you can freeze the column headers so that they remain visible even when you have a spreadsheet with many rows. 
> if you are not sure how to do this, see the [documentation on how to freeze column headers in Excel](https://support.office.com/en-ca/article/Freeze-column-headings-for-easy-scrolling-57ccce0c-cf85-4725-9579-c5d13106ca6a).
{: .callout}

## <a name="zeros"></a> Not filling in zeros

It might be that when you are measuring something, it is
mostly zero. For example, the number of times a rabbit
is observed in the survey. Why bother
writing in the number zero in that column, when it is mostly zeros?

There is a big difference between a zero and a blank cell in a spreadsheet. To the computer, a zero is actually data. You measured
or counted it. A blank cell means that it was not measured and the computer will interpret it as an unknown value (otherwise known as a
*null* value). 

The spreadsheets or statistical programs will likely misinterpret blank cells that you intend to be zeros. By not entering the value of
your observation, you are telling your computer to represent that data as unknown or missing (null). This can cause problems with 
subsequent calculations or analyses. For example, the average of a set of numbers which includes a single null value is always null
(because the computer cannot guess the value of the missing observations). Because of this, it is very important to record zeros as zeros and truly missing data as nulls.


## <a name="null"></a> Using problematic null values
Using problematic null values is as big a mistake as mixing zeros and null values. Fir example, 
using -999 or other numerical values (or zero) to represent missing data. 

There are a few reasons why null values get represented differently within a dataset.
Sometimes confusing null values are automatically recorded from the measuring device. If that is the case, there is not 
much you can do, but it can be addressed in data cleaning with a tool like 
[OpenRefine](https://southampton-rsg.github.io/openrefine-data-organisation-and-management/) before analysis. Other times different null 
values are used to convey different reasons why the data is not there. This is important information to capture, 
but is in effect using one column to capture two pieces of information. Similar to fixing the errors when
[using formatting to convey information](#formatting), it would be good here to create a new column, e.g. 
'data_missing', and use that column to capture the different reasons. 

Whatever the reason, it is a problem if unknown or missing data is recorded as -999, 999, or 0.
Statistical programs do not know that these are intended to represent missing (null) values and, because they are 
valid numbers, they will be used in calculations causing incorrect results. How these values are interpreted will depend on 
the software you use to
analyse your data. It is essential to use a clearly defined and consistent null indicator.
Blanks (most applications) and 'NA' (for R) are good choices. White et al., 2013, explain good choices for 
indicating null values for different software applications in their article:
[Nine simple ways to make it easier to (re)use your data](http://doi.org/10.4033/iee.2013.6b.6.f).

![White et al.](../fig/3_white_table_1.jpg)


## <a name="formatting"></a> Using formatting to convey information 

For example, highlighting cells, rows or columns that should be excluded from an analysis (see figure below), or 
leaving blank rows to indicate separations in data will cause problems with later data analyses.

![formatting](../fig/formatting.png)

The solution in this case is to create a new field to encode which data should be excluded.

![good formatting](../fig/good_formatting.png)


## <a name="formatting_pretty"></a> Using formatting to make the spreadsheet look pretty

Fo example, merging cells (especially in headers) or using borders to separate different data.

If you are not careful, formatting a worksheet to be more aesthetically pleasing can compromise your computer’s ability to
see associations in the data. Merged cells will make your data unreadable by statistics software, which will read the 
merged cell as a single data value anc cause misalignment with data in the following rows. Consider restructuring your data in
such a way that you will not need to merge cells to organise your data.

## <a name="units"></a> Placing comments or units in cells

Sometimes you need to make a note or a comment on an observation. For example, your data was collected, in part, 
by a summer student who you later found out was misidentifying some of your species, some
of the time. You want a way to note these data are suspect.

Most analysis software cannot see Excel or LibreOffice comments, and would be confused by comments placed within your data
cells. As described above for formatting, create another field if you need to add notes to cells. Similarly, do not include units in
cells: ideally, all the measurements you place in one column should be in the same unit, but if for some reason they are not, create
another field and specify the units the adjacent cell is in.


## <a name="info"></a> Entering more than one piece of information in a cell

For example, you are counting species and you find one male, and one female of the same species. You enter this as 
'1M, 1F.'

Do not include more than one piece of information in a cell. This will limit the ways in which you can analyse your data. 
If you need both these measurements, design your data sheet to include this information. 
For example, include one column for number of
individuals and a separate column for sex.

## <a name="field_name"></a> Using problematic field names
Choose descriptive field names, but be careful not to include spaces, numbers, or special characters of any kind. Spaces can be
misinterpreted by parsers that use whitespace as delimiters and some programs do not like field names that are text strings that start
with numbers.  

Underscores (`_`) are a good alternative separator to spaces. Or consider writing names in camel case 
(like this: ExampleFileName) to improve
readability. Remember that abbreviations that make sense at the moment may not be so obvious in 6 months, 
but do not overdo it with names
that are excessively long. Including the units in the field names avoids confusion and enables others to readily 
interpret your fields.

Table below gives some examples of names to use and good alternatives as well as names to avoid.
<table>
<tr>
	<td> <b>Good Name</b></td> <br />
	<td> <b>Good Alternative</b> </td><br />
	<td> <b>Avoid</b></td><br />
    <td> <b>Reason</b></td><br />
</tr>
<tr>
	<td>Max_temp_C</td>
	<td>MaxTemp</td>
	<td>Maximum Temp (°C)</td>
    <td>Uses a special character (°)</td>
</tr>
<tr>
	<td>Precipitation_mm</td>
	<td>Precipitation</td>
	<td>precmm </td>
    <td>Not very readable</td>
</tr>	
<tr>
	<td>Mean_year_growth</td>
	<td>MeanYearGrowth </td>
	<td>Mean growth/year</td>	
    <td>Uses a special character (/)</td>
</tr>	
<tr>
	<td>sex</td>
	<td>sex</td>	
	<td>M/F</td>
    <td>Uses special character (/) and not very readable</td>
</tr>
<tr>	
	<td>weight</td>
	<td>weight</td>	
	<td>w.</td>	
    <td>Uses a special character (.) and not very readable</td>
</tr>
<tr>	
	<td>cell_type </td>
	<td>CellType </td>
	<td>Cell Type </td>
    <td>Uses a blank character</td>
</tr>
<tr>
	<td>Observation_01 </td>
	<td>first_observation</td>
	<td>1st Obs</td>
    <td>Uses a blank character and starts with a number</td>
</tr>
</table>

## <a name="special"></a> Using special characters in data

A common mistake is treating your spreadsheet program as a word processor when writing notes. For example, copying 
data directly from Microsoft Word or other applications. For example, when writing longer text in a cell, 
people often include line breaks, em-dashes,
etc. in their spreadsheet.  Also, when copying data in from applications such as Microsoft Word, 
formatting and fancy non-standard characters (such
as left- and right-aligned quotation marks) are included. When exporting this data into a coding/statistical environment or into a
relational database, errors may occur - for example, lines being cut in half and encoding errors being thrown.

General best practice is to avoid adding characters such as newlines, tabs, and vertical tabs. In other words, 
treat a text cell as if
it was a simple Web form that can only contain text and spaces.

## <a name="metadata"></a> Inclusion of metadata in data table

Recording data about your data (“metadata”) is essential. You may be on intimate terms with your dataset while you are 
collecting and analysing it, but the chances that you will still remember that the variable "sglmemgp" means single 
member of group, for
example, or the exact algorithm you used to transform a variable or create a derived one, after a few months, a year, 
or more are slim.  

As well, there are many reasons other people may want to examine or use your data - to understand your findings, to verify your findings,
to review your submitted publication, to replicate your results, to design a similar study, or even to archive your data for access and 
re-use by others. While digital data by definition are machine-readable, understanding their meaning is a job for human beings. The 
importance of documenting your data during the collection and analysis phase of your research cannot be overestimated, especially if your
research is going to be part of the scholarly record.

However, you should not be adding a legend at the top or bottom of your data table explaining column meaning, units, 
exceptions, etc. Metadata should not be contained in the data file itself. Unlike a table in a paper or a supplemental file, metadata (in the 
form of legends) should not be included in a data file since this information is not data, and including it can disrupt how computer 
programs interpret your data file. Rather, metadata should be stored as a separate file in the same directory as your data file, 
preferably in plain text format with a name that clearly associates it with your data file. Because metadata files are free text format,
they also allow you to encode comments, units, information about how null values are encoded, etc. that are important to document but can
disrupt the formatting of your data file.  

Additionally, file or database level metadata describes how files that make up the dataset relate to each other; what format are they are 
in; and whether they supersede or are superseded by previous files. A folder-level `README.txt` file is the classic way of accounting for 
all the files and folders in a project.  

> ## Credit: MANTRA
> The above text on metadata was adapted from the online course Research Data [MANTRA](http://datalib.edina.ac.uk/mantra) by EDINA and Data Library, University of Edinburgh. MANTRA is licensed under a [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).
{: .testimonial}
