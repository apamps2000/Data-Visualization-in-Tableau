# Data-Visualization-in-Tableau
Visualising and analysing data from X  (Twitter data OR tweets) in Tableau
###NEVER AGAIN DATA WRANGLING 1
###Combining all the #NeverAgain.csv files into one single file using concat function
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

df1 = pd.read_csv ("#NeverAgain1.csv")
df3 = pd.read_csv ("#NeverAgain3.csv")
df4 = pd.read_csv ("#NeverAgain4.csv")
df5 = pd.read_csv ("#NeverAgain5.csv")
df6 = pd.read_csv ("#NeverAgain6.csv")
df7 = pd.read_csv ("#NeverAgain7.csv")
df8 = pd.read_csv ("#NeverAgain8.csv")
df9 = pd.read_csv ("#NeverAgain9.csv")
df10 = pd.read_csv ("#NeverAgain10.csv")
df11 = pd.read_csv ("#NeverAgain11.csv")
df12 = pd.read_csv ("#NeverAgain12.csv")
df13 = pd.read_csv ("#NeverAgain13.csv")

df_neveragain = pd.concat([df1, df3, df4, df5, df6, df7, df8, df9, df10, df11, df12, df13])

df_neveragain.to_csv('df_neveragain1.csv') #save as a new single file

##check for the summary of the saved df_neveragain.csv file
df_neveragain.shape 
df_neveragain.head(5)
df_neveragain.tail(5)

df_neveragain = pd.read_csv ("df_neveragain1.csv")

## the number of null or NA values in each column
df_neveragain.isnull().sum() 


##Thus, we have 18 features and 274,729 instances in our dataset. The “isnull” function was called to determine the number of row data ##that are missing from the dataset:

id_str                            6
from_user                         6
text                             23
created_at                       23
time                             40
geo_coordinates              274656
user_lang                        23
in_reply_to_user_id_str      257547
in_reply_to_screen_name      257530
from_user_id_str                 23
in_reply_to_status_id_str    260108
source                           23
profile_image_url                31
user_followers_count            790
user_friends_count              524
user_location                 84890
status_url                       40
entities_str                     40
dtype: int64
