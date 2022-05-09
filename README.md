# Bike-share-capstone-project
## Introduction
this Project was about a bike share compan based in chicago.
In order to answer the key business questions,I followed the steps of the data analysis process: ask, prepare, process, analyze,
share, and act. 
I was tasked to understand how casual riders and annual members use Cyclistic bikes differently. From these insights,
I would have to design a new marketing strategy to convert casual riders into annual members
## The Ask Phase 
After asking the Project owners on the main aim of the task it was concludent into 3 main objectives 
1. How do annual members and casual riders use Cyclistic bikes differently?
2. Why would casual riders buy Cyclistic annual memberships?
3. How can Cyclistic use digital media to influence casual riders to become members?

## The Prepare Phase
I used  Cyclistic’s historical trip data to analyze and identify trends. Downloaded the previous Quateer of Cyclistic trip data
here. (Note: The datasets have a different name because Cyclistic is a fictional company. For the purposes of this case study,
the datasets are appropriate and enabled me  to answer the business questions. The data has been made available by
Motivate International Inc. under this license.(https://ride.divvybikes.com/data-license-agreement) 
This is public data that I  used to explore how different customer types use Cyclistic bikes. 

## The Process Phase
Using the case road map i was able to clean the data using R as my cleaning tool.
I ensured removal of duplicate ,wrangled data and also went further to compare colnames funtion  to be sure all the data had same column names.
I discovered the divy trip data for 2nd quater of 2019 had different name i had to use the renme function to make them aligned .
I converted some column names to fit that of 2020 quater,since the column name changed from 2020,this helped me in binding the data to one frame.
## FIXING OF SETBACKS IN DATA
 (1) In the "member_casual" column, there are two names for members ("member" and "Subscriber") and two names for casual riders ("Customer" and "casual"). We will need to consolidate that from four to two labels.
 (2) The data can only be aggregated at the ride-level, which is too granular. We will want to add some additional columns of data -- such as day, month, year -- that provide additional opportunities to aggregate the data.
 (3) We will want to add a calculated field for length of ride since the 2020Q1 data did not have the "tripduration" column. We will add "ride_length" to the entire dataframe for consistency.
 (4) There are some rides where tripduration shows up as negative, including several hundred rides where Divvy took bikes out of circulation for Quality Control reasons. We will want to delete these rides.
 
Added new columns to the list ( date, month, day, and year of each ride)
#Descriptive analysis Phase
Here i added trip length to the combined trip data frame so i could get the mean median ,minimun ride as well as maximum ride 
I used this in comparing the ride data between members and casual members .
Had to rearrange the days of the week in chronological order to determnine that of casual riders  and members 
#Share Phase 
I used ggplot2 Package in visualizing the number of rides by riders type(members or casual)
also i visualised average duration of the bike used by the riders by weekdays .
# The Act Phase
After the analysis i was able to share some insight that i dicuvered and some recommendations
 *Casual riders prefer to take longer trips averaging more than twice from members.
this analyze help show casual riders, how they could save more money in the long run by becoming a member instead of paying for rides based on ride_length
Introduce a casual only rewards program based on ride_length a certain range should be set ,which if they meet would  automatically qualify them to become members with free first month fee or 50% first month fee.

*taking a look at the table (averahe ride vs weekday)we can say the casual members tend to ride more on the weekends ,marketing team should create a weekend voucher promo for members. Cyclistic can callaborate with sport store or fashion store, so weekend trip so such locations can get them a discount .
