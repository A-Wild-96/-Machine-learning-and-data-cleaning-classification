#### Errors to fix
Numeric features. Function conv_check_float does not convert strings to floats. It checks if string is numerical, retains string if true and replaces with nan if false. Then conversion to float is done by astype(float). The reason for this is because astype(float) gets confused by characters such as backslashes, so they need to be filtered beforehand.

Machine learning - change i=1,2,3 to i=0,1,2

# Machine-learning-and-data-cleaning-classification

## Predicting chronic kidney disease

### Abstract
Learning project using supervised machine learning algorithms (logistic regression, k nearest neighbour and random forests available in python package sklearn) to predict chronic kidney disease (CKD) based off a large list of features. High recall values were consistently obtained in each algorithm indicating a low rate of false negatives - a valued feature of disease diagnosis algorithms. The dataset was cleaned - replaced erroneous values, fixed datatypes and addressed missing entries. Three different methods of missing entry replacement was performed. On average it is found that logistic regression and k nearest neighbour algorithms perform best by retaining as many features as possible, replacing missing entries with the mean the feature. Random forest algorithms showed no preference on method of data replacement.

Dataset was obtained from kaggle.com (https://www.kaggle.com/datasets/mansoordaku/ckdisease).

### Contents
<ul>
    <li>
      Dataset
    </li>
    <li>
      Data cleaning (errors and converting datatype)
      <ul>
          <li>Removing redundant features</li>
          <li>
              Categoric features
              <ul>
                  <li>Removing erroneous entries</li>
                  <li>Dummy variables</li>
              </ul>
          </li>
          <li>
              Numeric features
              <ul>
                  <li>Removing erroneous entries</li>
                  <li>Correcting datatype of numeric strings</li>
              </ul>
          </li>
      </ul>
  </li>
  <li>
       Data visualisation
  </li>
  <li>
       Data cleaning (missing values)
       <ul>
          <li>Reduce dataset due to sparse missing entries</li>
          <li>Create datasets with different cleaning methods
              <ul>
                  <li>Dataset 0 - Remove any features with missing entries</li>
                  <li>Dataset 1 - Remove subset of features with few missing entries, inpute average for remaining missing entries</li> 
              <li>Dataset 2 - Impute average for all missing entries</li> 
              </ul>
       </ul>
  </li>
  <li>
       Machine learning<ul>
    <li>Logistical regression</li>
    <li>K nearest neighbours</li>
    <li>Random forest decision trees</li>
    </ul>
  </li>
  <li>Conclusion</li>
</ul>
