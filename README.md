java c
ECON 2300: INTRODUCTORY ECONOMETRICS
Research Project 1
Background
You are interested in estimating the effect of education on earnings using data on wage and educ. Here, wage is measured in dollars per hour. Thus, for a particular person, if wage = 6.75, the hourly wage is $6.75. Also, educ denotes years of schooling; for example, educ = 12 corresponds to a complete high school education. The data file wage4hw1.xlsx contains 526 individuals, who were randomly drawn from the population of people in the US workforce in 1976. The dataset has additional variables.
• exper: years potential experience
• tenure: years with current employer
• profocc: =1 if in professional occupation
• clerocc: =1 if in clerical occupation
• servocc: =1 if in service occupation
Submission of your report
Your report must be single-spaced and in 12 Font size. You should give your answer to each of the following questions following a similar format of the solutions to the tutorial problem sets. When you are required to use R, you must show your R command and R outputs (screenshots or figures generated from R). You will lose 2 points whenever you fail to provide R commands and outputs. For each question, when you are asked to discuss or interpret, your answer has to be brief and compact. You will lose 2 points if your answer is needlessly wordy. You must upload your assignment on the course webpage (Blackboard) in PDF format. (Do not submit a hard copy.)
Research tasks
1. (7 points) You are given a dataset in an Excel format. Figure out how to load this dataset in R. Provide your R-commands to load the data. In particular, be clear about which R-package you install and use. (Hint: use the Internet. There are several different ways of doing it.)
2. (15 points) Obtain summary statistics and histograms for the variables wage and educ and scatter diagram of those two variables. For the diagrams, give informative titles and variable names instead of just using the default titles and variable names. For example, you could use Years of Education in place of educ. Discuss the data characteristics.
3. (9 points) Estimate the linear regression
wagei = β1 + β2educi + ui,
where uiis the error and β1 and β2 are the unknown population coefficients. Assuming that E[u|educ] = 0, interpret the estimated coefficient on educ (3 points) and test whether or not the population coefficient is zero at the 1 % significance level (3 points). What is the predicted wage of a person with eight years of education (3 points)
4. (8 points) Estimate the linear regression
ln(wagei) = β1 + β2educi + ui,
where uiis the error and β1 and β2 are the unknown population coefficients. Assuming that E[u|educ] = 0, and using the estimates, what is the predicted change of wage for every additional year of education (3 points)? Then, interpret the R2(2 point). This numeric value of R2 here can be similar to that of the regression in Question 3. However, they are conceptually different. Explain the difference (3 points).
5. (6 points) You suspect that the hourly wage could depend on experience (years of potential experience). Discuss under what condition(s) the estimated coefficients in the previous questions would be biased due to the omission of the experience (2 points). Give a reasonable and intuitive story on why omission of experience would cause omitted variable bias in the regression with only educ like in the previous question (2 points). Under your story, explain whether the estimated coefficient on educ in Question 4 would be overestimated or underestimated (2 points).
6. (4 points) The variable exper is years of potential experience. Regress ln(wage) on educ and exper. Discuss the estimation results. In particular, explain statistical significance and the difference between the estimated coefficient o代 写ECON 2300: INTRODUCTORY ECONOMETRICS Research Project 1
代做程序编程语言n educ in this regression and that in Question 5.
7. (6 points) tenure is years with current employer. Since tenure captures the productivity of the individual at a particular job, we may consider it as a determinant of hourly earnings. Regress ln(wage) on educ, exper, and tenure (3 points).
Using the estimates, compute the estimated effect on wage when an individual stays at the same firm for another year (3 points). Note that when tenure increases by one year, exper must also increase by one year.
8. (8 points) Is your predicted effect in Question 7 statistically significantly different from zero at the seven percent of level? Clearly write down the null hypothesis (3 points). Test your hypothesis using R by loading relevant packages (2 point). Explain your decision whether to reject the hypothesis (3 points).
9. (7 points) Occupation is a critical determinant of wage. The data has three binary variables, each indicating a certain category of occupations. Run the regression in Question 7, but extending it by including those three occupation dummies on the right-hand side of the regression equation (2 points). Discuss the estimated coefficients on exper and tenure in this regression comparing them against the estimates in Question 7 (3 points). If you find that the estimated coefficient on exper in Question 7 is biased compared to that in this question, provide plausible explanation for the bias (2 points).
10. (7 points) Modify and estimate the regression model in Question 9 to allow for the effect of educ on wage to differ across the four occupation categories. Which occupation category has the largest effect of educ on wage, i.e., returns to education (or schooling) (2 points)? What is the returns to education for that occupation category (3 points)? Are the returns to education of that occupation statistically different from that of the benchmark occupation at the 5% significance level (2 points)?
11. (7 points) Jenny is a waitress (service) who has worked for two years with no interruption right after she finished high school, i.e., educ = 12 and exper = tenure = 2. What is her predicted hourly wage (2 points)? Suppose that she quits her job, studies at a community college for one year, and comes back to the same cafe taking the same serving position. What would be her predicted hourly wage (3 points)? Is the difference statistically significant (2 points)? Use the regression results in the previous question.
12. (16 points) The returns to schooling may not be linear in years of education. For example, increasing years of schooling from 12 years to 13 years, high school diploma to some college, would be different from increasing it from 15 years to 16 years, some college to bachelor’s degree. Therefore, it may be more useful to estimate the effect on earnings of education by using the highest diploma/degree rather than years of schooling. Define four dummy variables to indicate educational achievements;
• lt hs = 1 if educ < 12
• hs = 1 if educ = 12
• col = 1 if educ ≥ 16
• some col = 1 for all other values of educ.
(a) Create the dummy variables (lt hs, hs, col, some_col) as defined above and regress wage on lt_hs, hs, and col (including a constant, as usually). (4 points)
(b) Compute the sample average of hourly wage for individuals with some university education but do not finish university. (3 points)
(c) Compute the sample average of hourly wage for individuals who finished high school with 12 years of education. Is the difference statistically different compared to the individuals in part (b)? (4 points)
(d) Compute the sample average of hourly wage for individuals who achieved a Bachelor’s degree Is the difference statistically different compared to the individuals in part (b)? (5 points)





         
加QQ：99515681  WX：codinghelp
