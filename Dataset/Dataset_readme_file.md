### Context
----
This is a useful dataset to train and test Machine Learning forecasting algorithms and compare results with the official forecast from weekly pre-dispatch reports. The following considerations should be kept to compare forecasting results with the weekly pre-dispatch forecast:

Saturday is the first day of each weekly forecast; for instance, Friday is the last day.
A 72 hours gap of unseen records should be considered before the first day to forecast. In other words, next week forecast should be done with records until each Tuesday last hour.
Data sources provide hourly records. The data composition is the following:

1. Historical electricity load, available on daily post-dispatch reports, from the grid operator (CND).
2. Historical weekly forecasts available on weekly pre-dispatch reports, both from CND.
3. Calendar information related to school periods, from Panama's Ministery of Education.
4. Calendar information related to holidays, from "When on Earth?" website.
5. Weather variables, such as temperature, relative humidity, precipitation, and wind speed, for three main cities in Panama, from Earthdata.

### Content
----
The original data sources provide the post-dispatch electricity load in individual Excel files on a daily basis and weekly pre-dispatch electricity load forecast data in individual Excel files on a weekly basis, both with hourly granularity. Holidays and school periods data is sparse, along with websites and PDF files. Weather data is available on daily NetCDF files.

For simplicity, the published datasets are already pre-processed by merging all data sources on the date-time index:

1. A CSV file containing all records in a single continuous dataset with all variables.
2. A CSV file containing the load forecast from weekly pre-dispatch reports.
3. Two Excel files containing suggested regressors and 14 training/testing datasets pairs as described in the PDF file.

### Acknowledgements
----
Aguilar Madrid, Ernesto (2021), “Short-term electricity load forecasting (Panama case study)”, Mendeley Data, V1, doi: 10.17632/byx7sztj59.1
