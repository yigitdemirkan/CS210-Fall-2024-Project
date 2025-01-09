# 1. Motivation
The motivation behind this project was to understand if and how my Instagram interactions are influenced by exam periods. Specifically, I wanted to test the hypothesis that interactions on Instagram decrease during times of exams. Additionally, with the recommended topics data which provided by Instagram, I tried to monitor my future activity on Instagram by using a ML model to predict the topics I will be interested in.

# 2. Data Source
The data used in this project was requested from Instagram (see [raw_data file](https://github.com/yigitdemirkan/DSA210-Fall-2024-Project/tree/main/raw_data)) and all kinds of activites are organized in [extracted_timestamps.csv](https://github.com/yigitdemirkan/DSA210-Fall-2024-Project/blob/main/extracted_timestamps.csv). The data for the exam dates are extracted by hand into a txt file ([sınav_tarihleri.txt](https://github.com/yigitdemirkan/DSA210-Fall-2024-Project/blob/main/s%C4%B1nav_tarihleri.txt))

# 3. Data Analysis (in [main.ipynb](https://github.com/yigitdemirkan/DSA210-Fall-2024-Project/blob/main/main.ipynb))
## Data Extraction & Preprocessing:
Timestamps from the activity data were extracted, and only valid (non-null) timestamps were kept.
Both Instagram interaction data and exam dates were converted into a suitable date format using Python's pandas library.
## Group Data:
The data was grouped into two sets: exam periods and non-exam periods based on the date values.
## Statistical Testing:
A Mann-Whitney U test was performed to check for a significant difference in Instagram activity between the exam period and non-exam period.
## Hypothesis Test:
The null hypothesis was that there is no significant difference in interactions between exam and non-exam periods.
The alternative hypothesis was that interactions drop during exam periods.
## Visualization:
A histogram and boxplot were generated to visualize the distribution of Instagram interactions during exam and non-exam periods.
## Future Predictions for Interested Topics:
Using the [recommended_topics.html](https://github.com/yigitdemirkan/DSA210-Fall-2024-Project/blob/main/raw_data/recommended_topics.html) data, the 5 topics which are most likely to catch my interest is listed. I used the TF-IDF vectorization method and Cosine similarity in order to build the relevant ML model. 

# 4. Findings
The statistical test showed that there was a significant drop in interactions during exam periods. This means that, on average, I interact less with Instagram during my exam periods. This finding might reflect that my focus shifts more towards studying and other exam-related activities, leading to reduced social media activity. 

On the other hand, according to the prediciton of ML model, the top 5 topics which are most likely to attarct my attention are:
1) Types of Sports
2) Beauty Product Types
3) Video Games by Game Mechanics
4) Travel by Region
5) Video Games

# 5. Limitations and Future Work
## Limitations:
Besides exams; the quizzes, projects or some other assignments related to school can also result in a decrease in Instagram usage but those factors are excluded in this study.

## Future Work:
For managing time effectively, I can monitor my usage based on this study and I can plan my days or weeks in exam times accordingly. 

# 6. Conclusion
The hypothesis that Instagram interactions drop during exam periods has been validated by the analysis. The significant p-value (indicating a drop in interactions) suggests that I engage less on Instagram during times of high academic pressure, which can be valuable for content recommendation algorithms and understanding social media patterns.
