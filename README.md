# EDA_MUSIC_FM1213

# Music Streaming Listener Preferences – Exploratory Data Analysis (EDA)

## Project Overview
This project focuses on performing Exploratory Data Analysis (EDA) on a Music Streaming dataset to understand user listening patterns, genre preferences, demographic behavior, and engagement levels. The analysis includes data cleaning, descriptive statistics, outlier detection, data transformation, and visualization for deriving meaningful insights that can support personalized recommendation systems and marketing strategies.

---

## Dataset Information
Dataset Name: music_streaming_preferences.csv  
Total Records: ~1,000+ listener entries  

### Features Used:
| Feature Name | Description |
|-------------|-------------|
| Listener_ID | Unique identifier for each listener |
| Age | Age of listener |
| Gender | Male / Female / Other |
| Country | Country of the listener |
| Favorite_Genre | Music genre most listened to |
| Daily_Listen_Time | Average listening time per day (minutes) |
| Subscription_Type | Free / Premium |
| Platform | Streaming platform used (Spotify, Apple Music, etc.) |

---

## Project Structure
```
├── music_streaming_preferences.csv # Dataset

├── EDA_Music_Listening.ipynb # Notebook

└── README.md # Documentation file
```

---

## Analysis Workflow

### 1. Dataset Overview
- Checked dataset shape, info, data types
- Reviewed unique values per feature
- Displayed summary statistics for numeric columns

### 2. Data Quality Checks
- Minor missing values detected and handled
- Removed duplicate records
- Standardized inconsistent text formatting (e.g., genre labels)

### 3. Data Cleaning
- Numerical missing values filled using median
- Categorical missing values filled using mode
- Listener_ID dropped for modeling purposes
- Final dataset has no null or duplicate values

### 4. Descriptive Statistics (Key Observations)
- Average listener age: ~27 years
- Average daily listening time: ~145 minutes
- Most popular genre: Pop
- Most commonly used platform: Spotify

Gender Distribution:
- Male: ~51%
- Female: ~48%
- Other: ~1%

### 5. Data Transformation and Feature Engineering
- StandardScaler used for scaling continuous variables
- Label Encoding applied to categorical fields for machine learning readiness
- New features created:
  - AgeGroup (Teen, Adult, Senior)
  - EngagementScore (based on Age + Daily Listening Time + Subscription Type)

### 6. Outlier Detection
Methods applied:
- IQR Method: Outliers in Daily Listening Time detected and capped
- Z-Score Method: ~2.8% extreme listeners identified but kept as meaningful behavior records

### 7. Data Visualization
Visualizations generated:
- Histogram (Age, Listening Time)
- Bar Chart (Genre Popularity)
- Boxplot (Engagement Patterns)
- Heatmap (Correlation among numerical features)
- Countplot (Subscription vs Genre Preference)

---

## Key Insights

### Demographics
- Majority of listeners are between 18–35 years old.
- Balanced distribution across genders.

### Music Preferences
- Pop, Hip-Hop, and EDM are the most preferred genres.
- Older listeners tend to listen more to Classic, Folk, and Jazz.

### Engagement Patterns
- Premium users listen significantly longer daily compared to free users.
- Spotify has the highest usage share among platforms.

---

## Technologies Used
- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- scipy
- scikit-learn

---

## How to Run
Install necessary dependencies:


Run the notebook:
1. Open Google Colab: https://colab.research.google.com
2. Upload `EDA_Music_Listening.ipynb`
3. Run all cells in sequence

---

## Author
Name: Shivprasad Kuber Gajare 

Roll No: FM1215

Course: MSc Computer Science  

Year: 2025  

---

## License
This project is for educational and academic purposes only.

---

## Acknowledgments
This project was created as part of the MSc Computer Science Data Analytics Module. The dataset used is a simulated open-source dataset intended for research and learning.

