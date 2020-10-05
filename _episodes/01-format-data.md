---
title: "Formatting data in spreadsheets"
teaching: 10
exercises: 15
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

Using the power of computers, we can manage and analyse data in much more 
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
limit how the "future self" or your collaborators can work with the
data.

> ## Best data formats may differ
> The best layouts/formats (as well as software and
> interfaces) for data entry and data analysis might be
> different for each specific use case. It is important to take this into account, make decision 
> on a case by case basis, and ideally
> automate the conversion from one format to another.
{: .callout}

## Keeping track of your analyses

When you are working with spreadsheets, during data clean up or analyses, it is
very easy to end up with a spreadsheet that looks very different from the one
you started with. In order to be able to reproduce your analyses or figure out
what you did when Reviewer #3 asks for a different analysis, you should:

- Create a new copy of the original data file to keep your cleaned or analysed data. Do not modify
the original dataset, or you will never know where you started!
- Keep track of the steps you took in your clean up or analysis. You should record 
these steps as you would any step in an experiment. We recommend that you 
do this in a plain text file stored in the same folder as the data file. 

This might be an example of a spreadsheet setup:

![spreadsheet setup](../fig/spreadsheet-setup-updated.png)

Put these principles into practice today during your exercises.

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
   most data repositories. We will covere this in one of the later episodes.

For instance, have a look at the following data from a survey of small mammals in a desert
ecosystem. Different people have gone to the field and entered data into a spreadsheet. 
They kept track of things like species, plot,
weight, sex and date collected.

If they were to keep track of the data like this:

![multiple-info example](../fig/multiple-info.png)

the problem is that species and sex are in the same field. So, if they wanted to 
look at all of one species or look at different weight distributions by sex, 
it would be hard to do this using this data setup. If, instead, we put sex and species 
in different columns, you can see that it would make it much easier to do such analyses. 

So, instead, the data should be organised as:

![single-info example](../fig/single-info.png)

> ## Columns for variables and rows for observations
> The rule of thumb, when setting up data in a table is: columns = variables, rows = observations, cells = data (values).
{: .callout}

## Fixing mistakes in data organisation

If you have not already done so, download the [messy survey data](/data/survey_data_spreadsheet_messy.xls?raw=true) 
(as outlined in [Setup section](/setup.html#data)). You will attempt to clean this data during the lesson and learn 
some best practices in data organisation in the process.

You will see four tabs in the messy data spreadsheet. Two field assistants conducted the surveys, one
in 2013 and one in 2014, and they both kept track of the data in their own way in tabs '2013' and 
'2014' of the dataset, respectively. There is a tab 'dates' too, but you can ignore it for now as we will come back to 
it the [episode on dates](/03-dates-as-data/index.html). Finally, there is a tab 'semi-cleaned-combined', which 
contains combined data from tabs '2013' and '2014', which is what you should be aiming for and can be used as a reference
while you are working on reorganising the data. We will revisit this tab in 
[episode on quality assurance and control](/04-quality-control/index.html) and you will see why it is 'semi-clean'. 

> ## Full & clean dataset
> If you want to have a look at the full, clean dataset - have a look [surveys.csv](https://ndownloader.figshare.com/files/2292172) (that combines data from all the surveys) or [combined.csv](https://ndownloader.figshare.com/files/10717186) (clean data from [surveys.csv](https://ndownloader.figshare.com/files/2292172), [plots.csv](https://ndownloader.figshare.com/files/3299474) and [species.csv](https://ndownloader.figshare.com/files/3299483) combined into one clean file).
{: .testimonial}  

> ## Exercise
> Take the messy version of the survey data and open it in a spreadsheet programme. Look at tabs '2013' and '2014' and 
> identify what is wrong with data in these two tabs. Make steps to clean up the "2013" and "2014" tabs, and 
> put them all together in one spreadsheet. 
>
> > ## Keep your raw data - raw 
> > Do not forget to create a new file or a new tab for the cleaned data; never
> > modify your original (raw) data.
> {: .callout}  
> 
> > ## Solution
> > All the mistakes in this messy dataset are addressed in the [next episode](../02-common-mistakes). 
> > You can refer to it to check if you spotted them all and go back and fix your spreadsheet.
> {: .solution}
{: .challenge}
