# Alphabet Soup :: Deep Learning Challenge

### Background

The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures.

Alphabet Soup’s business team provided a CSV file containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as:

-   **EIN**  and  **NAME** — Identification columns
-   **APPLICATION_TYPE** — Alphabet Soup application type
-   **AFFILIATION** — Affiliated sector of industry
-   **CLASSIFICATION** —G overnment organization classification
-   **USE_CASE** — Use case for funding
-   **ORGANIZATION** — Organization type
-   **STATUS** — Active status
-   **INCOME_AMT** — Income classification
-   **SPECIAL_CONSIDERATIONS** — Special considerations for application
-   **ASK_AMT** — Funding amount requested
-   **IS_SUCCESSFUL** — Was the money used effectively

### Technical Requirements

The implementation of this project requires the use of [TensorFlow](https://www.tensorflow.org/install/pip).

## Alphabet Soup

The main objective of this project is to develop a solution using the knowledge on machine learning and neural networks, analysing the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

### Overview

This projects aims to analyse different models to implement a solution for the Alphabet Soup database.

The first model consists in a multi-layer Neural Network, that can be setup to be trained using a reduced database, and finally the evaluation of its performance.

Last but not least, an optimisation of the first model is considered in this project, where there are further analysis on the features that have been used, as well as combination of different setup to find an optimisation of this model.

This report is organised in 3 main sections
 * Preprocess the Data
 * Compile, Train, and Evaluate the Model
 * Optimise the Model

### Preprocess the Data

The initial steps required for this project is to preprocess the data, removing the unwanted columns, if any, as well as converting the data type when it is appropriate.

The column `IS_SUCCESSFUL` is assigned as the target variable for the proposed model.

The columns `EIN`  and  `NAME` have been removed from the input data, considering those variables are identifiers for each entry in the database.

The remaining columns (`APPLICATION_TYPE`, `AFFILIATION`, `CLASSIFICATION`, `USE_CASE`, `ORGANIZATION`, `STATUS`, `INCOME_AMT`, `SPECIAL_CONSIDERATIONS` and `ASK_AMT`) are assigned to be the features analysed by the proposed model.

After the definition of the target variable and the set of features, it was applied a binning technique to reduce the number of different groups within a feature. The following features (columns) were  revised:
* `APPLICATION_TYPE`: as presented in the figure below, a cutoff value of **528** was applied to identify the list of application types to be replaced by "Other".
![Applicatin Type cuttof](./Images/application_type.png)
* `CLASSIFICATION`: as presented in the figure below, a cutoff value of **1883** was applied to identify the list of classifications to be replaced by "Other".
![Classification cuttof](./Images/classification.png)

Finally, the categorical features that are not numeric to be converted accordintly using the function `pd.get_dummies`, which is presented in the figure below:
![Convert categorical data to numeric with pd.get_dummies](./Images/dummies.png)

After all these previous steps, data can be now processed and scaled accordingly to prepare the training and test data, which will be used for the further phases of this project.

### Compile, Train, and Evaluate the Model


-   What variable(s) are the target(s) for your model?
-   What variable(s) are the features for your model?
-   What variable(s) should be removed from the input data because they are neither targets nor features?




### Optimize the Model


## References

IRS. Tax Exempt Organization Search Bulk Data Downloads.  [https://www.irs.gov/](https://www.irs.gov/charities-non-profits/tax-exempt-organization-search-bulk-data-downloads)