


# BELLABEAT DATA ANALYTICS CASE STUDY USING PYTHON







## Overview


Welcome to my Bellabeat Data Analytics Case Study! 🚀 In this project, I've taken on the role of a junior data analyst, collaborating with Bellabeat—a leading manufacturer of health-focused products for women. The journey involved addressing key business questions, and I've meticulously followed the data analysis process:

- **Ask:** Formulated relevant questions.
- **Prepare:** Cleaned and prepared the dataset.
- **Process:** Processed and organized data.
- **Analyze:** Conducted in-depth analysis.
- **Share:** Shared insights with the team.
- **Act:** Formulated actionable strategies.








## Scenario


Urška Sršen, cofounder and Chief Creative Officer of Bellabeat, believes that analyzing smart device fitness data could help unlock new growth opportunities for the company. I have been asked to focus on one of Bellabeat’s products and analyze smart device data to gain insight into how consumers are using their smart devices. The insights I discover will then help guide marketing strategy for the company.







## Characters


  **Urška Sršen**: Bellabeat’s cofounder and Chief Creative Officer 

  
  
  **Sando Mur**: Mathematician and Bellabeat’s cofounder; key member of the Bellabeat executive team 


  
  **Bellabeat marketing analytics team**: A team of data analysts responsible for collecting, analyzing, and reporting data that helps guide Bellabeat’s marketing strategy. I have joined this team six months ago and have been busy learning about Bellabeat’’s mission and business goals — as well as how me, as a junior data analyst, can help Bellabeat achieve them. 




  
## products 


  **Bellabeat app**: The Bellabeat app provides users with health data related to their activity, sleep, stress, menstrual cycle, and mindfulness habits. This data can help users better understand their current habits and make healthy decisions. The Bellabeat app connects to their line of smart wellness products. 

  
  **Leaf**: Bellabeat’s classic wellness tracker can be worn as a bracelet, necklace, or clip. The Leaf tracker connects to the Bellabeat app to track activity, sleep, and stress. 

  
  **Time**: This wellness watch combines the timeless look of a classic timepiece with smart technology to track user activity, sleep, and stress. The Time watch connects to the Bellabeat app to provide you with insights into your daily wellness. 

  
  **Spring**: This is a water bottle that tracks daily water intake using smart technology to ensure that you are appropriately hydrated throughout the day. The Spring bottle connects to the Bellabeat app to track your hydration levels. 

  
  **Bellabeat membership**: Bellabeat also offers a subscription-based membership program for users. Membership gives users 24/7 access to fully personalized guidance on nutrition, activity, sleep, health and beauty, and mindfulness based on their lifestyle and goals. 






  


## About the company 


Urška Sršen and Sando Mur founded Bellabeat, a high-tech company that manufactures health-focused smart products. Sršen used her background as an artist to develop beautifully designed technology that informs and inspires women around the world. Collecting data on activity, sleep, stress, and reproductive health has allowed Bellabeat to empower women with knowledge about their own health and habits. Since it was founded in 2013, Bellabeat has grown rapidly and quickly positioned itself as a tech-driven wellness company for women. 







## First Phase: ASK Phase

### Business Task

Identify trends in how consumers use non-Bellabeat smart devices to apply insights into Bellabeat’s marketing strategy.

### Stakeholders

  **Sršen** — Bellabeat’s cofounder and Chief Creative Officer

  
  **Sando Mur** — Bellabeat’s cofounder; key member of the Bellabeat executive team

  
  **Bellabeat marketing analytics team**




## Second Phase: PREPARE Phase
  ### Dataset used:
 
   The data source used for our case study is FitBit Fitness Tracker Data. This dataset is stored in Kaggle and was made available through Mobius.

 ### Accessibility and privacy of data:

Verifying the metadata of our dataset we can confirm it is open-source. The owner has dedicated the work to the public domain by waiving all of his or her rights to the work worldwide under copyright law, including all related and neighboring rights, to the extent allowed by law. You can copy, modify, distribute and perform the work, even for commercial purposes, all without asking permission

### About Dataset


This dataset generated by respondents to a distributed survey via Amazon Mechanical Turk between 03.12.2016-05.12.2016. Thirty eligible Fitbit users consented to the submission of personal tracker data, including minute-level output for physical activity, heart rate, and sleep monitoring. Individual reports can be parsed by export session ID (column A) or timestamp (column B). Variation between output represents use of different types of Fitbit trackers and individual tracking behaviors / preferences.



## Third Phase: PROCESS Phase


I choose to use python for my analysis considering the data sets are large and python makes it easier to visualize the data .



 **1. importing datasets**

```python
dailyActivity_merged=pd.read_csv(r"F:\dataanalytics project\Fitabase Data 4.12.16-5.12.16\dailyActivity_merged.csv")
dailyCalories_merged=pd.read_csv(r"F:\dataanalytics project\Fitabase Data 4.12.16-5.12.16\dailyCalories_merged.csv")
dailyIntensities_merged=pd.read_csv(r"F:\dataanalytics project\Fitabase Data 4.12.16-5.12.16\dailyIntensities_merged.csv")
dailySteps_merged=pd.read_csv(r"F:\dataanalytics project\Fitabase Data 4.12.16-5.12.16\dailySteps_merged.csv")
heartrate_seconds_merged=pd.read_csv(r"F:\dataanalytics project\Fitabase Data 4.12.16-5.12.16\heartrate_seconds_merged.csv")
hourlyCalories_merged=pd.read_csv(r"F:\dataanalytics project\Fitabase Data 4.12.16-5.12.16\hourlyCalories_merged.csv")
hourlyIntensities_merged=pd.read_csv(r"F:\dataanalytics project\Fitabase Data 4.12.16-5.12.16\hourlyIntensities_merged.csv")
hourlySteps_merged=pd.read_csv(r"F:\dataanalytics project\Fitabase Data 4.12.16-5.12.16\hourlySteps_merged.csv")
minuteCaloriesNarrow_merged=pd.read_csv(r"F:\dataanalytics project\Fitabase Data 4.12.16-5.12.16\minuteCaloriesNarrow_merged.csv")
minuteCaloriesWide_merged=pd.read_csv(r"F:\dataanalytics project\Fitabase Data 4.12.16-5.12.16\minuteCaloriesWide_merged.csv")
minuteIntensitiesNarrow_merged=pd.read_csv(r"F:\dataanalytics project\Fitabase Data 4.12.16-5.12.16\minuteIntensitiesNarrow_merged.csv")
minuteIntensitiesWide_merged=pd.read_csv(r"F:\dataanalytics project\Fitabase Data 4.12.16-5.12.16\minuteIntensitiesWide_merged.csv")
minuteMETsNarrow_merged=pd.read_csv(r"F:\dataanalytics project\Fitabase Data 4.12.16-5.12.16\minuteMETsNarrow_merged.csv")
minuteSleep_merged=pd.read_csv(r"F:\dataanalytics project\Fitabase Data 4.12.16-5.12.16\minuteSleep_merged.csv")
minuteStepsNarrow_merged=pd.read_csv(r"F:\dataanalytics project\Fitabase Data 4.12.16-5.12.16\minuteStepsNarrow_merged.csv")
minuteStepsWide_merged=pd.read_csv(r"F:\dataanalytics project\Fitabase Data 4.12.16-5.12.16\minuteStepsWide_merged.csv")
sleepDay_merged=pd.read_csv(r"F:\dataanalytics project\Fitabase Data 4.12.16-5.12.16\sleepDay_merged.csv")
weightLogInfo_merged=pd.read_csv(r"F:\dataanalytics project\Fitabase Data 4.12.16-5.12.16\weightLogInfo_merged.csv")
```

**2.Understanding Data Structures and cleaning**


```python
dataframes = [dailyActivity_merged, dailyCalories_merged, dailyIntensities_merged,
               dailySteps_merged, heartrate_seconds_merged, hourlyCalories_merged,
               hourlyIntensities_merged, hourlySteps_merged, minuteCaloriesNarrow_merged,
               minuteCaloriesWide_merged, minuteIntensitiesNarrow_merged, minuteIntensitiesWide_merged,
               minuteMETsNarrow_merged, minuteSleep_merged, minuteStepsNarrow_merged,
               minuteStepsWide_merged, sleepDay_merged, weightLogInfo_merged]

for df in dataframes:
    print(df.info())
    print('\n' + '='*50 + '\n')  # Separating each DataFrame's info for better readability


for df in dataframes:
    df.drop_duplicates(inplace=True)
    df.dropna(inplace=True)

dataframes_to_verify = [dailyCalories_merged, dailyIntensities_merged, dailySteps_merged,
                        heartrate_seconds_merged, hourlyCalories_merged, hourlyIntensities_merged,
                        hourlySteps_merged, minuteCaloriesNarrow_merged, minuteCaloriesWide_merged,
                        minuteIntensitiesNarrow_merged, minuteIntensitiesWide_merged, minuteMETsNarrow_merged,
                        minuteSleep_merged, minuteStepsNarrow_merged, minuteStepsWide_merged, sleepDay_merged,
                        weightLogInfo_merged]

for df in dataframes_to_verify:
    common_columns = set(dailyActivity_merged.columns) & set(df.columns)
    matching_ids = dailyActivity_merged['Id'].equals(df['Id'])
    
    if common_columns and matching_ids:
        print(f"Dataframe: {df}")
        print(f"Common Columns: {common_columns}")
        print(f"Matching IDs: {matching_ids}")

        common_columns_values = dailyActivity_merged[common_columns].equals(df[common_columns])
        print(f"Matching Data Values for Common Columns: {common_columns_values}")

        print(f"Sample rows from dailyActivity_merged:")
        print(dailyActivity_merged[common_columns].head())

        print(f"Sample rows from other_dataframe:")
        print(df[common_columns].head())
        print("="*50)


```


**note:**


**1.** Here date and time associated columns are also inconsistent . Actually we need to make them all consistent , but since the dataset is large it takes significant amount of time . so i will convert them when i am actually using those dataframes in the analysis . That way we donot need to parse all the dataframes and convert those values instead we modify some dataframes only when we need them 


**2.** The reason why we have compared Id and other columns of dailyActivity_Merged with others is some of the other Data frames are actually subsets of this dataframe . so we donot need to analyze all of them . so to check what other dataframes are subsets of this one we compared the ids and other columns .

## Analyzing the data 

##### 1.summarizing daily data


```python




        
# Selecting specific columns
selected_columns = ['TotalSteps', 'TotalDistance', 'SedentaryMinutes', 'Calories']

# Creating a subset of the dataframe with selected columns
subset_daily_activity = dailyActivity_merged[selected_columns]

# Using the describe method for summary statistics
summary_statistics = subset_daily_activity.describe()

# Displaying the summary statistics
print(summary_statistics)
print(sleepDay_merged.describe())
print(weightLogInfo_merged.describe())
print(heartrate_seconds_merged.describe())

```


output :  
```
 ==============
         TotalSteps  TotalDistance  SedentaryMinutes     Calories
count    940.000000     940.000000        940.000000   940.000000
mean    7637.910638       5.489702        991.210638  2303.609574
std     5087.150742       3.924606        301.267437   718.166862
min        0.000000       0.000000          0.000000     0.000000
25%     3789.750000       2.620000        729.750000  1828.500000
50%     7405.500000       5.245000       1057.500000  2134.000000
75%    10727.000000       7.712500       1229.500000  2793.250000
max    36019.000000      28.030001       1440.000000  4900.000000
                 Id  TotalSleepRecords  TotalMinutesAsleep  TotalTimeInBed
count  4.100000e+02         410.000000          410.000000      410.000000
mean   4.994963e+09           1.119512          419.173171      458.482927
std    2.060863e+09           0.346636          118.635918      127.455140
min    1.503960e+09           1.000000           58.000000       61.000000
25%    3.977334e+09           1.000000          361.000000      403.750000
50%    4.702922e+09           1.000000          432.500000      463.000000
75%    6.962181e+09           1.000000          490.000000      526.000000
max    8.792010e+09           3.000000          796.000000      961.000000
                 Id   WeightKg  WeightPounds       Fat        BMI         LogId
count  2.000000e+00   2.000000      2.000000   2.00000   2.000000  2.000000e+00
mean   2.911832e+09  62.500000    137.788914  23.50000  25.050000  1.461586e+12
std    1.991031e+09  14.000716     30.866296   2.12132   3.394113  9.164104e+08
min    1.503960e+09  52.599998    115.963147  22.00000  22.650000  1.460938e+12
25%    2.207896e+09  57.549999    126.876030  22.75000  23.850000  1.461262e+12
50%    2.911832e+09  62.500000    137.788914  23.50000  25.050000  1.461586e+12
75%    3.615768e+09  67.450001    148.701798  24.25000  26.250000  1.461910e+12
max    4.319704e+09  72.400002    159.614681  25.00000  27.450001  1.462234e+12
                 Id         Value
count  2.483658e+06  2.483658e+06
mean   5.513765e+09  7.732842e+01
std    1.950224e+09  1.940450e+01
min    2.022484e+09  3.600000e+01
25%    4.388162e+09  6.300000e+01
50%    5.553957e+09  7.300000e+01
75%    6.962181e+09  8.800000e+01
max    8.877689e+09  2.030000e+02


```
**observations**


**1.**
The average total steps per day is 7637, close to the daily recommended amount of 7500 steps.

**2.**
Participants spend an average of 991 sedentary minutes per day (~17 hours).

**3.**
The average calorie burn is 2303 per day, with a minimum of 0 and a maximum of 4900.

**4.**
Participants, on average, have 1.12 sleep records and spend approximately 419 minutes asleep.

**5.**
Heart rate data shows an average value of 77.33.   which is good 

**6.**
Average weight of 62.5 kg.

##### 2. steps taken vs calorie burned 
From the above observations we can see that avg steps taken = 7637 and calorie burned = 2303 per day indicating there could be a positive correlation between them 

```

#2.verifying correlation between steps and calories burned



selected_columns = ['TotalSteps', 'Calories']
subset_dataframe = dailyActivity_merged[selected_columns].dropna()  # Drop rows with missing values
sns.regplot(x='TotalSteps', y='Calories', data=subset_dataframe)

# Adding labels and title
plt.title("Total Steps vs. Calories")
plt.xlabel("Total Steps")
plt.ylabel("Calories")
plt.legend()

# Display the plot
plt.show()

```
output : 



![stepsvscaloriescorr](https://github.com/Kedhar193/BellaBeat-DataAnalytics-casestudy-python-/assets/115712936/b77a704b-4429-4104-b84a-4447d76da4d0)


this indicates a positive correlation 


##### 3.Analyzing number of steps per weekday 

```python



dailyActivity_merged['ActivityDate'] = pd.to_datetime(dailyActivity_merged['ActivityDate'])

# Extracting day of the week and setting the order
dailyActivity_merged['weekday'] = dailyActivity_merged['ActivityDate'].dt.strftime('%A')
weekday_order = ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday", "Sunday"]
dailyActivity_merged['weekday'] = pd.Categorical(dailyActivity_merged['weekday'], categories=weekday_order, ordered=True)

# Grouping by weekday and calculating mean steps
weekday_steps = dailyActivity_merged.groupby('weekday')['TotalSteps'].mean().reset_index()

# Plotting the data
plt.figure(figsize=(10, 6))
sns.barplot(x='weekday', y='TotalSteps', data=weekday_steps, palette="viridis")
plt.axhline(y=7500, color='red', linestyle='--', label='Threshold (7500 steps)')
plt.title('Daily Steps per Weekday')
plt.xlabel('Weekday')
plt.ylabel('Daily Steps')
plt.xticks(rotation=45, ha='right')
plt.legend()
plt.show()


```

output : 
                                                             
![dailystepsperweekend](https://github.com/Kedhar193/BellaBeat-DataAnalytics-casestudy-python-/assets/115712936/59c38137-f1a3-42b5-aa6b-5bfe76ac96b8)



##### 4.analyzing sleeping hours per weekday


```python
sleepDay_merged['SleepDay'] = pd.to_datetime(sleepDay_merged['SleepDay'])

# Extracting day of the week and setting the order
sleepDay_merged['weekday'] = sleepDay_merged['SleepDay'].dt.strftime('%A')
weekday_order = ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday", "Sunday"]
sleepDay_merged['weekday'] = pd.Categorical(sleepDay_merged['weekday'], categories=weekday_order, ordered=True)

# Grouping by weekday and calculating mean sleep duration
weekday_sleep = sleepDay_merged.groupby('weekday')['TotalMinutesAsleep'].mean().reset_index()

# Plotting the data
plt.figure(figsize=(10, 6))
sns.barplot(x='weekday', y='TotalMinutesAsleep', data=weekday_sleep, palette="pastel")
plt.axhline(y=480, color='red', linestyle='--', label='Threshold (480 minutes)')
plt.title('Minutes Asleep per Weekday')
plt.xlabel('Weekday')
plt.ylabel('Minutes Asleep')
plt.xticks(rotation=45, ha='right')
plt.legend()
plt.show()

```

output : 



![minutesasleepperweekday](https://github.com/Kedhar193/BellaBeat-DataAnalytics-casestudy-python-/assets/115712936/41fd60fb-e3b6-47d6-bbda-779abc35258e)

##### 5.analyzing hourly intensities


```
hourlyIntensities_merged['ActivityHour'] = pd.to_datetime(hourlyIntensities_merged['ActivityHour'], format='%m/%d/%Y %I:%M:%S %p')

# Splitting into date and time
hourlyIntensities_merged['date'] = hourlyIntensities_merged['ActivityHour'].dt.date
hourlyIntensities_merged['time'] = hourlyIntensities_merged['ActivityHour'].dt.time

# Grouping by time and calculating mean total intensity
hourly_intensities = hourlyIntensities_merged.groupby('time').agg(mean_total_int=('TotalIntensity', 'mean')).reset_index()

# Plotting the data
plt.figure(figsize=(12, 6))
sns.barplot(x='time', y='mean_total_int', data=hourly_intensities, color='purple')
plt.title('Average Total Intensity vs. Time')
plt.xlabel('Time')
plt.ylabel('Mean Total Intensity')
plt.xticks(rotation=90)
plt.show()

```


output : 


![hourlyintensities](https://github.com/Kedhar193/BellaBeat-DataAnalytics-casestudy-python-/assets/115712936/0ec4d997-6b58-46cb-8811-320ce20d7306)



##### 6.hourly steps through out the day 

```

if not hourlySteps_merged['ActivityHour'].empty:
    # Convert 'ActivityHour' to datetime format
    hourlySteps_merged['ActivityHour'] = pd.to_datetime(hourlySteps_merged['ActivityHour'], format='%m/%d/%Y %I:%M:%S %p')

    # Extracting date and time
    hourlySteps_merged['date'] = hourlySteps_merged['ActivityHour'].dt.strftime('%Y-%m-%d')
    hourlySteps_merged['time'] = hourlySteps_merged['ActivityHour'].dt.strftime('%H:%M:%S')

    # Grouping by time and calculating mean steps
    hourly_steps_grouped = hourlySteps_merged.groupby('time')['StepTotal'].mean().reset_index()

    # Plotting the data
    plt.figure(figsize=(12, 6))
    sns.barplot(x='time', y='StepTotal', data=hourly_steps_grouped, palette='RdYlGn_r')
    plt.title('Hourly Steps Throughout the Day')
    plt.xlabel('Time')
    plt.ylabel('Average Steps')
    plt.xticks(rotation=90)
    plt.show()
else:
    print("Error: 'ActivityHour' column is empty.")

```

output: 



![hourlystepsperday](https://github.com/Kedhar193/BellaBeat-DataAnalytics-casestudy-python-/assets/115712936/2b03c486-2daf-4321-93d7-5628a70263ce)




### overall observations 


**1.** Users donot get recommended 8 hrs sleep 


**2.** Heart rate and weights are in recommended range . 


**3.** Users are taking less number of steps and excercise on weekends .


**4.** Users are most active around 7-9 p.m .


**5.** Users are taking more number steps at this time too 7-9 p.m . This probably indicates that most of the active users are working class women and they do excercise after they are done with work at office .


### Suggestions (ACT phase)


**1.** It is proven that users are not getting recommended sleep . so product could give reminders and recommendations to get the recommended sleep .


**2.** Product could focus on motivating the users to work on weekends too since we can see that users are not working out enough on weekends as they do in other weekdays . 


**3.** It seems that most of the active users are working class women as per the hourly intensities data . So target audience for marketing will be working class women . So company needs to advertise on platforms where most working women engage or use . 




