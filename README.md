# School District Analysis Report


## Section I: Overview of the Analysis

Mariah, the Chief Data Scientist for City School District, hired SATC Consulting to help her with analyzing data on student funding and student standardized test scores. The data sets were analyzed including the reading and math scores for students on standardized tests as well as information on the schools. There were two CSV files provided to us: one for the schools and one for students and their standardized test grades. There were 15 schools and about 39,170 students within the school district. We aggregated the data and showed trends on school performances. The analysis is to assist the school board and super intendent on making strategic decisions and budget priorities.

## Section II: Results

This section provides he results of our analysis. We organized this section based on each area were reviewed. The list below contains our insights on each subject within the overall analysis:


•	**School District Summary**:

<img src='Resources/District Summary Before Changes.png'>
Figure 2-1

<img src='Resources/District Summary Snapshot.png'>
Figure 2-2

*Analysis*: The standardized test scores were administered to all 15 schools within City School District. Of the 39,170 students that were eligible for the tests, all of them sat for their exams. City School District maintained a budget of $24,649,428.

Before the ninth-grade math and reading scores were taken out for Thomas High School, the average math and reading scores for the entire district were 79.0% and 81.9%. The percentages of students who passed math and reading were 75.0% and 85.8%. The overall passing rate for all students within City School District were 65.2%. These results are presented in Figure 2-1.

After the changes were made on the data set with regards to Thomas High School, the average math scores declined to 78.9%  while the average reading scores remained the same at 81.9%.  Both the percentages of students who passed math and reading declined to 74.8% and 85.7% respectively. The overall passing rate for the district decline to 64.9%. The results of this analysis are presented in Figure 2-2. 

•	**School Summary**:

<img src='Resources/School Summary Before Changes.png'>
Figure 2-3

<img src='Resources/School Summary Snapshot.png'>
Figure 2-4

*Analysis*: Figure 2-3 shows the table for all schools before the changes to Thomas High School were made while Figure 2-4 shows the same table for all schools but the effects after the changes were made. As you can see, all of the metrics for each school remained the same before and after the changes with the exception of Thomas Highs School, which we will discuss more in the next section.


•	**Thomas High School’s performance:**

<img src='Resources/Top Five Schools Before Changes.png'>
Figure 2-5

<img src='Resources/Top Five Schools After Changes.png'>
Figure 2-6

*Analysis*: Thomas High School was in second place of the top five performers within the school district with the ninth-grade scores included. Figure 2-5 shows Thomas High School’s position within the top five performers within City School District. As you can see, the average math and reading scores were 83.41% and 83.85% respectively while the percentage of students who passed both subjects were 93.27% (math) and 97.31% (reading). The overall passing rate for the high school was 90.95%.

These numbers declined marginally after the ninth grade scores were taken out. The results are presented in Figure 2-6. Even though the scores declined, they were not enough to change Thomas High School’s number two position within the top five performing high schools within City School District. 


•	**Math and Reading Scores By Grade**

<img src='Resources/Math Scores By Grade Before Changes.png'>
<img src='Resources/Reading Scores By Grade Before Changes.png'>

Figure 2-7

<img src='Resources/Math Scores By Grade After Changes.png'>
<img src='Resources/Reading Scores By Grade After Changes.png'>

Figure 2-8

*Analysis*: As expected, none of the math and reading scores for grades 10 -12 were affected by the removal of 9th grade math and reading scores for Thomas High School. The only metrics affected were the math and reading scores for the ninth graders at Thomas High School. We presented images anyways to show evidence of our results. Figure 2-7 shows both the math (on the top) and the reading scores (on the bottom) for all grade levels before the changes. Figure 2-8 shows the same scores (again, math on the top and reading on the right) for all grade levels after ninth-grade scores were removed for Thomas High School. Again, the only change made was that ninth grade scores for both math and reading at Thomas High School went from numbers to NaN. 

•	**Scores By School Spending**

<img src='Resources/Scores By Spending Before Changes.png'>
Figure 2-9

<img src='Resources/Scores By Spending After Changes.png'>
FIgure 2-10

*Analysis*: We created a new metric called  spending per student and created four bins: “<=548”,  “$585-$629”,  “$630-$644”, and “$645-$675”. Thomas High School’s spending per student was $638 and so fell under the $630-$644 range. Hypothettically speaking, with the removal of the ninth graders’ scores from Thomas High School, the “$630-$644” range should have been the only bin that changed. Interestingly, it did not change at all after the changes were made as you can compare boh Figures 2-9 and 2-10. 

•	**Scores By School Size**

<img src='Resources/Score By School Size Before Changes.png'>
Figure 2-11

<img src='Resources/Score By School Size After Changes.png'>
Figure 2-12

*Analysis*: We organized the data into a new DataFrame by grouping the data according to the size of the school. We created three bins for the all 15 schools within City School District: small (<1,000 students), medium (1,000 – 2,000 students), and large (2,000 – 5,000 students). Thomas High School had 1,635 students and so was considered as a medium-sized school. Just like with the previous analysis where we organized the data by spending per student, we would only expect the categorical data containing Thomas High School to be affected after ninth graders’ scores for the high school were removed. As a result, the medium-sized schools should have been changed. However, none of the scores were affected by the removal of the ninth graders’ scores for Thomas High School. You can see this lack of change by comparing Figures 2-11 (before the changes were made) to Figure 2-12 (after the changes were made). 

•	**Scores By School Type**
<img src='Resources/Scores By School Type Before Changes.png'>
Figure 2-13

<img src='Resources/Scores By School Type After Changes.png'>
Figure 2-14

*Analysis*: Thomas High School was a Charter High School and so we would expect the changes made to its scores by removing the ninth graders’ math and reading scores from the data would have impacted Charter schools. However, as you compare Figure 2-11 (before the changes were made) to Figure 2-13 to Figure 2-14 (after the changes were made), you can see that none of the aggregate data was impacted by the changes.

## Section III: Summary

After reviewing the results of the data analysis that we performed, we can conclude the following:

•	The amount spent per student seemed to have an inverse relationship with student performance on both math and reading scores. Intuitively, you would think the more resources available per student would improve testing outcomes but in reality it did not. We recommend that Mariah and her team think carefully about allocating additional financial resources to schools as this could have no affect on student learning. Indeed, we recommend that she and her team further look into this issue as to why more financial resources leads to worse outcomes. The following questions should be considered in their follow-up analyses: Are the schools with more money misappropriating funds? Are they overpaying for teaching talent that has a negligible effect on student learning? Are the wrong classes or programs being over-funded while more effective classes and programs are being under-funded?

•	School size seemed to be another driver of performance with smaller schools doing better on math and reading standardized tests than larger schools. There are several reasons that could explain this trend but the biggest one we believe that deserves a lot of attention is that bigger schools probably have bigger classrooms per teacher, which means it is difficult for every student to receive the individualized learning he or she needs to do well in school.

•	Finally, the third driver of student performance that we identified within the data analysis was the effect of school type on students’ math and reading scores. Charter Schools, which include Thomas High School, had way more students pass their math and reading tests than district schools. If we could go back and compare the average school size per charter school, we believe that they would have smaller amounts of students per school. This is one metric that we had suggested Mariah should calculate as part of her and her team’s follow-up analysis. The school type results then seem to strengthen our reasoning that smaller students per school, where students can receive more time from their teachers, is a stronger driver than money in terms of improving academic performance. But again, more research and data is needed to confirm these conclusions. 

This marks the end of our report. Please reach out to SATC Consulting if you have any questions. Thank you!





