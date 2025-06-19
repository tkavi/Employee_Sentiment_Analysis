# Employee_Sentiment_Analysis
This project is to analyze an unlabeled dataset of employee messages to assess sentiment and engagement trends. Using natural language processing and statistical analysis, the goal is to:  
•	**Sentiment Labeling**: Automatically label each message as Positive, Negative, or Neutral.  
•	**Exploratory Data Analysis (EDA)**: Analyze and visualize the data to understand its structure and underlying trends.  
•	**Employee Score Calculation**: Compute a monthly sentiment score for each employee based on their messages.  
•	**Employee Ranking**: Identify and rank employees by their sentiment scores.  
•	**Flight Risk Identification**: A Flight risk is any employee who has sent 4 or more negative mails in a given month.  
•	**Predictive Modeling**: Develop a linear regression model to further analyze sentiment trends. 

### Setup
**Requirements**
- IDE to run the code (Jupyter Notebook preferred)
- Support for Python 3.9 or higher

**Installation**
Install the required libraries (pip preferred) :
- pip install transformers
- pip install torch --index-url https://download.pytorch.org/whl/cpu
- pip install wordcloud

Libraries Used :
  - pandas
  - numpy
  - matplotlib
  - seaborn
  - scikit-learn
  - transformers
  - wordcloud

### Usage
- Place the input dataset (test.csv) in the project directory.  
- Run the main Jupyter notebook or Python script to perform all the above mentioned tasks.  
- Charts, graphs and images are saved to the Visualization folder.  
- Use the input prompts to query rankings for specific months and years.

### Methodology 
Sentiment Labeling :  
- Utilized Hugging Face’s DistilBERT fine-tuned on SST-2 for automated sentiment classification.  
- Messages were labeled as Positive, Negative, or Neutral based on model predictions with a confidence threshold.  
- This approach provides reproducible, scalable sentiment labeling without manual annotation.  

Exploratory Data Analysis (EDA) :  
- Explored dataset size, structure, and missing values.   
- Analyzed sentiment distribution and trends over time.  
- Examined message lengths by sentiment and employee communication patterns.  
- Created word clouds to visualize common themes in positive and negative messages.  

Employee Score Calculation & Ranking :  
- Assigned scores to messages (+1 for Positive, -1 for Negative, 0 for Neutral).  
- Aggregated scores monthly per employee.  
- Ranked employees monthly to identify top 3 positive and negative communicators.

  The top three positive and negative employees for **Feb 2011** are:   
  **Top 3 Positive Employees:**  
  | Employee                  | sentiment_score |
  | --------------------------| --------------- |
  | lydia.delgado@enron.com   |               2 | 
  | eric.bass@enron.com       |               1 |
  | patti.thompson@enron.com  |               1 | 
  
  **Top 3 Negative Employees:**  
   | Employee                     | sentiment_score |
   | -----------------------------| --------------- |
   |  kayne.coulter@enron.com     |            -4   |
   |     sally.beck@enron.com     |            -4   |
   |  bobette.riner@ipgdirect.com |            -3   | 

Flight Risk Identification :  
- Defined flight risk employees as those sending 4 or more negative messages in any rolling 30-day window.  
- This metric flags potentially dissatisfied employees for early intervention.
  
  **Identified Flight Risk Employees are:**    
  •	bobette.riner@ipgdirect.com  
  •	don.baughman@enron.com  
  •	eric.bass@enron.com  
  •	john.arnold@enron.com  
  •	johnny.palmer@enron.com  
  •	kayne.coulter@enron.com  
  •	lydia.delgado@enron.com  
  •	patti.thompson@enron.com  
  •	rhonda.denton@enron.com  
  •	sally.beck@enron.com

Predictive Modeling :  
- Used features such as message frequency, message length stats, word count, and positive message counts.   
- Developed a linear regression model to predict monthly sentiment scores.  
- Evaluated model performance using R² and RMSE, demonstrating strong predictive capability.
- Visualized the residual plots, Actual Vs Predicted Scatter Plot etc.
  
### Key Insights & Recommendations:  
• More messages have a negative tone over positive, which might infer about how people are communicating at work.  
• There are employees who usually send either positive or negative messages. This can help managers understand who might need extra support.  
• Employees who send negative messages frequently in a period of short span could be at risk of leaving the company or feeling unhappy. It’s important to check upon them.  
• This model can fairly predict the emotion/sentiment of the messages, based on frequency and lengthof the messages.  
• It’s a good practice to keep tracking the sentiments of the employees so that help can be extended to those stressed or unhappy with necessary training or support. This can improve the workplace culture. 

### Summary  
This project offers a comprehensive approach to understanding and forecasting employee sentiment through email communication analysis. The tools and findings can guide organizational decision-making around employee engagement and retention.
