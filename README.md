# Multicampus_semi_project
   This is my first project as a Data Analyst and the project was done with Multicampus(based in Seoul, Gangnam) between Nov 14th, 2023 ~ Nov 20th, 2023 (4.5 days) to review what i learned in the first month.
   This project is to analize and predict three movies to be released in South Korea in Nov & Dec 2023.
   In order to execute the analisys and prediction, I've used a dataset from KOBIS and crawled sets of data from a Korean search engine Naver.


## Description

Including myself, the vast majority of people enjoy watching movies. 

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
* Encoding='UTF-8' / plt.rc('font', family='Malgun Gothic') - to use Korean letters in the visualization tools


### Installing

* Except for BigQuer, all libraries are usable on Jupyter Notebook. You can simply call them with "!pip install"
* A dataset from KOBIS and crawled data from Naver should be uploaded on Cloud Storeage before visualizing data


### Executing program

* This isn't a program, but a step by step guide to show how i analized and predicted the data(conclusion not mentioned)


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
