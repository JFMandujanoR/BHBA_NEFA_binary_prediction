# My_classification
Classification for NEFA and BHBA:
Report of prediction model for bNEFA and bBHBA using QCheck data

In this repository we present the outcomes of the Regression Tree Full Model Selection (rtFMS) approach to select the best prediction model in two tasks: to dectect high blood BHBA and NEFA values (detection/classification task), and to predict a numeric value of those indicators (regression task). We used the QCheck data to test different permutations of possible models, we list the different options per task below.

__Detection/Classification Task:__

We run 384 models (per indicator), using one of the following options:

- Type of Variable (5): FAF, FAF1, FAF2, FAF3, IR
- Use of EMR_standardization (2): EMR.STAND, EMR.NONE (just for IR)
- Type of Standardization (5): Raw, FD, SD, FD.EMR, SD.EMR (just for IR)
- Filter (2): AllWN, EMR212 (just for IR)
- Use of Breed (2): Breed.Yes, Breed.No
- Time of milk sampling (2): Milk.Model.Yes, Milk.Model.No
- Algorithms (4): Elastic Net, LDA, GBM, Random Forest"

We fit a __regression tree model__ using the metric __balanced accuracy__ as target variable and as regressors the afforementioned _options for the model_. With the following links we can see the results obtained for detecting high blood NEFA and blood BHBA.

- Here we can find the [rtFMS detection outcome for blood NEFA in dairy cows](https://github.com/JFMandujanoR/My_classification/blob/master/BloodNEFA.md)
- Here we can find the [rtFMS detection outcome for blood BHBA in dairy cows](https://github.com/JFMandujanoR/My_classification/blob/master/BloodBHBA.md)
__________________________________________________________________
_Reported by: J. Francisco Mandujano R. (UW-MAdison)_

_mandujanorey@wisc.edu_
