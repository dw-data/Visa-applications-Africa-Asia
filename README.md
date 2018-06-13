# How are the prospects of receiving a long-term visa for Germany?

You can read one article based on this data analysis [at DW](http://dw.com/a-44097212).

**Idea:** by Daniel Pelz

**Additional Research:** by Rodion Ebbighausen

**Data analysis:** Gianna-Carina Gruen

**Data Source:** German Foreign Office. Provided to German party "Die Linke" via several "Kleine Anfragen" and upon own request

**Provided Data Format:** PDF files

## Data cleaning

- Conversion with Abbyy Fine Reader into csv
- Cleaning csv files with Regular Expressions
- Joining the files for each year into one big file
- Cleaning it via Open Refine
- Converting all numbers in the right number format (German to English formatting)

## Data preparation

- Remodeling data so there is only one value column for each step of the application process and adding an additional column `applied to` containing information whether it was an application for asylum to Germany or to the Schengen area in general. In our analysis we focused on applications for visa in Germany (for study, work or family reunion for example), thus the below figures do not include visa for short term stays in the Schengen area.

- For countries with several branches, each office is initally listed separately. In addition the respective country has a total ('Gesamt') entry.
In order to not falsify results, these total figures are filtered out. Additionally, country and local branch are fused into one name in a new column `application_origin`.

- The dataset also contains applications filed in a country that is part of the EU/Schengen zone. Since EU citizens would not need to apply for a visum, it must be citizens of other nations. Since we cannot determine the nationality of these applicants, for further analysis applications from EU countries are excluded.

- The German Federal Foreign Office calculates the rejection rate based on the number of "processed" applications which includes granted, rejected and withdrawn requests. For our own analysis, we calculated the rejection rate differently: We introduced a new variable "decided applications" that equals the sum of all granted and all rejected applications that were filed in a specific local branch. Our rejection rate that we call "share negative" is calculated by dividing the number of rejected applications by the number of total decisions multiplied by 100.

- Please note that the data refers to applications filed in a specific location/country and do not necessarily translate to the applicant's nationality. We assume that this is the case for the majority of applications, however not all countries have German embassies where visa applications can be made, so that applicants will have to file in another country.

## Data Analysis results

The results for Africa can be found in this article [at DW](http://dw.com/a-44097212). Results for other regions to follow.

If you would like to look at the data for specific branches or single years, please refer to this [interactive data table](https://dw-data.github.io/datatable-visa-applications/).
