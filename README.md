# Data-Cleaning-FIFA-2021
## Introduction
This is a rundown of the cleaning process for FIFA '21 dataset. This data set was provided as part of a challenge #Datacleaningchallenge launched on twitter by data ethusiasts to test the prowess of newbies , intermediate and pro Data analyst alike for a large messy dataset.

The data set contains 18,979 rows and 77 columns of football players statistics and demography in 2021 The dataset is publicly available on kaggle which contains data scrapped from sofifa The datafile also includes a Data dictionary as well as a column named player url which contains a link to the player profile on sofifa to give the analyst furher insight and full details of the player in view in case of missing information.

My prefered tool for this Data cleaning challenge based on proficiency is Power Query as available on Power BI

## Data Cleaning process
![image](https://user-images.githubusercontent.com/124640415/228377986-ab40fab7-2cc5-4826-a431-ad90f7536d74.png)


To ensure data quality , the following approach was used

After loading the data , whitespaces were removed by unticking the button from the viewtab.

#                                                           White Spaces
  ![image](https://user-images.githubusercontent.com/124640415/228378535-7018372d-6e2d-4676-bff7-e22e1fd09c4c.png) ![image](https://user-images.githubusercontent.com/124640415/228378552-7e1a3b35-7d18-4a3c-8bfa-3e251b22541e.png)
  
### Data Auditing: 
To ensure data quality, during the auditing stage of understanding the data and identifying any inconsistencies, missing values, or errors that need to be addressed, the following columns were marked for cleaning ; Name, Longname, OVA , POT , Club , Contract , Positions , Height , Weight , Best position , Joined , Loan End date , Value, wage , release clause , W/F , SM , IR , and Hits.
### Data Cleaning and Transformation:

The previously identified columns were worked on , in an orderly manner
###                                                                      Names
The Name and Longname column were checked for errors and correction was made to the one name(S.Radu) which had a symbol in his name instead of the appropriate initial.
### Percentages
As advised by the Data Dictionary , the columns OVA and POT were reformatted to reflect percentages. Column from example was used to add % to the end of the row figures ,then the data type was changed to percentage.

![image](https://user-images.githubusercontent.com/124640415/228381751-9e59e573-25d0-496d-ad06-f9958561b816.png) ![image](https://user-images.githubusercontent.com/124640415/228381779-ac5da5a5-cca2-481d-a3ef-aa655be989dc.png)

