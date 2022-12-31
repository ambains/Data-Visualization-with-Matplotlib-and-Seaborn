# Ford GoBike Sharing System
## by Amrita Bains


## Dataset

The Ford GoBike dataset has information on the bike riders (customer or subscribers) such as their trip times, start stations, end stations, etc and the bike rides are covering the greater San Francisco Bay area.

The preliminary wrangling included the following findings:

1. The columns are not expanded in and part of the end_station_name is hidden. 

2. The duration_sec can be converted to hours so it is easier to interpret.

3. For tidiness, time and date can be separated in two different columns in the start_time and end_time columns.

4. Null values in member_birth_year and member_gender- these values cannot be replaced as these values are user entered fields. 

5. Null values in start_station_id and start_station_name- these values cannot be replaced as these values are captured by the database system and is an error in capturing these fields. 
 
6. start time and end time datatypes can be converted to datetime datatypes.



## Summary of Findings

The above findings were corrected to start the univariate visualizations for the variables of interest (duration_sec, start_station_id, start_time,start_date,bike_share_for_all_trips, user_type). The univariate visualizations focused on applying logarthimic axes transformation on the duration_sec variable and squart root axes transformation on the start_station_id to normalize the curves and get the insights outlined in the observation markdown cells.

The bivariate visualizations continued the focus on duration_sec, start_station_id, user_type. The plots used were heatmap, violinplot and scatterplot. An overplotting issue was recognized when plotting the days in start_date and log_duration_sec and to fix this issue, the plot type was changed from scatterplot to heatmap. The plot type change fixed the overplotting issue.

The multivariate visualizations continued the focus on duration_sec,start_station_id, and the days of the month from start_date. Another overplotting issue was recognized when plotting a scatter plot of the log_duration_sec against the start_station_id per the days of the month from start_date. The plot was changed to FacetGrid to resolve the overplotting, the FacetGrid provided a distribution per day of the month but it did not fully resolve the issue of overplotting. The overplotting issue was resolved by the solution provided by the mentor in the knowledge portion and the analysis question was changed from:

The duration of the trip in seconds per station id and day of the month to Average Time in minutes by hour and day.

Overall, the Ford GoBike sharing system is a dataset with attributes that provide great insights such as the longest trip taken by a bike rider, the busiest starting point for bike riders, the bike sharing experience for customer versus subscriber and the day of the month of the longest trip. 


## Key Insights for Presentation

From the exploration of the Ford GoBike Sharing System, the key insights are the the longest and shortest trip in seconds, the distribution of the bike rides per user type and the duration of a bike trip per day and hour.

The key insights focused on the usage of the bike, who is using the bike and the times and days are the busiest for the Ford GoBike Sharing System.