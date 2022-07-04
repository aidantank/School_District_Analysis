# School District Analysis

## Overview of Project
Create a detailed report for the school board regarding math and reading scores based on grade, school spending, school size, and school type. Furthermore, there is suspicion of academic dishonesty for the reading and match scores from Thomas High School ninth graders. Create the same report of reading and math scores, but remove math and reading scores from Thomas High School 9th graders, then determine how the two reports difer if at all.

## Resources
- Data sources: [schools_complete.csv](/Resources/schools_complete.csv) and [students_complete.csv](/Resources/students_complete.csv)
- Software: Python 3.7.13, Jupyter Notebook 6.4.8, Anaconda 4.13.0

## Results

### District Summary
Below are charts of summary data from the district. The top chart has ninth grade data from Thomas High School whereas the bottom one does not. There are minor changes in the reading and math scores. In all the categories, there is a very small decline or no change. This indicates that the data excluded from ninth graders at Thomas High School was a little higher than average, and thus the district summary data is lower when their data is not included.

![](/Resources/district_summary_original.PNG)
> District Summary Unchanged

![](/Resources/district_summary_updated.PNG)
> District Summary Changed

- Summary of Changes:
    - Average Math Score: 79.0 &rarr; <span style="color: red;">78.9</span>
    - % Passing Math: 75.0 &rarr; 74.8
    - % Passing Reading: 85.8 &rarr; 85.7
    - % Overall Passing: 65.2 &rarr; 64.9

### School Summary
The only changes that occur in school summary are for Thomas High School as that is the only school affected by the suspicous activity. Looking at the differences from when the data was unchanged to removing ninth grade math and reading scores, we see a decrease in Average Math Score, % Passing Math, % Passing Reading, and % Passing Overall. We see an increase in Average Reading Score. All of these changes are very small and are less than half a percent.

![](/Resources/school_summary_original.PNG) 
> School Summary Unchanged

![](/Resources/school_summary_updated.PNG)
> School Summary Changed

- Summary of Changes for Thomas High School:
    - Average Math Score: 83.42 &rarr; 83.35
    - Average Reading Score: 83.85 &rarr; 83.90
    - % Passing Math: 93.27 &rarr; 93.19
    - % Passing Reading: 97.31 &rarr; 97.02
    - % Overall Passing: 90.95 &rarr; 90.63

### Top Performing Schools
As noted in the school summary, we see a very minor change in Thomas High School's performance relative to other schools when we remove the ninth grader data. Due to this, we actually see no change in Thomas High School's % Overall Performance compared to other schools. It still ranks 2nd with 90.63 overall passing percentage. However, it is much closer in performance to Griffin.

![](/Resources/top_schools_original.PNG) 
> Top Performing Schools Unchanged

![](/Resources/top_schools_updated.PNG)
> Top Performing Schools Changed

- Summary of Changes:
    - No change in relative postion. Still ranked 2nd in % Overall Passing
    - Amount ahead of Griffin: 0.35 &rarr; 0.03

### By Grade
When viewing the two charts below, we see that the reading and math scores for ninth graders at Thomas High School have in fact been removed. Nothing else has changed, so there is no other change. It is important looking at the Math and Reading Scores Unchanged charts as we can see how similar Thomas High School average ninth grade scores were to tenth through twelfth grade. This shows removing the ninth grade data has little impact on the overall analysis.

![](/Resources/math_scores_by_grade_original.PNG) ![](/Resources/math_scores_by_grade_updated.PNG)
> Math Scores by Grade Unchanged and Math Scores by Grade Changed

![](/Resources/reading_scores_by_grade_original.PNG) ![](/Resources/reading_scores_by_grade_updated.PNG)
> Reading Scores by Grade Unchanged and Reading Scores by Grade Changed

- Summary of Changes:
    - Reading and Math Scores for Thomas High School ninth graders are now `NaN`

### By School Spending, School Size, and School Type
I included only one chart for grouping by school spending, school size, and school type as the charts for changed and unchanged are identical if you round to the nearest whole percent. Thomas High School was in the $631 - 645 bin for school spending, Medium in school size, and a charter school. Thus, these are the only rows that are affected when altering Thomas High School math and reading data. Since this summary data includes more schools than just Thomas High School with each category, the change in math and reading score data is much smaller.

![](/Resources/spending_summary.PNG)
> Performance by School Spending

![](/Resources/size_summary.PNG)
> Performance by School Size

![](/Resources/type_summary.PNG)
> Performance by School Type

- Summary of Changes:
    - The average math and reading scores did not change when looking at 3 significant digits
    - % Passing Math, Reading, and Overal did not change when looking at 2 significant digits

## Summary
Replacing ninth grader math and reading scores at Thomas High School with `NaN` due to potential score altering will change the data. The most effected data is math and reading summaries for Thomas High School itself. I have highlighted four changes that replacing the grades have caused:
 
1. The percent overall passing from Thomas High School has gone down from 90.95% to 90.63%.
2. The average reading score at Thomas High School has gone up from 83.85 to 83.90 out of 100.
3. The percent passing math at Thomas High School has gone down from 93.27% to 93.19%.
4. The percent overall passing for all schools has gone down from 65.2% to 64.9%.