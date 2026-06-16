# Employee Sentiment Analysis


## 🛠️ Local Setup & Installation

To run this project on your local machine, follow these steps:

**1. Clone the Repository**
Ensure you have the `test.csv` dataset in the root directory of this project.

**2. Create a Virtual Environment**
It is recommended to use a virtual environment to manage dependencies.

# On Windows
`python -m venv venv
venv\Scripts\activate`

# On Mac/Linux
`python3 -m venv venv
source venv/bin/activate`

# **3. Install Dependencies**
Install the required Python libraries using pip:


```pip install pandas numpy matplotlib textblob scikit-learn jupyter```

# **4. Run the Code**
Launch Jupyter Notebook in your terminal and open the .ipynb file to view the analysis and interactive charts

## Project Overview
This project analyzes an unlabeled dataset of employee communications to derive insights regarding sentiment and engagement. Using Natural Language Processing (TextBlob) and statistical analysis, the project evaluates monthly sentiment scores, ranks employees, identifies potential flight risks, and utilizes a linear regression model to predict sentiment trends.

## Key Findings

### 🏆 Top Employee Rankings (Cumulative)
**Top 3 Positive Employees:**
1. kayne.coulter@enron.com
2. lydia.delgado@enron.com
3. eric.bass@enron.com

**Top 3 Negative Employees:**
1. bobette.riner@ipgdirect.com
2. rhonda.denton@enron.com
3. johnny.palmer@enron.com

### ⚠️ Flight Risk Identification
A "flight risk" is defined as any employee sending 4 or more negative emails within a rolling 30-day period. The following 6 employees have been flagged based on this criteria:
* bobette.riner@ipgdirect.com (22 total negative messages)
* don.baughman@enron.com (15 total negative messages)
* john.arnold@enron.com (11 total negative messages)
* johnny.palmer@enron.com (18 total negative messages)
* kayne.coulter@enron.com (19 total negative messages)
* sally.beck@enron.com (23 total negative messages)

## 💡 Key Insights & Recommendations

### Insights from Predictive Modeling (R² = 0.829)
1. **Communication Volume Predicts Positivity:** Message frequency positively correlates with sentiment scores. Highly communicative employees generally exhibit a more positive and engaged tone.
2. **Dominant Sentiment:** Overall, positive sentiment dominates the dataset across all months, with negative messages making up a much smaller fraction of the volume.
3. **Consistency of Sentiment:** The percentage of positive messages (`pct_positive`) is the strongest overall driver of high monthly scores, indicating that consistently positive individuals tend to stay positive over time.

### Recommendations for Management
* **Engage with Flight Risks Immediately:** HR or management should conduct stay interviews or check-ins with the 6 flagged flight risks. Note that even overall positive employees (like `kayne.coulter@enron.com`, who is a top positive scorer) can experience acute periods of frustration that trigger the flight risk threshold.
* **Monitor Communication Drop-offs:** Since message frequency is positively correlated with engagement, sudden drops in a normally communicative employee's email volume could serve as an early warning sign of disengagement.
* **Leverage Top Performers:** Employees like `lydia.delgado@enron.com` and `eric.bass@enron.com` exhibit sustained positive sentiment. Management could leverage these individuals as cultural ambassadors or peer mentors.
