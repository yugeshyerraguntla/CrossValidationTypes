# CrossValidationTypes

Normal Train-Test split does not give an indication of how well the model will perform to an unseen data set. Hence we choose cross validation to ensure that all data is considered in training and testing at some point.

Cross-Validation
- resampling technique that helps to make our model sure about its efficiency and accuracy on the unseen data. 
- It is a method for evaluating Machine Learning models by training several other Machine learning models on subsets of the available input data set and evaluating them on the subset of the data set.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

- The first step is to divide the cleaned data set into K partitions of equal size.
- Then we need to treat the Fold-1 as a test fold while the other K-1 as train folds and compute the score of the test-fold.
- We need to repeat step 2 for all folds taking another fold as a test while remaining as a train.
- Last step would be to take the average of scores of all the folds.

Techniques:
- LeaveOne Out CV : Taking only 1 value at a time.
- K Fold CV       : The data is divided into k subsets or we can take it as a holdout method repeated k times, such that each time, one of the k subsets is used as the validation set and the other k-1 subsets as the training set. The error is averaged over all k trials to get the total efficiency of our model.
  - We can see that each data point will be in a validation set exactly once and will be in a training set k-1 time. 
  - This helps us reduce bias as we are using most of the data for fitting and reduces variance as most of the data is also being used in the validation set.
 - StratifiedKFold: K Fold will not work for imbalanced dataset. Each fold contains approximately the same strata of samples of each output class as the complete. This variation of using a stratum in K Fold Cross Validation is known as Stratified K Fold Cross Validation.
