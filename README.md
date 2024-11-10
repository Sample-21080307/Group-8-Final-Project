# Group-8-Final-Project
**Group 8 Final Project Report**

   **Topic: Students Improvement Project**
**   Group Evaluation**:

**1.Introduction to the main concept**

  In today's dynamic and complex educational environment, knowing the elements that influence student attainment is critical for promoting development and success. The Students Improvement Project is dedicated to investigating these issues and devising solutions to improve the learning results of different student populations. Using a data-driven approach, this initiative seeks to discover patterns and trends in student accomplishment, giving actionable insights to assist program intervention and support to help students attain their full potential.

  The project's purpose is to not only identify the elements that influence academic success, but also to deliver actionable information to teachers, administrators, and legislators. By integrating data insights, we hope to lay the groundwork for creating supportive and individualized educational environments that are tailored to each student's requirements. This project will assist instructors in making educated decisions and developing individually designed programs to address specific obstacles, close achievement disparities, and provide each kid with the opportunity to develop well-rounded academic and personal skills.

  Through this concentrated approach, the Student Improvement Project intends to establish a culture of continuous improvement by providing educational institutions with the resources they need to increase academic achievement, well-being, and overall student development.

**2.Finding dataset**
  This data is available via the UCI Machine Learning Repository, which is a trustworthy data source since it is censored and updated on a regular basis, assuring correctness and usefulness for study. Many research, scientific journals, and academic documents include data from UCI, which increases the data's dependability. Furthermore, this data warehouse delivers a wide range of data from many domains, making it suitable for a number of machine learning models. 

  The Student Performance dataset in the UCI Machine Learning Repository contains information about students' performance in secondary mathematics and Portuguese language courses. It covers information about demographics, family history, school-related issues, social and behavioral elements, and kids' grades during three periods. This dataset is valuable for assessing and predicting factors that influence academic performance, as well as identifying patterns in student success or issues.

**3.Data Explanation**

  Students performance data has 395 rows which reflect 395 students in both schools and 33 columns which reflect their data. The dataset includes various attributes related to students enrolled in the Math course from two schools: Gabriel Pereira ("GP") and Mousinho da Silveira ("MS"). These attributes cover demographic, academic, and socio-economic factors. The attributes include school, which indicates the student’s school ('GP' or 'MS'), and sex, which shows the student’s gender ('F' for female or 'M' for male). Age records the student’s age, ranging from 15 to 22, while address specifies the type of home location ('U' for urban and 'R' for rural). Famsize describes the family size ('LE3' for families with less or equal to three members, 'GT3' for families with more than three). The Pstatus attribute indicates whether the parents live together ('T') or are apart ('A').

  Parental education is described by Honey and Fed, which show the educational level of the mother and father, respectively, on a scale from 0 (none) to 4 (higher education). Mjob and Job identify the mother’s and father’s occupations, including categories like teacher, healthcare, civil services, at home, or other. The reason for selecting the school is also recorded (home proximity, reputation, course preference, or other), as well as the guardian (mother, father, or other). The traveltime attribute measures the daily commute to school, from less than 15 minutes (1) to over an hour (4), while study time reflects weekly study hours, ranging from less than 2 hours (1) to more than 10 hours (4).

  The attribute failures track the number of previous class failures, with 4 indicating a count of 3 or more. Schoolsup and famsup indicate additional educational support at school and from family, respectively, while paid shows if the student is enrolled in extra paid classes for Math or Portuguese. Activities capture participation in extracurricular activities, nursery records nursery school attendance, and higher reflects the aspiration to pursue higher education. Internet records home internet access, and romance indicates if the student is in a romantic relationship.

  Other attributes provide insights into the student’s well-being and social environment: with fam measures family relationship quality (1 for very bad to 5 for excellent), freetime reflects free time after school, and go out records the frequency of going out with friends. Dalc and Waltz measure alcohol consumption on weekdays and weekends, respectively. Health represents the student’s current health status (1 for very bad to 5 for very good), and absences track school absences, ranging from 0 to 93.

  Finally, academic performance is recorded with G1 (first period grade), G2 (second period grade), and G3 (final grade), each ranging from 0 to 20. G3 serves as the output target for performance prediction, providing a comprehensive view of student profiles that combine demographic, educational, and personal factors with academic outcomes.

**3. Feature Selection**
  In our student improvement project, we carefully selected a set of features that provide a comprehensive overview of critical elements influencing student performance and engagement.

  The features of School and Sex were chosen to reflect demographic and institutional influences on academic achievement. By analyzing these factors, we can assess any differences in achievement patterns between schools or between male and female students, which helps in tailoring supportive measures that address unique challenges faced by specific groups.

  Study time is another essential feature, as it reflects students’ dedication and time management—skills that directly correlate with academic success. By examining the relationship between study time and grades, we aim to uncover how varying study habits affect learning outcomes and identify the optimal level of study commitment for improvement. Paid (extra paid classes) is included to evaluate the impact of additional support outside regular school hours. For some students, extra tutoring can be critical in solidifying their understanding of course content, especially in complex subjects like math and language, where more personalized assistance can make a substantial difference.

  Finally, we selected the academic performance metrics G1, G2, and G3, representing grades across three key periods, as these are direct indicators of student progress and achievement. Monitoring these grades over time enables us to identify students’ growth trajectories, as well as any patterns or deviations that might signal areas needing intervention. Together, these features provide a well-rounded foundation for identifying influential factors in students’ academic journeys, allowing us to design targeted strategies that encourage consistent improvement and support for all students.

**4.Data Cleaning **
  In the source we got the data from, it has described that the data has no duplicated or null value. So we do not have to clean the dataset. The only thing we need to do is make it become easier to process by eyes as the data before was so messy and hard to look at. Columns were all stuck together.

  So we decided to clean the data by using excel, first we press on the “data” on the toolbar. Seccondly, we click on the “get data” button and then choose “from file”. After that we choose “from test/csv” then click on “transform data”. Finally, we get new data that looks perfect which is easier to look at than before. 

**  5. Data Exploration **
In this part, we only choose a GP school to analyze for the project because the number of students in a GP school is much larger than in an MS school. There are 396 students in the data and 350 students are from MP school.

**- The output score of GP students:**

![image](https://github.com/user-attachments/assets/4ad29100-83b4-4447-83cf-2cb0e13f29f5)

Student grading plot from the school GP (Gabriel Pereira) - Red is overall grades G3 The x-axis is the score ranges, and y-axis the number of students that fall into each score range. This chart outlines student performance at this school which allows us to see how many grades did students achieve.

Almost 45 students obtained between 9 and 10 marks, which was the most frequent score interval. This indicates that most of GP school students are average performers in their studies. The cluster of scores in the middle indicates that a sizable number of students may be receiving passing, but not impressive marks.

The score distribution appears somewhat symmetrical and skewed slightly to the right, with fewer students scoring at the top (17-20) than in the low and middle ranges. This shows that the number of students achieving excellent scores is still small, and a significant proportion of students are still average or below average. Despite this, there are still some students who score very low (0-1) and high (15-16), indicating a degree of diversity in academic performance.

Since the majority of students scored below the average 10, this chart shows there is plenty of room for improvement. Strategies can focus on helping students move from low average scores (7-10) to higher scores, helping them improve their academic performance. Overall, this distribution indicates that the majority of GP students have average to slightly below average results, and only a small number of students achieve excellent or very low scores. This information can help guide interventions to improve academic outcomes for student groups clustered around the average.

**-	The output score of male and female in GP school **

![image](https://github.com/user-attachments/assets/191450c5-ff69-45a3-87bc-d6a3b7c873bc)

The boxplot of male and female students' final grades (G3) shows a few notable differences. The median score for male students is higher than that for female students, suggesting that on average, male students tend to have slightly better academic results. The median is a reliable measure in the presence of outliers, as it is not affected by scores that are too high or too low. This shows the difference in average scores between the two gender groups.

The interquartile range (IQR) of both groups was of similar width, meaning that the diversity of scores in the two groups was quite similar. However, the IQR of male students was slightly higher than that of female students, demonstrating that the majority of male students scored better. This reinforces the observation of differences in the academic performance of male and female students. Although this difference is not huge, it is still noticeable.

Both groups of male and female students have an outlier at a score of 0. This may represent cases where students did not complete the exam or had particular difficulties in learning, leading to a lower score. low number. However, because these are outliers, they do not greatly affect the median of the two groups. Outliers at 0 reflect some isolated cases that need attention but are not a general trend.
In addition, the score distribution range of both groups of students is quite wide, ranging from 0 to over 20 points. This shows that there is wide variation in student performance, with both groups containing students with very high scores and students with low scores. This wide distribution shows that not all students achieve average scores but that there are significant differences between individuals.

To support female students in improving their academic performance and narrowing the gap with male students, separate learning support programs for female students can be established. Mentoring sessions or group study sessions with the guidance of teachers or excellent students will help female students better understand knowledge. These tutoring sessions can be held weekly and focus on subjects in which female students often struggle. Besides, developing soft skills is also an important factor to help female students improve their academic results. Some female students may have difficulty managing their time or lack confidence in studying. Schools can organize soft skills workshops with topics such as “Effective time management” or “Building confidence in learning”. For example, in a workshop, experts can guide students on how to create a daily schedule to divide study time appropriately, or how to determine short-term and long-term learning goals. In addition, children can participate in inspirational talks with speakers who are successful people, especially women, to gain more motivation and belief in their own abilities.

Finally, building a supportive learning community among female students will also bring many benefits. After each exam or test, teachers can conduct individual meetings with each female student whose score is not good to provide specific feedback and plan their improvement. For example, if a student has a low score on a Literature test, the teacher can point out errors, helping the student identify areas that need improvement (such as analytical, reasoning, or writing skills). At the same time, teachers and students together set specific goals for the next exam, such as achieving a higher score on text analysis or practicing essay writing in a shorter time. This personalized plan will help female students clearly identify their weaknesses and have specific directions for progress. In general, these measures are aimed at creating favorable conditions for female students to develop their learning abilities and improve their achievements. Creating an equitable and supportive learning environment will help students become more confident, overcome learning obstacles, and be ready to face future challenges.

**-	Study time of female students under 11 score**

![image](https://github.com/user-attachments/assets/c0e31ec9-4d6a-4058-a352-053178b0f40f)

As we can see from the pie chart above, most female students with scores lower than 11 in self-study spend only 2 to 5 hours per week on outside learning. In particular, the proportion of second group students may be largest with 62.64%, while groups who spend less than 2-5 hours or more than 2-5 hours per week have a lower proportion. However, here we can see that the self-study time of students is still not much – especially for high school students, which age, if only referring to knowledge improvement and exam preparation, will be an age when the role of self-study is extremely important. important exam.

In fact, for high school students, spending only 2 to 5 hours per week on self-study is too little to achieve high learning efficiency. With increasingly complex knowledge requiring mastery from many subjects, students need to spend more time self-reviewing and consolidating knowledge outside of class. If students only study 2 to 5 hours per week, this can lead to a superficial grasp of knowledge, easy to forget, and lead to low scores. Especially among these female students, there are cases where they received a score of 0 in the final grade.

In order to improve the situation, several particular procedures can be taken. First, schools should establish academic clubs where students can engage in conversations, share knowledge, and assist one another in their studies. Second, accomplished female speakers from a variety of industries should be invited to share their experiences and motivate students.Tales of achievement will inspire and motivate you to pursue your dreams. Successful female speakers include Ms. Shark Thai Van Linh, Nguyen Phi Van, PhD. Ta Minh Trang, and... Finally, the school can provide group study sessions or individual coaching in which instructors teach you how to study effectively, manage your time, and complete difficult work. These tactics not only improve learning interest, but also contribute to a positive and welcoming learning environment.

In general, to improve academic performance, students need to increase their self-study time, especially beyond 2 to 5 hours per week. Diverse solutions from teachers, parents, and the students' own efforts will help them develop better self-study habits, thereby improving their learning results.

**- Having extra lesson or not :**
![image](https://github.com/user-attachments/assets/7796484a-f2a3-4d48-9a9f-c8f8d82b3c7e)

The chart provided shows that among the female students, 96 chose to participate in paid extra classes, while 87 did not. This reflects a nearly even split between those who choose to take extra classes and those who do not. This divide raises questions about why some students choose to participate and others do not, as well as about the effectiveness of tutoring on academic achievement.
From the chart, we see that the scores of students who take extra classes and those who do not take extra classes do not differ much, but the scores of these two subjects are not high. The cause may be from the school or from the student, which leads to the student's score.

On the school side, the teacher's teaching technique may either stimulate or demotivate pupils' enthusiasm in learning. Many teachers may still employ traditional teaching methods, which frequently involve one-way lectures from the teacher, with pupils mostly taking notes and receiving information. Students who merely listen to lectures may have less opportunity to debate and ask questions, resulting in a lack of in-depth understanding of the material. This can lead to bad test outcomes, as well as pupils feeling bored and disengaged from the learning process. Furthermore, the quality and relevancy of the curriculum influence pupils' ability to absorb information. Students may not attain satisfactory outcomes if the program is out of date or does not meet real-world requirements.  For example, we should change and improve the program such as opening more extracurricular classes on "hard and soft skills in life" to encourage student participation and initiative. Invite psychologists with good expertise to discuss and share about the topic you want to target. Organize training courses for teachers on modern teaching methods and how to apply technology to teaching, helping students be more flexible in imparting knowledge.

On the other hand, some students with poor scores may not feel interested or aware of the importance of studying, and do not have specific goals, leading to them not making efforts in studying. Many students do not know how to take notes, review or take tests effectively, leading to poor knowledge absorption. Guide students on how to identify specific, feasible and measurable learning goals. Help them understand why learning is important. Use small rewards (such as bonus points, certificates) to encourage students to complete assignments and actively participate in class. Organize training sessions on note-taking techniques, reading comprehension and effective review methods. Encourage students to practice newly learned skills through exercises and small projects to reinforce their knowledge.

Finally, encourage students to set personal goals and develop specific study plans. Parents' participation in monitoring and evaluating their children's learning progress is also very important, helping to motivate and encourage students to continue trying, thereby gradually improving their scores and progress. long term development.

**6. Building and Evaluating Model**

**a.	Heat map: There are only two predictable components: G1 and G2**

![image](https://github.com/user-attachments/assets/7a716a51-226a-4787-b71c-2638b77d9817)

From the heatmap, we see clearly that G1 and G2 have the highest correlation to G3, with coefficients of 0.801 and 0.905 respectively. This indicates that G1 (First exam score) and G2 (Second exam score) are strong indicators that predict final grades (G3). Students' scores on these two exams fairly accurately reflect their final results, highlighting the importance of maintaining consistent performance across each exam.

**b.	Linear regression:**

+	**Check Linearity of G1, G2, G3:**

![image](https://github.com/user-attachments/assets/e376f9ef-914f-46d9-ad59-ee347be80f21)

Based on the chart, we can analyze the linear relationship between the scores of three semesters: G1 (semester 1 score), G2 (semester 2 score), and G3 (final score). The chart shows the pairwise relationship between scores, helping us easily see the degree of connection between each semester.

First, the relationship between G1 and G2 exhibits a strong linear correlation. The data points are distributed in a clear diagonal line, showing that students who score high in G1 also tend to score high in G2, and vice versa. This implies that factors that affect students' scores in the first semester may continue to influence their scores in the second semester. It can be said that the score in the first period is a pretty good predictor of the score in the next period.

Next, the relationship between G2 and G3 also shows a very strong linear correlation. The strong association between G2 and G3 suggests that second term scores are an important factor in predicting final scores. Students with high scores in G2 will often score high in G3. This may be because subsequent semesters have many similar elements in terms of learning content or assessment, making scores in previous semesters accurately reflect the final results.

Finally, the relationship between G1 and G3 also shows linearity, but appears to be weaker than the relationship between G2 and G3. This shows that the first semester's score also affects the final score, but not as strongly as the influence of the second semester's score. However, the existence of a linear relationship between G1 and G3 still suggests that grades from previous semesters may be valuable in predicting final grades.

Overall, the graph shows a strong linear relationship between scores across the three periods, especially between consecutive scores (G1-G2 and G2-G3). This suggests that previous scores are good indicators of future scores, and shows the potential for applying a linear regression model if we want to predict final G3 scores based on G1 and G2.

+	**Creating model:**

![image](https://github.com/user-attachments/assets/ff2b675d-530b-4c24-8f31-c7a790d58294)
![image](https://github.com/user-attachments/assets/1eab5131-0b72-4ddb-ae0b-543d83714075)
![image](https://github.com/user-attachments/assets/b2a823bd-867d-4e5c-80ab-9c76ab6aed0d)

**Data Preparation**
  First, create the variables X and y, in there X includes columns G1 and G2 from DataFrame reg, and y is the column G3 also from this DataFrame. Then use functions train_test_split from the library sklearn to divide the data into training set and test set, with the test set ratio being 30% of the total data with random_state ensuring consistency across different runs. This is important to be able to evaluate the model on unseen data, ensuring the model is highly generalizable.
Building a Regression Model

  After the data has been divided, you have built a linear regression model using the Ordinary Least Squares (OLS) method from the library state models. This model is trained on the training data set to find the relationship between G1 and G2 for G3. I use the formula "G3 ~ G1 + G2" to specify that G3 is the dependent variable and G1, G2 are the independent variables. The model is trained on the training set and evaluated on both the training set and the validation set to test its accuracy and generalization ability.

**Model Evaluation**
  After the model has been trained, I calculate model evaluation metrics on both the training set and the test set, including R-squared (R²) and Root Mean Squared Error (RMSE). R² indicates how well the model fits the data (higher is better, maximum is 1). The results show that R-squared for the training set is 0.935 and for the testing set is 0.936, showing that the model explains well 93.5% to 93.6% of the variation of G3 scores from G1 and G2. RMSE provides an estimate of the average error of predictions with Train RMSE: 0.8237969065067964 and TEST RMSE: 0.7981245595750468. We can see that RMSE is slightly different in the two sets, but still meets the requirements because these two results are very small. Both of these metrics show that your model is performing quite well. 

  The QQ plot is used to check whether the residuals (error between prediction and actual) follow a normal distribution, which is very important in linear regression. The graph shows that the model residuals do not completely follow a normal distribution, which can affect the reliability of model estimates and related statistical tests. It is worth noting that the points at both ends of the graph, especially at the right end and left end, deviate significantly from the straight line. This indicates residuals that are not normally distributed, with the presence of noise or outlier data points, or possibly residuals that tend to be skewed. Data points that are very far from the straight line in the QQ plot indicate the existence of outliers in the data. These outliers can distort parameter estimates and reduce the model's predictive ability.

**Conclude**
  The analysis shows that there is a slight difference between the model performance on the training set and the test set, which may indicate that the model is not severely overfitting but still needs monitoring. The histogram shows that some residual scores do not follow a normal distribution, especially at the two ends of the distribution. This can be a problem if the residuals are non-random, affecting the underlying assumptions of the linear regression model and possibly reducing the reliability of the parameter estimates. This shows that the model is not completely good and needs further improvement.
  
  In my opinion, One potential solution is to apply a logarithmic transformation to the variables G1, G2 and G3. This transformation not only helps minimize the influence of outliers but can also help make the residual distribution more normal. After applying the transformation, the model needs to be re-evaluated to determine if the improvement is effective, using R² and RMSE metrics as well as a new QQ Plot.

+	**Model summary when logarithm data :**
![image](https://github.com/user-attachments/assets/f280155d-017a-4f92-8375-cd7013b46188)
![image](https://github.com/user-attachments/assets/bcf46619-af5f-4de7-bef8-958be0af0c04)

  This new code made a significant change: applying a logarithmic transformation to the independent variables (G1, G2) and dependent variable (G3). Logarithmic transformation is often used in regression analysis to solve problems such as heteroscedasticity, improve the linearity of the relationship between variables, and make the data distribution closer to more normal distribution.

X = np.log(X)
 y = np.log(y)

1.	This reduces bias due to outliers and improves normality of residuals, an important assumption in linear regression.\

2.	Data Division: The code further divides the data into training and testing sets, using a ratio of 70% for training and 30% for testing, keeping the same random_state to ensure reproducible results.
  
3.	Building and Evaluating Regression Models: The training and prediction steps do not change compared to before logarithmic transformation. However, model evaluation is now based on transformed data, with a constant model formulation of G3 ~ G1 + G2.
  
4.	Model Evaluation:
○	R-squared (R²) and RMSE were calculated for both training and testing sets. These values indicate that the model is able to explain the data well, with a high R² indicating a close fit of the model to the data.
○	A low RMSE indicates that the error between the predicted and actual values is small, which is both a positive result and shows that the regression model has improved significantly after applying logarithms.

5.	Check Residuals (QQ Plot):
○	The code uses QQ Plot to check whether the residuals follow a normal distribution or not. The results show a significant improvement in the fit of the residuals to the normal line, which increases the validity of the regression model.

**Conclude**
The regression model was significantly improved through the application of logarithmic transformation. The high R² and low RMSE indices along with the residuals conforming better to the normal distribution show that this model is suitable and has good applicability in practice. The improved QQ Plot shows that the assumptions about the residuals of the regression model have been satisfied, thereby increasing the reliability of the estimates and statistical tests.
This regression model, once properly adjusted, can be accepted for use in contexts requiring high accuracy and reliable prediction. This highlights the importance of considering appropriate transformations for the data during regression model building, especially when input values show uneven distributions or trends. exception.

+	**Check observation independence (whether auto-correlated)**
![image](https://github.com/user-attachments/assets/043fb99c-3e14-47b6-9770-0a053659109a)

R-squared và Adjusted R-squared: Both of these indices are high (R² = 0.917 and Adjusted R² = 0.915), which shows that the model explains 91.7% of the variation of the dependent variable from the independent variables. This also proves that the model is very effective in explaining data.

F-statistic and Prob (F-statistic): The F-statistic value is 580.6 with a very low p-value (1.70e-57), this confirms that the model is statistically significant with high reliability.

Durbin-Watson: This index is used to check for autocorrelation in the errors (autocorrelation) of the regression model. The Durbin-Watson index near 2 (1.865) indicates a very slight, but generally acceptable, degree of autocorrelation. This index typically ranges from 0 to 4, with 2 indicating no autocorrelation, values less than 2 indicating positive autocorrelation, and greater than 2 indicating negative autocorrelation.

This linear regression model, after applying transformations and thorough evaluation, was found to be suitable and effective for predicting the final grade (G3) from the grades of the previous two periods. The high R² index and low P-value from the F test show that the model is very robust. The slight autocorrelation detected through Durbin-Watson is noteworthy but not a major concern, suggesting that the model can be accepted and used in practical predictions while still maintaining robustness. Reliable and high accuracy. 

+	**Check homoscedasticity**:
![image](https://github.com/user-attachments/assets/8c09b084-d60a-4806-a496-06575fdce691)

The scatter plot between predicted values and residuals is an important tool for testing the assumptions of regression models, specifically homoscedasticity and no pattern. in the distribution of the residuals.

One of the key assumptions of linear regression is that the variance of the residuals should be consistent across all values of the independent variable. In the plot you provided, the residuals are distributed around the horizontal line at 0 and there is no tendency to increase or decrease variance at higher or lower predicted values, which is a good indication of the variance. false uniformity.

The plot shown shows no correlation between the predicted values and the residuals, and shows a uniform distribution of the residuals around zero with no obvious pattern. This indicates that your regression model has achieved the requirement of no correlation between the predicted values and the residuals, and also that the variance of the residuals is preserved at all levels of predicted values. This increases the confidence of the regression model, allowing the prediction to be considered reliable and not influenced by unmodeled latent factors.

+	**Interpret model: **
+	Coefficients (G1 and G2):
●	G1: The coefficient for G1 is 0.1001 with a p-value of 0.095, indicating that G1 has a positive effect on G3 but is not statistically significant.
●	G2: The coefficient is 0.8634 with a p value close to 0, showing that G2 has a very large and significant influence on G3. This confirms that G2 is a strong predictor of final G3 scores.

The regression model shows that G2 is the main factor influencing G3 scores, while G1 has no significant impact considering the presence of G2. This can help educators recognize the importance of maintaining stable academic performance across semesters to achieve better results in the final exam.

This model also provides compelling evidence that focusing on improving previous semester scores will have direct benefits on final results, especially G2 scores, thereby supporting educators in developing Develop teaching strategies and support students.

**c. Logistic Regression**

**-	Convert the results of column 'higher':**
Use functions abc() aims to convert the value of the 'higher' field from text ('no', 'yes') to numeric (0, 1):
●	abc(x): This function checks if the value of x is 'no' then returns 0, if not (ie 'yes') then returns 1.
●	Apply function: The function is applied to the 'higher' column of the DataFrame df use method .apply(). The result is a new 'higher' column with the value 0 or 1 instead of 'no' or 'yes'.

**-	Binning values in the grade columns (G1, G2, G3):**
![image](https://github.com/user-attachments/assets/b6840cd1-e51f-4939-a330-caf5e38dab6d)

G1, G2, and G3 columns, which represent grades from three different periods. A new function, ghi, is created to categorize these grades into four performance levels or bins. Specifically, the function assigns a grade between 0 and 5 to bin 1, a grade between 5 and 10 to bin 2, a grade between 10 and 15 to bin 3, and a grade between 15 and 20 to bin 4. By binning the grades, the code converts continuous grade values into categorical performance levels, which may simplify analysis or make it easier to identify patterns in student performance.

-	**Prepare the data and divide it into training and test sets**
+	Input variable and target variable:

X = dft[['G2']]
 y = dft[["higher"]]
 
In this step, input variable X selected as column G2, which can be a score or the results of a previous test. Variable target and is the column higher, can be a binary categorical variable (yes or no), representing whether the student wishes to continue further education or not. This code helps us prepare input data and target variables for the Logistic Regression model to make predictions based on.

**+	Split the data into training and testing sets:**
The data is divided into two sets: 70% for the training set (X_train, y_train) and 30% for the test set (X_test, y_test). This division ensures that the model has enough data to learn (training) and has a separate data set to evaluate performance (testing). Parameter random_state=0 makes the data division process reproducible, ensuring that reruns will produce the same division result.

**-	Build and train the Logistic Regression model**

After preparing the data, we proceed to build the Logistic Regression model. This is a binary classification model, suitable for predicting whether a student wishes to pursue higher education or not. The model is trained using data X_train and y_train. During training, the model learns how to relate scores G2 and the likelihood that students have a desire to pursue higher education (variable higher). After training the model, it will predict labels for the training and test sets, and evaluate the prediction results based on metrics such as Precision, Recall, and F1-score. This helps evaluate the model not only for its accuracy but also its ability to detect important cases.

**-	Predict and evaluate the model on the training set**
In this step, the model will use the learned information to predict the labels of the data in the training set. Prediction results are saved in y_p:
ma_train = confusion_matrix(y_train, y_p) 
pre_train = precision_score(y_train, y_p) 
recall_train = recall_score(y_train, y_p) 
f1_train = f1_score(y_train, y_p)

Performance metrics on the training set are calculated to see how the model performs when applied to the same data it learned from:

●	Confusion Matrix (my_train): The confusion matrix provides a detailed analysis of the number of correct and incorrect predictions of the model.
●	Precision (pre_train): Measures the model's accuracy in predicting "yes" cases (i.e., of the "yes" predictions, how many are correct).
●	Recall (recall_train): Measures the model's ability to detect all true "present" instances in the data.
●	F1-score (f1_train): Is the harmonic average between Precision and Recall, helping to evaluate model performance in a balanced way.

**-	Predict and evaluate the model on the test set**
Once the model has been trained, we will evaluate it on the test data set X_test to see how the model performs with new data. The prediction results on the test set are stored in y_p1:

ma_test = confusion_matrix(y_test, y_p1) 
pre_test = precision_score(y_test, y_p1) 
recall_test = recall_score(y_test, y_p1) 
f1_test = f1_score(y_test, y_p1)

Similar to above, we calculate the Precision, Recall and F1-score indices for the test set to evaluate the model's ability to generalize to new data.

**-	Analyze results:**
![image](https://github.com/user-attachments/assets/d4040287-2b34-4c4d-aa4e-54a84a33d247)

  On the training set, the model achieved high accuracy with Precision of 0.9565, Recall of 1.0, and F1-score of 0.9777. Precision measures the proportion of correct predictions among "yes" cases, indicating that the model makes few errors when predicting the "yes" label. A recall of 1.0 shows that the model did not miss any "yes" cases. F1-score is the harmonic average value between Precision and Recall, showing that the model maintains a good balance between these two factors, helping to evaluate overall performance more accurately. This shows that the model performs very well when applied to the data set on which it was trained.

  On the test set, the model also showed impressive results with Precision of 0.9327, Recall of 1.0, and F1-score of 0.9652. Precision on the test set shows that the model can correctly identify "present" instances in the data that have never been seen before. Similar to the training set, Recall reaches 1.0, ensuring that all "yes" cases are detected. F1-score on the test set is high, proving that the model maintains stable performance when switching from training data to test data. This proves that the model not only learns well from training data but also generalizes well when faced with new data.

  In summary, the evaluation indicators show that this Logistic Regression model works very effectively with this data, is able to predict accurately and does not miss "yes" cases. High Precision and Recall on both the training set and test set show that the model does not suffer from overfitting (overfitting the training data) but generalizes well to the test data. In particular, Recall reaching 1.0 shows that the model detects all "yes" cases without missing them. This shows that the model is not overfit but generalizes well to new data

8. Conclusion

  In conclusion, the Students Improvement Project has identified key factors that significantly impact student performance and outlined actionable strategies to enhance academic outcomes. Through analyzing data on demographics, family background, study habits, social behaviors, and previous academic performance, we found that consistent study time, positive family support, and engagement in school activities are crucial for student success. Additionally, strong correlations between students' scores across different grading periods highlight the importance of early interventions and support, as students who perform well in initial periods are likely to continue succeeding.

  Based on these findings, targeted support programs can be developed, such as personalized tutoring sessions, workshops on time management and study skills, and community support systems that involve family members. By fostering a supportive learning environment both inside and outside the classroom, educators, parents, and policymakers can work together to address individual student needs, reduce barriers to learning, and encourage a culture of continuous improvement. The insights from this project provide a foundation for ongoing initiatives to enhance student engagement, boost motivation, and ultimately improve educational outcomes across diverse student populations.

**REFERENCES **

-	Student Performance Data retrieved from: https://archive.ics.uci.edu/dataset/320/student+performance
-	“Why embracing a growth mindset is important to students” retrieved from:https://www.beanstack.com/blog/why-embracing-a-growth-mindset-is-important-for-students 
-	“Academic performance: how can it be improved?” retrieved from: https://www.britishschoolbarcelona.com/blog/academic-performance-how-can-it-be-improved/ 
-	“The Importance of Skill Development for Students” retrieved from: https://www.drishtiias.com/blog/the-importance-of-skill-development-for-students 
-	“9 Effective Strategies for Improving School Performance” retrieved from: https://pioneerseschool.com/en/effective-strategies-improving-school-performance 
  



