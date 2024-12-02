# Student-Performance-Prediction-Modeling
## Project Brief
The management of an academic institution has observed the general underperformance of students. Playing the role of a data scientist, I have been tasked with investigating the reasons for poor performance. In addition to this, I was also instructed to create a student performance predictive model to guide teachers and advisors on who could potentially be falling behind before tests and exams arrive. 

I am expected to deliver :
- A dashboard for easy monitoring and comprehension of key variables affecting student performance.
- A performance forecasting model to help the institution predict student performance with a maximum MAE of 2 points.
## Data
  To aid the analysis process, I have been provided with some data. Data fields are identified below:
- Student_ID : The identification number assigned to the student by the school.
- First_Name : The first name of the student.
- Last Name : The last name of the student.
- Age : Student's age.
- Gender : Student's gender.
- Library_weekly_hours : Average number of hours spent in the library per week.
- Class_weekly_attendance_percentage: The attendance percentage of a student for the course in question.
- Extra-curricular_weekly_hours: Average number of hours spent on extra-curricular activities per week.
- Previous_Exam_Score: The previous score of the student in the course in question (this is what we aim to predict)
- Father_Occupation : The occupation of the student's father.
- Mother_Occupation : The occupation of the student's mother.
- Parent_Income_Level: The combined income level of the student's parents.

The dependent variable of interest is the previous exam score. This is the variable we intend to predict and analyze. By examining and modelling the relationship between this variable and others, we can forecast the future performance of a student given relevant information that is already known about the student which can help the school help the student better.

## Project Overview 
To resolve the issues identified in the project brief, three steps would be taken in the analytics pipeline :
- Student performance analysis, including exploratory data analysis and inferential statistical testing (Python).
- Student performance visualization (Power BI). This is to visualize the relationship between student performance and key variables identified in the analysis process.
- Student performance modelling. In this section of the project a prediction model that support performance forecasting would be developed.

## Student performance analysis
EDA and inferential testing were carried out using Python. Key takeaways were:

1. Statistically Significant Relationships:

- Age: Weak negative correlation with exam scores.
- Library Weekly Hours: Moderate positive correlation with exam scores.
- Class_weekly_attendance_percentage: Strong positive correlation with exam scores.
- Extra-curricular Weekly Hours: Moderate negative correlation with exam scores.


2. Non-Significant Relationships:

- Gender: No statistically significant difference in exam scores across the categories.
- Parent Income Level: No statistically significant difference in exam scores across the categories.

## Student performance visualization
A dashboard for understanding and monitoring the relationship between student performance and key variables was developed using Power BI.

![Student Performance Dashboard](https://github.com/user-attachments/assets/5da501b5-d053-4e46-bb62-b29ddf8c06f4)

## Student performance modelling

Due to the nature of the data and the need for explainability, a linear regression model was trained to aid with the prediction forecasting process.

A mean absolute error of 0.83 was recorded on unseen data.

The equation of the regression model was given as:


Previous_Exam_Score = 41.28 + (-0.06) * Age + (8.53) * Average_library_weekly_hours + (11.27) * Class_weekly_attendance_percentage + (-8.79) * Average_extra-curricular_weekly_hours

Subsequently a Streamlit app was built:

![Screenshot (1021)](https://github.com/user-attachments/assets/1088e246-8391-444a-aab9-4118d19b5b9a)


## Conclusion

This project was able to achieve the goals highlighted in the brief. A dashboard and a prediction model was built and the factors affecting student performance were identified.





