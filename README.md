# Alphabet Soup Deep Learning Model - Testing and Analysis
- - -
## Overview of the Analysis

### Purpose

The nonprofit foundation Alphabet Soup is interested in a tool that can help them select the applicants for funding with the best chance of success in their ventures. We will be using Python to design a Deep Learning Neural Network to create a Binary Classification Model that can predict if an Alphabet Soup-funded organization will be successful based on the features in a historical funding dataset.

### The Dataset

CSV file containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, including:

* **`EIN`** and **`NAME`**—Identification columns  
* **`APPLICATION_TYPE`**—Alphabet Soup application type  
* **`AFFILIATION`**—Affiliated sector of industry  
* **`CLASSIFICATION`**—Government organization classification  
* **`USE_CASE`**—Use case for funding  
* **`ORGANIZATION`**—Organization type  
* **`STATUS`**—Active status  
* **`INCOME_AMT`**—Income classification  
* **`SPECIAL_CONSIDERATIONS`**—Special considerations for application  
* **`ASK_AMT`**—Funding amount requested  
* **`IS_SUCCESSFUL`**—Was the money used effectively

### Process

From this labeled dataset, we built a [neural network model](Colab_Notebooks/Alphabet_Soup_Model.ipynb) to predict if historical funding was marked "IS_SUCCESSFUL" or not using `Binary Classification Analysis`, and then set about several attempts at building a [second model](Colab_Notebooks/AlphabetSoupCharity_Optimization.ipynb) to optimize those results with the goal of a 75% accuracy rate, according to the process outlined below:

## Results

### Term Descriptions (?)

### Neural Network 1

### Neural Network 2

#### Optimization Notes

## Summary

### Recommendations

- - -

## References

IRS. Tax Exempt Organization Search Bulk Data Downloads. [https://www.irs.gov/](https://www.irs.gov/charities-non-profits/tax-exempt-organization-search-bulk-data-downloads)