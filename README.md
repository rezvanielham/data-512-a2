# Human Centered Data Science Second Assignment
## Bias On WikiPedia

[Assignment](https://wiki.communitydata.cc/HCDS_(Fall_2017)/Assignments#A2:_Bias_in_data) Description

## Goal of the project:
The goal of this assignment is to explore the concept of 'bias' through data on Wikipedia articles - specifically, articles on political figures from a variety of countries.
* perform an analysis of how the coverage of politicians on Wikipedia and the quality of articles about politicians varies between countries
* list the countries with the greatest and least coverage of politicians on Wikipedia compared to their population.
* list the countries with the highest and lowest proportion of high quality articles about politicians.

## Steps to Reproduce 
* Clone the repository.
* Run the Jupyter Notebook named "hcds-a2-bias" : Note that call to ORES service might take close to an hour to complete.

### ORES
* [ORES](https://en.wikipedia.org/wiki/Aaron_Halfaker https://www.mediawiki.org/wiki/ORES)  (Objective Revision Evaluation Service) is a web service and API that provides machine learning as a service for Wikimedia projects maintained by the Scoring Platform team. The system is designed to help automate critical wiki-work – for example, vandalism detection and removal. Currently, the two general types of scores that ORES generates are in the context of "edit quality" and "article quality".More detailed API documentation can be found [here](https://www.mediawiki.org/wiki/ORES). 

## Source data
Wikipedia data:

## License of the source data
* MIT License(https://opensource.org/licenses/MIT)
## Wikimedia Foundation terms of use
https://wikimediafoundation.org/wiki/Terms_of_Use/en


Column name | Value | Description
--- | --- | ---
page | string | artcile name on Wikipedia
country | string | name of country
rev_id | int | revision id required to make ORES api call

Population data:

Column name | Value | Description
--- | --- | ---
Location | string | name of country
Location type | string | country type
Timeframe | string | time at which data was acquired-mid2015
Data | string(need to be converted to number format) | population size of the country

## Final data

Column name | Value | Description
--- | --- | ---
country | string | name of country
artcile_name | string | artcile name on Wikipedia
revision_id | int | revision id required to make ORES api call
artcile_quality | string | predicted quality returned from ORES api call
population | int | population size of the country
