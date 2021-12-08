# kickstarter-analysis
### Performing analysis on Kickstarter data to aid in the successful launch of a new theatrical project

## Overview of Project
### This analysis of Kickstarter data proivdes insights into the best fundraising strategies. Specifically, the analysis focused on former fundraising efforts for both theaters and plays, as our fictional client Louise is hoping to raise enough money to put on her own show, *Fever*. The analysis seeks to identify which month is best to launch a Kickstarter campaign and how the loftiness of the fundraising goal effects its success.

## Analysis and Challenges
### To begin the analysis of how different launch dates influenced the success of a fundraising campaign, I had to create a pivot table from the Kickstarter data that showed campaign outcomes (successful, failed, canceled) based on launch month. With my limited pivot table experience, it was challenging to figure out where to place each field. However, due to my practice in class and throughout the modules, I was able to determine that outcomes had to be assigned to both the columns and values where it would automatically be converted to a count. Additionally, I assigned my Date Created Conversion field to the rows, and had to ensure that I got rid of the automatically-generated Years and Quarters fields. Next, I filtered out the active campaings from the table and used the Parent Category field to filter on only theater fundraisers, and sorted the pivot table to display the count of successful efforts in the first column. With these fields and filters in place, my pivot table was now accurately displaying the number of successful, failed, and canceled theater fundraising campaigns for each month. Having built a robust pivot table, I then made a line pivot chart to aid in the visualization of the analyzed data.

### With a better understanding of how launch month has influenced the success of former theater Kickstarter fundraisers, I moved on to an analysis of how the loftiness of the fundraising goal effects its success. I first grouped the monetary goals of the campaigns into 12 ranges. With these ranges set, I utilized the COUNTIFS() function to determine the number of successful, failed, and canceled play fundraisers. I am familiar with this function, but it took me a second to remember how to correctly use it. On top of this, I had never incorporated inequalities into a COUNTIFS() function and was unaware that they required quoatation makrs, and so I had to consult Stack Overflow before creating my first valid function, =COUNTIFS(Kickstarter!$R$2:$R$4115,"plays",Kickstarter!$D$2:$D$4115,"<1000",Kickstarter!$F$2:$F$4115,"successful"). Next, it was just a matter of slightly tweaking this formula in order to produce accurate values for every cell in my makeshift table, a process that could present a time challenge if it needed to be applied to a larger table. 
