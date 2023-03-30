# Alphabet Soup Deep Learning Model - Testing and Analysis
![Neural Network stock photo](Images/neural-network.jpg)
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

#### Data Preprocessing:

1. Binning rare occurances of categorical values with more than 10 unique values into an "Other" category for clarity.

2. Encoding all categorical values into 1s and 0s so our model can parse them.

3. Splitting the data into a "features" array `X` and a "target" array `y` and further splitting those into `training` and `testing` datasets.
    * We determined that the `IS_SUCCESSFUL` column was our target value, and so set this as our `y` array.
    * We determined that the `EIN` and `NAME` columns were neither targets nor features, and so removed them from the dataset
    * We determined that the remaining columns were our features, and so set them as our `X` array

4. Scaling the `training` and `testing` features to a standard level so no values are overly favored by the algorithm

#### Model Creation:

1. Creating an initial model with an input layer of 80 nodes and a hidden layer of 30 nodes assigned, loosely shooting for a simpler model with about a double nodes to features ratio after preprocessing as a starting point.

2. Compiling and training the model.

3. Evaluating the model using the testing data to calculate its loss and accuracy.

4. Plotting the training history loss and accuracy for context.

5. Saving and exporting the model to an `HDF5` file.

#### Model Optimization:

1. Initial attempts were made to simplify the input data & remove potential outliers, but this caused the network to perform more poorly.

2. Adjusting the input data to improve accuracy and correct for possible underfitting, we modified the binning process to allow for more complexity in the dataset.

3. Importing `keras tuner` and attempting many variations in model depth, number of neurons per layer, alternative activation functions, and number of epochs in the training regimen by using an early stopping callback function.

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