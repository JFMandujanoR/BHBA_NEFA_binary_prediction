# rtFMS Detection Outcome for Blood BHBA

The following picture is a histogram of the balanced accuracy after running all the options. We have a mean = 0.748 with sd = 0.036

![histogram](https://github.com/JFMandujanoR/My_classification/blob/master/bal_acc_BHBA_multi_bin.png)

We used the rtFMS technique to obtain the following tree with 21 terminal nodes:

![tree](https://github.com/JFMandujanoR/My_classification/blob/master/tree_BHBA_multi_bin.png)

We have n models per branch. These n models have a similar performance. On the bottom of the tree we can see box plots centered in the mean balanced accuracy of the n models in the branch. We then choose the branch with the highest mean balanced accuracy.

Then we can select the branch 10, with mean = 0.79 and sd = 0.007:

- Variable: IR
- EMR Standardization: EMR.STAND
- Standardization: FD, FD.EMR, SD, SD.EMR
- Algorithm: GLMNET

Top 5 branches: 7, 6, 14, 2, 13


Note: The other variables do not appear in these conclusions because their elections among their options are not significant for the final result. In other words, _it doesn't matter which option we choose_.

_________________________________________________________________________________________________________________________________
