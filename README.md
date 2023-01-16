Responsible-Data-Journalism-amid-COVID-19
===
2023/01/16 Update
---
Applied the machine learning algorithms to the covid-19 data in the US. See the jupyter notebook in this link: [link](https://github.com/Anqi-Xu/Responsible-Data-Journalism-amid-COVID-19/blob/main/Forecasts%20of%20COVID-19%20Cases%20in%20the%20US.ipynb)


2021/09/28 Update
---
You can try the interactive plot in Colab Notebooks in this link：
https://drive.google.com/file/d/1n6GsXXbffj19VhVnuXb_sEI6oEkCZKW3/view?usp=sharing

2021/08/17 Update
---
* I added a trendline to the existing plots that shows cumulative RMSE.
* To compare the RMSE between three months, I normalized the error and added another kind of plot to show the differences.
* I simplified the python code by using for loops and arrays.

Canada cases and vaccinations predictions (Last updated 2021/08/13)
---
* I used timeseries data for cumulative cases and vaccinations in Canada to predict three consecutive months, and made three predcitions showed in the same plot for each model.
* For cumulative cases, I used timeseries data to predict date of April 2020, May 2020, and June 2020.
* For vaccinations,I used timeseries data to predict data of Feb 2021, March 2021 and April 2021.

Canada cases and vaccinations predictions (Last updated 2021/08/09)
---
* I tested four timeseries models(MA Model, AR Model, ARIMA Model and SARIMA Model) to predict both cumulative cases and total vaccinations in Canada and also generated 95% pointwise bands for each model.
* For cumulative cases, I used timeseries data from 2020/1/25 to 2020/3/31 to predict data of next month(April 2020).
* For vaccinations,I used timeseries data from 2020/12/14 to 2021/1/31 to predict data of next month(Feb 2021).
* The reason why I did not use the other 5 models I used last week：
1. For Holt's Linear Model and Holt's Winter Model, Python's statsmodel and sklearn cannot output the confidence intervals of results from the two models(I have checked the Python's offical guide.).
2. For other three regression models such as linear regression model, their prediction accuracies are quite poor(It can be seen from the experiment last week that their RMSE are relatively high.).
3. Linear regression has the basic assumption that the independent variables are independent of each other, but I think daily cumulative cases and vaccinations cannot meet this assumption.
---
Canada cases and vaccinations predictions (Last updated 2021/08/03)
---
* I tested nine models to predict the cumulative number of cases and vaccinations in Canada in July, and came to the following conclusions. For the cumulative number of cases, the SARIMA Model performs best. For the number of vaccinations, Holt's Linear Regression performs best. 
* The two jupter notebooks have been uploaded into the folder: Prediction Code.
### Additional notes
* Due to limited time,I have just tested two Canada datasets. If this method works, I will test more datasets later.
---
Covid-19 Timeseries Dataset (Last updated 2021/07/27)
---
I collected the data on 7/24/2021 and 7/25/2021 and compiled this covid-19 time series dataset. The following is a detailed introduction for each data set. (The latest update time of the data is around 2021/7/22).  

| Name of dataset  | Indicator description  | Selected countries  | Source| <img width=20000/> Notes<img width=20000/> |
| :--: |-- | -- | -- | -- |
| cases_timeseries | It includes 2 indicators: the number of daliy new confirmed cases (new_cases) and the cumulative number of confirmed cases (cumulative_cases). | Canada, US, China, UK, Brazil, South Africa, Australia | Our World in Data|  |
| deaths_timeseries |It includes 2 indicators: the number of daily new deaths (new_deaths) and the cumulative number of deaths (cumulative_deaths). | Canada, US, China, UK, Brazil, South Africa, Australia | Our World in Data| |
| recovered_timeseries | It includes 2 indicators: the number of daily new recovered cases (recovered_cases) and the cumulative number of recovered cases (cumulative_recovered). | Canada, US, China, UK, Brazil, South Africa, Australia | JHU CSSE COVID-19 Dataset | US has stopped updating the data since 2020/12/14. UK has stopped updating the data since 2020/4/12. |
| hospital_patients_timeseries | It includes two indicators: the number of hospitalized patients daily due to covid-19 (hosp_patients), and the number of hospitalized patients due to covid-19 per million of the country population (hosp_patients_per_million). | Canada, US, UK | Our World in Data | The data from Our World in Data comes from the European Centre for Disease Prevention and Control (ECDC) for a select number of European countries; and government sources for the United Kingdom, the United States, Canada, Israel, and Algeria. They are unable to provide data on hospitalizations for other countries for now. I just selected three of these countries.|
| testing_timeseries | It includes 2 indicators: daily number of new nucleic acid tests (new_tests) and the cumulative number of nucleic acid tests (total_tests). |Canada, US, UK, Australia |Our World in Data | Many countries are not providing the data, such as China and Brazil. I just selected four of these countries. |
| vaccine_administration_timeseries | It includes 3 indicators: the total number of vaccinations (total_vaccinations), the number of people who have received at least one dose (people_vaccinated), and the number of people who have been fully vaccinated (people_fully_vaccinated). | Canada, US, China, UK, Brazil, South Africa, Australia | Our World in Data | China only has data on the total number of vaccinations. Australia fails to provide data for the latter two indicators from 2021/3/15 to 2021/5/23. |
| Other covid-19 data provided by CDC | | US | Centers for Disease Control and Prevention | I found a lot of more detailed data from the United States on the CDC website, which is very interesting. For example, the number of deaths divided by indicators such as age, gender, and race. Because the CSV format data sheet does not support multiple sheets, I changed the format of the data sheet to xlsx.| 
### Data resource URL
* Our World in Data : <https://github.com/owid/covid-19-data/tree/master/public/data>
* JHU CSSE COVID-19 Dataset: <https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_time_series>
* Centers for Disease Control and Prevention: <https://data.cdc.gov/browse>
### Additional notes
* In the process of collecting data, I found that for unknown reasons, some countries lack certain kind of data (for example, China did not disclose data on the number of covid-19 hospitalizations, etc.).
* Due to the limited time, I only selected data from some representative countries. I can continue to collect data from other countries later if necessary.

---
