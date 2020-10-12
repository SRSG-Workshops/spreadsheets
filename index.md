---
layout: lesson
---
> ## Credit: Data Carpentry 
> This lesson is based on [Data Carpentry's](https://datacarpentry.org.) "Data Organisation In Spreadsheets" lessons from the [ecology](https://datacarpentry.org/lessons/#ecology-workshop) and [social 
> sciences](https://datacarpentry.org/lessons/#social-science-curriculum) curricula.
{: .testimonial} 

Good data organisation is the foundation of any research project. Most 
researchers have data in spreadsheets, so it is the place that many research
projects start. 

We often organise data in spreadsheets in the ways that we as humans want to work with data. However, in order
to use tools that make computation and data analysis more efficient, reusable and reproducible, such as programming 
languages like R or Python, we need to structure our data in a particular way so that computers can "understand" and 
"make use of" the data. Since this is where most research projects start, 
this is where we want to start too!

In this lesson, you will learn:

- What the basic principles for using spreadsheets for good data organisation are and how to format 
data in spreadsheets for effective data use,
- What some common mistakes with formatting data in spreadsheets are and how to avoid them,
- Peculiarities of storing and handling dates in spreadsheets and how to avoid mistakes with dates,
- Validating data on input for basic quality assurance and control in spreadsheets and to limit incorrect data on entry, and
- How to export data from spreadsheets in a way that is useful for downstream applications or publications.

All these will help you to get your current data into a good shape and plan new data 
collections so less "data cleaning" and "data wrangling" is needed in the future.

In this lesson, however, you will *not* learn:
- How to do statistics and formulas in spreadsheets, or
- How to plot graphs using spreadsheets. 

There are many good tutorials available online on the topic of doing data analysis in spreadsheets. If you are looking 
to learn any of the above, a good reference is [Head First Excel](https://www.amazon.com/Head-First-Excel-learners-spreadsheets/dp/0596807694/ref=sr_1_1?ie=UTF8&qid=1491594584&sr=8-1&keywords=head+first+excel), published by O'Reilly.
 
Why are we not teaching data analysis in spreadsheets?

- Data analysis in spreadsheets usually requires a lot of manual work. If you want to change a parameter or run an analysis with a new dataset, you usually have to redo everything by hand or copy all the formulas to a new dataset. This is labourious and error-prone. We do know that you can create macros in spreadsheets, but see the next point.
- There is no natural “starting point” for an analysis in a spreadsheet as it can happen in any cell. Some formulas depend on formulas in other cells being evaluated and values calculated prior to execution. This makes it difficult to follow, track or reproduce statistical or plotting analyses done in spreadsheet programs when you want to go back to your work or someone asks for details of your analysis or you inherit someone else’s spreadsheet containing formulas.
- There are better tools for doing data analysis - e.g. writing a Python or an R script. While these are also not error-proof (there is always the human factor), they are much more readable and easier to analyse, test and verify by yourself and others.

> ## Getting Started
> This lesson assumes no prior knowledge of the computational skills or tools apart from the basic 
> usage of spreadsheet software.
>
> To get started, follow the directions in the "[Setup](/setup.html)" section to 
> download the lesson data to your computer.
{: .prereq}
