# Employee_Sentiment_Analysis
This project is to analyze an unlabeled dataset of employee messages to assess sentiment and engagement trends. Using natural language processing and statistical analysis, the goal is to:
•	**Sentiment Labeling**: Automatically label each message as Positive, Negative, or Neutral.
•	**Exploratory Data Analysis (EDA)**: Analyze and visualize the data to understand its structure and underlying trends.
•	**Employee Score Calculation**: Compute a monthly sentiment score for each employee based on their messages.
•	**Employee Ranking**: Identify and rank employees by their sentiment scores.
•	**Flight Risk Identification**: A Flight risk is any employee who has sent 4 or more negative mails in a given month.
•	**Predictive Modeling**: Develop a linear regression model to further analyze sentiment trends.

The top three positive and negative employees for **Feb 2011** are:
  **Top 3 Positive Employees:**
                  employee  sentiment_score
   lydia.delgado@enron.com                2
       eric.bass@enron.com                1
  patti.thompson@enron.com                1
  
  **Top 3 Negative Employees:**
                     employee  sentiment_score
      kayne.coulter@enron.com               -4
         sally.beck@enron.com               -4
  bobette.riner@ipgdirect.com               -3

**Flight Risk Employees:**
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

**Key Insights & Recommendations:**
• More messages have a negative tone over positive, which might infer about how people are communicating at work.
• There are employees who usually send either positive or negative messages. This can help managers understand who might need extra support.
• Employees who send negative messages frequently in a period of short span could be at risk of leaving the company or feeling unhappy. It’s important to check upon them.
• This model can fairly predict the emotion/sentiment of the messages, based on frequency and lengthof the messages.
• It’s a good practice to keep tracking the sentiments of the employees so that help can be extended to those stressed or unhappy with necessary training or support. This can improve the workplace culture.
