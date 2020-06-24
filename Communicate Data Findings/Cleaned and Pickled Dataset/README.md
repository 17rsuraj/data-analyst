### Cleaned Dataset

At the end of data wrangling process, a cleaned dataset is exported in <code>ford_gobike_data_cleaned.csv</code> file.

For Explorative Data Analysis, few columns are added to the existing cleaned dataset. This extended dataset is exported in <code>ford_gobike_data_extended.csv</code>.
Added new columns are:

* `age` :        Age of the user
* `year_month` : Year and month of the Ford GoBike trip
* `dayofweek` :  Day of week of the Ford GoBike Trip
* `start_hr` :   Ford GoBike trip starting hour in a day
* `end_hr`:      Ford GoBike trip ending hour in a day

### Pickle Dataset

As the project is completed over few days, it is always good to store the DataFrame as Pickle file.
Following pickle files are generated.

* `ford_gobike_data_extended.pkl` : Cleaned dataset with additional calculated columns
* `df_main.pkl` :                   Cleaned Dataset
* `df_route.pkl` :                  Dataset with Ford GoBike trip routes - calculated DataFrame from cleaned dataset
