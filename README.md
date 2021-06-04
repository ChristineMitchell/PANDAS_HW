# PANDAS_HW

# PyCity Schools Analysis

## Overview and Purpose of the Project
We were asked to complete an analysis on the PyCity School District test results utilizing Jupyter Notebook and the Pandas Library. With these tools, we were able to import and read the csv files of raw reporting data; then we were able to inspect, clean, and perform calculations with the data; and lastly, we created dataframe tables to complete our analysis of the school district results. We not only wanted to look at how the data rolled up at the district level, but we also wanted to see how the different schools faired amongst each other. The measurements evaluated were the following: 

      •	average math scores,
      •	average reading scores,
      •	the percentage of students who passed their math tests by 70% or more,
      •	the percentage of students who passed their reading test by 70% or more, as well as the
      •	the overall percentage of students who passed both their math and reading tests by 70% or more.

We utilized the last measurement, overall percentage of students who passed both their math and reading tests by 70% or more, to determine the top five schools in the district, as well as the bottom five schools. 

The stakeholders were eager to see the breakdown of the average math scores and the average reading scores by grade level for each high school in the district.

They wanted to look at the data from other angles as well. Because they wanted to see if the amount that a school spends per student impacts the results, we grouped the schools by spending levels to then evaluate the five measurements above. As well, we evaluated if the school size had any impact to the measurements above. Lastly, we wanted to compare the charter school results with the district school results. All of this will help the school board set their budgets for the upcoming school year.

Unfortunately, upon completing our data slicing and dicing, we learned that there was concern about the integrity of the freshman class results at one of the charter schools, Thomas High School, due to academic dishonesty. Therefore, we were tasked to “clean” the data by removing the math and reading results for the 9th graders at Thomas High School, re-run the analysis, and determine if the changes made impacted the overall analysis. 

## Results

### How is the district summary affected?

The district summary remained relatively the same despite us adjusting the data by removing the math and reading scores of the 9th graders at Thomas High School. See below:

![1](https://github.com/ChristineMitchell/PANDAS_HW/blob/main/School_District_Challenge/Resources/1.PNG)
 
      •	The total number of schools did not change, nor did the number of students in the district or the budget.
      •	The average math score dropped by .1 from 79.0 to 78.9 where there was only a -.13% change.
      •	The average reading score remained the same at 81.9.
      •	The percentage of students who passed math by 70% or more dropped by .2%, hence a -.27% change.
      •	The percentage of students who passed reading by 70% or more dropped by .1%, therefore a -.12% change.
      •	Lastly, the percentage of students who passed both math and reading by 70% or more dropped by .3% with a -.46% change. 

### How is the school summary affected? 

### How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?

There was little to no impact to the school summary results either. The top five schools and bottom five schools remained the same and in the same order. While the scores changed slightly for Thomas High School, the ranking remained the same relative to the other schools.  Again, despite removing the freshman class scores from Thomas High School, we can see that they remain a top performing school in the number two spot. See the top five schools below:

![2](https://github.com/ChristineMitchell/PANDAS_HW/blob/main/School_District_Challenge/Resources/2.PNG)

When we scrubbed the data to address the concerns of academic misconduct, it was important ensure that we were calculating the measurements properly. We could not just remove the scores for the average math and reading score, but we had to recalculate the percentage measurements. To recalculate the percentage of students who passed their tests by 70% or more we not only removed the scores from the numerator, but we needed to update the student count in the denominator by removing the 9th grade students. If this was not done, our data would have been skewed, hence our analysis would have been wrong. As seen below: 

![3](https://github.com/ChristineMitchell/PANDAS_HW/blob/main/School_District_Challenge/Resources/3.PNG)

### How does replacing the ninth-grade scores affect the following:

#### Math and reading scores by grade:

Other than the 9th grade math and reading scores for Thomas High School changing from 83.6 to nan for math and 83.7 to nan for reading, all other scores were not impacted for the Math and Reading Scores by Grade since they are calculated separately. 

![4](https://github.com/ChristineMitchell/PANDAS_HW/blob/main/School_District_Challenge/Resources/4.PNG)

![5](https://github.com/ChristineMitchell/PANDAS_HW/blob/main/School_District_Challenge/Resources/5.PNG)

As well, there was no impact to Scores by School Spending, Scores by School Size, or Scores by School Type. See below.

#### Scores by School Spending:
While there was not a change once the data was cleaned, it is important to note that we do not see an improvement in score with increased spending. A matter of fact, we see the opposite. It would be interesting to look at the budgets to see what programs the money is being put towards.

![6](https://github.com/ChristineMitchell/PANDAS_HW/blob/main/School_District_Challenge/Resources/6.PNG)

#### Scores by school size:
While there was not a change once the data was cleaned, it is important to note that larger schools are not performing as well as medium and smaller schools. 

![7](https://github.com/ChristineMitchell/PANDAS_HW/blob/main/School_District_Challenge/Resources/7.PNG)

#### Scores by school type:
While there was not a change once the data was cleaned, charter schools clearly outperform district schools.

![8](https://github.com/ChristineMitchell/PANDAS_HW/blob/main/School_District_Challenge/Resources/8.PNG)

## Summary
In summary, there was not a significant change to our updated analysis accounting for the removal of the average reading and math scores for the freshman class at the charter school, Thomas High School. The only data tables that changed were the District Summary results with a minimal dip in the results and the Average Math and Reading Scores by Grade (only change were the results to NaN for 9th graders at Thomas High School).  All other data measurements remained the same. Thomas High School ranks 2nds in performance in Percentage of students passing both their reading and math assessments and no other school shifted in their position. Charter schools continue to outperform district schools. Larger schools with over 2,000 students continue to underperform. And, the more a school spends per student does not equate to higher performance.  

