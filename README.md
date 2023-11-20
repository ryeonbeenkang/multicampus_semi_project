# Multicampus_semi_project
   This is my first project as a Data Analyst and the project was done with Multicampus(based in Gangnam, Seoul) between Nov 14th, 2023 ~ Nov 20th, 2023 (4.5 business days) to review what i learned in the first month.
   
   This project is to analyze and predict three movies to be released in South Korea in Nov & Dec 2023.
   
   In order to execute the analysis and prediction, I've used a dataset from KOBIS and crawled sets of data from a Korean search engine Naver.


## Description

   Including myself, the vast majority of people enjoy watching movies. Whenever i finish a good movie, there's always a remaining question, "What should i watch next?." I've decided to analyze a set of data and to see what i should watch next. 

   The dataset from KOBIS(1962.11.03 ~ 2021.7.15 with 23,403 movie data) allows me to understand the best 'director','production company','distributor','importer','nationality','genre','rating','run time', 'actors', and 'writers.' I give each category a point (1~5points) based on how the average people think as 'key factors.'(According to the analysis, the number of movies with more than 1 million viewers is 777)

   There are three upcoming movies that piqued my interest and I've decided to calculate their points based on my study above.

   In conclusion, two out of three movies have more than 50% chance of going viral(more than 1 million viewers) and i've summurized the step-by-step guide in a separate PDF(not uploaded here).

## Getting Started

### Dependencies

* Windows10
* Jupyter Notebook
* Google Cloud Platform(BigQuery, Cloud Storage)
* Seaborn / Matplotlib
* Requests 
* BeautifulSoup 
* Time 
* CSV
* collections module Counter
* Encoding='UTF-8' / plt.rc('font', family='Malgun Gothic') - to use Korean letters in visualization graphs


### Installing

* Except for BigQuery, all libraries are usable on Jupyter Notebook. You can simply call them with "!pip install"
* A dataset from KOBIS and crawled data from Naver should be uploaded on Cloud Storeage before visualizing data


### Executing program

* This isn't a program, but a step by step guide to show how i analyzed and predicted the data(conclusion not mentioned here)


## Help
A few advice from the coach Kim as follows.

1. A dataset written in Korean language should be saved as 'UTF-8' csv type.
2. Search Engines like Naver will detect and block unusual traffic when trying data crawling, you should then use time.sleep() function to delay the crawling time
   ```
   import time
   time.sleep(1)
   ```
3. To find out what sort of exception has occured, you can use the following except code. Then, e will specify the cause of error.
   ```
   except Exception as e:
   ```
4. When data crawling fails, take a deep breath and do not rush to try again. Take some time. It's unusual traffic, Server Engineer of the Search Engine would not like it.
5. When table names are too long, use AS {shorter_version_name} while using SQL
6. When bins parameter of Histplot doesn't work, you should check the data type by using 'df.describe()' or 'df.info().' You should also check either columns or rows includes inadequate data(In my case, there were a few). Additionally, you can use CAST to change the data type, in my case, i've changed object data type to INT 64 for numbers.


## Author
Ryeonbeen Kang
ryeonbeenk@gmail.com

## References
* Seaborn - https://seaborn.pydata.org/
* Google BigQuery - https://cloud.google.com/python/docs/reference/bigquery/latest
* Big Data Map(in Korean) - https://www.bigdata-map.kr/datastory
* Culture Big Data Platform(in Korean) - https://www.culture.go.kr/bigdata/user/data_market/detail.do?id=9d00dd80-4a54-11eb-af9a-4b03f0a582d6
* KOFIC(KOBIS) Data(in Korean) - https://www.kobis.or.kr/kobis/business/stat/offc/searchOfficHitTotList.do?searchMode=year
