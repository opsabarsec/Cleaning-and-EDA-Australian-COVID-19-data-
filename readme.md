# COVID-19 Australian data cleaning and exploratory analysis

![aucovid](covid.png)
## 1. Background
2020 will be remembered as the year pandemic struck. Healthcare is under pressure and everyone needs a picture of the situation as clear as possible.
Still, raw data are partial and most of all contain duplicates, typos and having those cleaned is the first step to understand how the situation is evolving.
The project goal is to clean the raw data automatically, then present graphically situation in Australia.

## 2. The data
Those contain personal data and PCR test results for the Australian population during the first pandemic wave. Two tables in sqlite format were supplied, one with patients personal information, and the other with the results of COVID-19 testing. These have to be transformed to Pandas Dataframes in Python and joined later. 

## 3 Cleaning and EDA

Data have been cleaned and deduplicated using the python package ["fuzzywuzzy"](https://programtalk.com/python-examples/fuzzywuzzy.process.dedupe/)
This package uses as criterium the Levenshtein distance:
% duplicates =  31.25

The code for cleaning is at the [following Jupyter notebook](https://github.com/opsabarsec/inria-aphp-assignment/blob/master/Australia_COVID-19_notebook_1.ipynb)

The final cleaned dataset has then been analyzed and data plotted with Matplotlib. 
[EDA code Jupyter notebook](https://github.com/opsabarsec/inria-aphp-assignment/blob/master/Australia_COVID-19_notebook_2.ipynb)

Data are plotted showing COVID incidence as a function of age or location in Australia.
Cloropleth maps are not shown in Jupyter notebooks by the GitHub website, the example below has been uploaded as image file

![tested_cases_map](covidau.png)
