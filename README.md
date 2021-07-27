Responsible-Data-Journalism-amid-COVID-19
===
Covid-19 Timeseries Dataset
---
I collected data and compiled this covid-19 time series dataset on 7/24/2021 and 7/25/2021. The following is a detailed introduction for each data set. (The latest update time of the data is around 2021/7/22).  

<style>
table th:first-of-type {
	width: 100px;
}
</style>

| Name of dataset  | Indicator description  | Selected countries  | Source| <div style="width: 500pt"> Notes |
| -- |-- | -- | -- | -- |
| cases_timeseries | It includes 2 indicators: the number of daliy new confirmed cases (new_cases) and the cumulative number of confirmed cases (cumulative_cases). | Canada, US, China, UK, Brazil, South Africa, Australia | Our World in Data Github URL: https://github.com/owid/covid-19-data/tree/master/public/data |  |
| deaths_timeseries |It includes 2 indicators: the number of daily new deaths (new_deaths) and the cumulative number of deaths (cumulative_deaths). | Canada, US, China, UK, Brazil, South Africa, Australia | Our World in Data Github URL: https://github.com/owid/covid-19-data/tree/master/public/data | |
| recovered_timeseries | It includes 2 indicators: the number of daily new recovered cases (recovered_cases) and the cumulative number of recovered cases (cumulative_recovered). | Canada, US, China, UK, Brazil, South Africa, Australia | JHU CSSE COVID-19 Dataset GitHub URL：https://github.com/  CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_time_series | US has stopped updating the data since 2020/12/14. UK has stopped updating the data since 2020/4/12. |
| hospital_patients_timeseries | It includes two indicators: the number of hospitalized patients daily due to covid-19 (hosp_patients), and the number of hospitalized patients due to covid-19 per million of the country population (hosp_patients_per_million). | Canada, US, UK | Our World in Data Github URL: https://github.com/owid/covid-19-data/tree/master/public/data | The data from Our World in Data comes from the European Centre for Disease Prevention and Control (ECDC) for a select number of European countries; and government sources for the United Kingdom, the United States, Canada, Israel, and Algeria. They are unable to provide data on hospitalizations for other countries for now. I just selected three of these countries.|
| testing_timeseries | It includes 2 indicators: daily number of new nucleic acid tests (new_tests) and the cumulative number of nucleic acid tests (total_tests). |Canada, US, UK, Australia |Our World in Data Github URL: https://github.com/owid/covid-19-data/tree/master/public/data | Many countries are not providing the data, such as China and Brazil. I just selected four of these countries. |
| vaccine_administration_timeseries | It includes 3 indicators: the total number of vaccinations (total_vaccinations), the number of people who have received at least one dose (people_vaccinated), and the number of people who have been fully vaccinated (people_fully_vaccinated). | Canada, US, China, UK, Brazil, South Africa, Australia | Our World in Data Github URL: https://github.com/owid/covid-19-data/tree/master/public/data | China only has data on the total number of vaccinations. Australia fails to provide data for the latter two indicators from 2021/3/15 to 2021/5/23. |
| Other covid-19 data provided by CDC | | US | Centers for Disease Control and Prevention https://data.cdc.gov/browse | I found a lot of more detailed data from the United States on the CDC website, which is very interesting. For example, the number of deaths divided by indicators such as age, gender, and race. Because the CSV format data sheet does not support multiple sheets, I changed the format of the data sheet to xlsx.| 

### Additional notes
* In the process of collecting data, I found that for unknown reasons, some countries lack certain kind of data (for example, China did not disclose data on the number of covid-19 hospitalizations, etc.).
* Due to the limited time, I only selected data from some representative countries. I can continue to collect data from other countries later if necessary.
