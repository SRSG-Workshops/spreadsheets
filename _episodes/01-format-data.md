---
title: "Formatting data in spreadsheets"
teaching: 15
exercises: 20
questions:
- "How do we format data in spreadsheets for effective data use?"
objectives:
- "Describe best practices for data entry and formatting in spreadsheets."
- "Apply best practices to arrange variables and observations in a spreadsheet."
keypoints:
- "Never modify your raw data. Always make a copy before making any changes."  
- "Keep track of all of the steps you take to clean your data in a plain text file."  
- "Organise your data according to tidy data principles."  
---

The most common mistake made is treating spreadsheets like lab notebooks, that is,
relying on context, notes in the margin,
spatial layout of data and fields to convey information. As humans, we
can (usually) interpret these things, but computers do not view information the same way, and
unless we explain to the computer what every single thing means (and
that can be hard!), it will not be able to see how our data fits
together.

Using the power of computers, we can manage and analyze data in much more 
effective and faster ways, but to use that power, we have to set up
our data for the computer to be able to understand it (and computers are very 
literal).

This is why it is extremely important to set up well-formatted
tables from the outset - before you even start entering data from
your very first preliminary experiment. Data organisation is the
foundation of your research project. It can make it easier or harder
to work with your data throughout your analysis, so it is worth
thinking about when you are doing your data entry or setting up your
experiment. You can set things up in different ways in spreadsheets,
but some of these choices can limit your ability to work with the data in other programs or
have the you-of-6-months-from-now or your collaborator work with the
data.

> ## Note on data formats
> The best layouts/formats (as well as software and
> interfaces) for data entry and data analysis might be
> different. It is important to take this into account, and ideally
> automate the conversion from one to another.
{: .callout}

## Keeping track of your analyses

When you are working with spreadsheets, during data clean up or analyses, it is
very easy to end up with a spreadsheet that looks very different from the one
you started with. In order to be able to reproduce your analyses or figure out
what you did when Reviewer #3 asks for a different analysis, you should:

- create a new copy of the original data file to keep your cleaned or analysed data. Do not modify
the original dataset, or you will never know where you started!
- keep track of the steps you took in your clean up or analysis. You should record 
these steps as you would any step in an experiment. We recommend that you 
do this in a plain text file stored in the same folder as the data file. 

This might be an example of a spreadsheet setup:

![spreadsheet setup](../fig/spreadsheet-setup-updated.png)

Put these principles in to practice today during your Exercises.

> ## Version controlling your data
> This is out of scope for this lesson, but for information on how to maintain version control over your data in a more manageable and scalable way look, for example, at Software Carpentry's lesson on ['Git version control system'](http://swcarpentry.github.io/git-novice/).
{: .callout}

## Structuring data in spreadsheets

The cardinal rule of using spreadsheet programs for data is to keep it "tidy":

1. Put all your variables in columns - the thing you are measuring,
   like 'weight' or 'temperature'.
2. Put each observation in its own row.
3. Do not combine multiple pieces of information in one
   cell. Sometimes it just seems like one thing, but think if that is
   the only way you will want to be able to use or sort that data.
4. Leave the raw data raw - do not change it!
5. Export the cleaned data to a text-based format like CSV (comma-separated values) format. This
   ensures that anyone can use the data, and is required by
   most data repositories. We will covered this in one of the later episodes.

For instance, have a look at the following data from a survey of small mammals in a desert
ecosystem. Different people have gone to the field and entered data into a spreadsheet. 
They keep track of things like species, plot,
weight, sex and date collected.

If they were to keep track of the data like this:

![multiple-info example](../fig/multiple-info.png)

the problem is that species and sex are in the same field. So, if they wanted to 
look at all of one species or look at different weight distributions by sex, 
it would be hard to do this using this data setup. If instead we put sex and species 
in different columns, you can see that it would be much easier. 

## Columns for variables and rows for observations

The rule of thumb, when setting up data in a table is: columns =
variables, rows = observations, cells = data (values).

So, instead we should have:

![single-info example](../fig/single-info.png)

> ## Exercise
> You are going to take the messy version of the survey data and describe how you would clean it up.
>
> 1. If you have not already done so, download the [messy survey data](https://ndownloader.figshare.com/files/2252083) from the 
> [Portal Project Teaching Database on FigShare](http://figshare.com/articles/Portal_Project_Teaching_Database/1314459).
> 2. Open up the data in a spreadsheet program. 
> 3. You can see that there are three tabs in the spreadsheet. Two field assistants conducted the surveys, one
in 2013 and one in 2014, and they both kept track of the data in their own way in tabs "2013" and 
> "2014" of the dataset, respectively. There is a tab "dates" too, but you can ignore it for now. 
> Now, you are the person in charge of this project and 
> you want to be able to start analysing the data.   
> 4. Identify what is wrong with this spreadsheet. Make steps to clean up the "2013" and "2014" tabs, and to put them all together in one spreadsheet. 
>
> > ## Keep your raw data raw 
> > Do not forget our first piece of advice:
> > create a new file (or a new tab) for the cleaned data, never
> > modify your original (raw) data.
> {: .testimonial}
> 
> > ## Solution
> > - All the mistakes in this messy dataset are addressed in the [next lesson](../02-common-mistakes). 
> > You can refer to it to check if you spotted them all.
> > - Note that there is a problem with dates in table 'plot 3' in tab "2014". The field assistant who collected the data for year 2014 initially forgot to include their data for 'plot 3'. They came back in 2015 to include the missing data and 
> > entered the dates for 'plot 3' in the dataset without the year. Excel automatically filled in the missing year as the
> > current year (i.e. 2015) - introducing an error in the data without the field assistant realising. We will address the peculiarities of working with dates in episode ["Dates as data"](../03-dates-as-data).  
> {: .solution}
{: .challenge}
