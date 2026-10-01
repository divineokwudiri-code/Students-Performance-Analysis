# Students-Performance-Analysis| Python(Pandas)
This repo contains a beginner-friendly students analysis project done in Python 

## Overview
This project analyzes the exam results of 1,000 students to understand how background factors such as: gender, parental level of education, lunch type, and test preparation relate to performance in math, reading and writing.
The analysis addresses the following objectives:
- Evaluating the structure and quality of the dataset
- Exploring and filtering the data to answer specific questions (test prep completion, high scorers, etc.)
- Calculating average scores across gender, parental education and test preparation
- Visualizing the distribution of scores and comparing performance by gender
- Delivering a data-backed interpretation of whether test preparation improves performance

The analysis was conducted in Python using Pandas, NumPy and Matplotlib, inside a Jupyter/Colab notebook.

The dataset used in this analysis can be downloaded [here]().

The notebook containing the full analysis is available [here]().

## Table of Contents
- Dataset
- Methodology
- Executive Summary
- Recommendations
- Limitations

### Dataset
This dataset, contains a single file with **1,000 rows and 8 columns**, with no missing values and no duplicate rows.

Key columns include:
- Gender: Male or female
- Race/Ethnicity: Anonymized group, from Group A to Group E
- Parental Level of Education: From "some high school" up to "master's degree"
- Lunch: "standard" or "free/reduced", used as a proxy for socio-economic status
- Test Preparation Course: "none" or "completed"
- Math Score, Reading Score, Writing Score: Exam results out of 100

No further data cleaning was needed, as confirmed by **df.isnull().sum()** and a check for duplicates, both returning zero.

### Methodology
The methodology followed the steps below, matching the structure of the analysis notebook: basic exploration, filtering and conditional selection, group-by aggregation, visualization, and interpretation.

A. Basic exploration: After importing the CSV file, I reviewed the dataset's structure using **df.head()**, **df.tail()**, **df.info()**, **df.shape**, **df.columns**, and **df.dtypes. df.describe()** confirmed that scores range from 0 to 100, and **df.isnull().sum()** confirmed there are no missing values across any column.

![df.info()](
https://github.com/divineokwudiri-code/Students-Performance-Analysis/blob/main/Screenshot%202026-09-28%20142629.png)

B. Filtering & conditional selection: I explored the data using conditional filters to answer specific questions, such as:

picture

I also checked the split between lunch types:

picture

C. Group-by & aggregation: I compared average scores across different groups:

picture

D. Visualization: I created histograms for the distribution of reading and writing scores.

![reading score](https://github.com/divineokwudiri-code/Students-Performance-Analysis/blob/main/Screenshot%202026-09-28%20142524.png)

![writing score](https://github.com/divineokwudiri-code/Students-Performance-Analysis/blob/main/Screenshot%202026-09-28%20142416.png)

E. Interpretation: The final step was translating the group-by comparisons into a written conclusion, answering the guiding question: does test preparation appear to improve performance?

### Executive Summary
Below are the major insights that emerged from the analysis:
- Across 1,000 students, the average scores were 66.1 in math, 69.2 in reading, and 68.1 in writing, giving an overall average score of 67.8.
- Test preparation matters. Students who completed the test prep course scored higher on average in every subject: 69.7 vs 64.1 in math, 73.9 vs 66.5 in reading, and 74.4 vs 64.5 in writing. However, only 358 of 1,000 students (35.8%) completed the course, meaning most students are not taking advantage of it.
- Gender split is subject-dependent. Male students scored higher in math (68.7 vs 63.6), while female students scored noticeably higher in reading (72.6 vs 65.5) and writing (72.5 vs 63.3). Female students had the higher overall average score (69.6 vs 65.8).
- Parental education correlates with performance. Students whose parents hold a master's degree had the highest average scores (69.7 math / 75.4 reading / 75.7 writing), while students whose parents' highest level was high school had the lowest (62.1 / 64.7 / 62.4).
- Lunch type shows the widest gap of any factor. Students on standard lunch scored substantially higher than students on free/reduced lunch across all subjects (70.0 vs 58.9 in math, a gap of over 11 points), suggesting a link between socio-economic status and performance.
- Race/ethnicity groups show a stepped pattern. Average scores rise steadily from Group A (62.99 average) to Group E (72.75 average), the highest-performing group in the dataset.
- Reading and writing scores are highly correlated (0.95), while math is less tightly linked to the other two (0.80–0.82), suggesting math draws on a partly distinct skill set.
### Recommendations
- Promote the test preparation course more aggressively. With only 35.8% of students enrolled and a consistent score advantage for those who complete it, expanding access or making the course a default option could raise performance broadly.
- Target support toward free/reduced lunch students. This group shows the largest performance gap of any factor studied. Additional tutoring, meal support, or after-school resources could help close it.
- Engage parents with lower levels of formal education. Programs that involve these families directly, such as parent workshops or take-home learning resources, could help support students who show lower average scores.
- Reinforce math instruction separately from reading and writing. Since math correlates less strongly with the other two subjects, it may benefit from its own targeted instructional strategies rather than being grouped with general literacy support.

### Limitations
- The dataset does not include the students school, city, or year, so results may not generalize beyond this specific sample.
- The analysis shows correlations, not causes. For example, test preparation is linked to higher scores, but the students who choose to prepare may already be more motivated or supported at home, which could also explain part of the gap.
- Race/ethnicity groups are anonymized, so they cannot be interpreted or explained beyond comparing the numeric results between groups.
- Important context is missing, such as attendance, study hours, class size, and teacher quality, all of which could meaningfully affect scores.
- Lunch type is used as a proxy for socio-economic status, but it is an imperfect one and does not capture household income directly.

Author: Divine | [LinkedIn](https://www.linkedin.com/in/divine-okwudiri-3ab106300/?isSelfProfile=true) | divineokwudiri219@gmail.com

