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

![image](https://user-images.githubusercontent.com/124640415/228381751-9e59e573-25d0-496d-ad06-f9958561b816.png)   ![image](https://user-images.githubusercontent.com/124640415/228381779-ac5da5a5-cca2-481d-a3ef-aa655be989dc.png)

### Contract
This column contained inconsistent data type and format, hence this was reguarized using a combination of 3 columns , namely; Contract Start , Contract End , and Agreement and Contract duration. The filter view reveals players whose contract column specify they are on loan tallies with the year on the Loan end date column. while players whose contract indicate free transfer, tally with those clubless players with no wage or value or release clause . These were replaced with null as there is no specified loan end date since they're not on contract and have no recorded wages. 

![image](https://user-images.githubusercontent.com/124640415/228384716-f1fe7622-0696-4d11-9c9a-71f3a6478f8a.png) ![image](https://user-images.githubusercontent.com/124640415/228384744-039f67f0-4aa1-4b2f-ba4e-6fc9a42a8dfe.png)

### Height
The majority of values in this column displays height in centimeter. While a few others uses feet and inches for example 6'2" . Initial thought was just to split by the delimiter ' " and multiply by 30.48 which is the standard conversion of feet to cm . However a quick google search reveals this formula only accounts for feet and not inches hence to resolve this after splitting, the feet column was multplied by 30.48 and the inches column by 2.54. then both columns were merged using addition and rounded up to the nearest whole number. then the cm text value was dropped from the other rows to successfully change the data type to numeric.

![image](https://user-images.githubusercontent.com/124640415/228385569-7fb2c559-b4e6-4731-bd3d-ce4735ad3dfa.png) ![image](https://user-images.githubusercontent.com/124640415/228385652-bf2b14d8-7244-4d86-b70f-454d3b5fcb32.png)

##  Weight
About 60% of the data values in this column contains weight in lbs (pounds) and the other 40% in Kg . After splitting the column using Digits to non-digits function, A decision was made to unify all data values as KG and the standard conversion rate of 0.45392 was used to multiply the weight in Lbs value to give the equivalent in KG and rounded up.

![image](https://user-images.githubusercontent.com/124640415/228388917-50d9bc34-9509-489c-9e22-888401d5b021.png) ![WEIGHT](https://user-images.githubusercontent.com/124640415/228388889-22b51e3d-455e-4f2c-81e2-9b91d3bf1c6c.JPG)


