# Random Forest-based clinical outcome prediction using radiomic features
- Clinical outcome include: "histype", "WT1", "ER", "TR"
- Radiomic features include: "age", "mean", "sd", "entropy", "mpp"
- Prediction algorithm: Random Forest

## Contents
1. [R code](https://github.com/Radilology-HKU/RF_class/blob/master/RF_Prediction_radioinfo.R) 
2. [Python code 1](https://github.com/Radilology-HKU/RF_class/blob/master/roc.ipynb) : A simplified version
of [origin code file](https://github.com/Radilology-HKU/RF_class/blob/master/open_img_train_rf.ipynb). 
3. [Python code 2](https://github.com/Radilology-HKU/RF_class/blob/master/roc1.ipynb) : A test version 
of [Python code 1](https://github.com/Radilology-HKU/RF_class/blob/master/roc.ipynb), only order of input features changes. 
4. [Python code 3](https://github.com/Radilology-HKU/RF_class/blob/master/roc2.ipynb) : A test version 
of [Python code 1](https://github.com/Radilology-HKU/RF_class/blob/master/roc.ipynb), only input label changes. 


## Attention
1. Before push local repository to Github, remember to ensure **all names of data files have been added to ".gitignore" file**, 
and are not traced by Git. Othervise data file will be submitted to Github repository. The code file itself is not so crucial without
original data. 
2. The difference between "training_n.xlsx" written in code file and original data file "training.xlsx" is that 
data belong to 7 indivisuals marked in red are delated. 


## Conclusion
1. Till now there is still few differences between prediction result calculated by R code and Python code. 
2. Reasons include, but not limited to: 
       1. Designs of packaging functions (random forest, roc/auc calculation) in R and Python are different. 
       For example, the number of altomatic generated thresholds in Python function is fewer, so the roc curve 
       looks like a "ladder diagram". (see [Python code 1](https://github.com/Radilology-HKU/RF_class/blob/master/roc.ipynb))
       
       2. Many default parameters in packaging functions (random forest, roc/auc calculation) might have an inestimable 
       impact on the final result, because some operation in packaging functions  are altomatically finished. 
       
       3. Essential problems are not considered into prediction. Throuth two test (see [Python code 2](https://github.com/Radilology-HKU/RF_class/blob/master/roc1.ipynb) and [Python code 3](https://github.com/Radilology-HKU/RF_class/blob/master/roc2.ipynb) ), we can conclude that 
       the order of input features can influence final result. Besides, whether 4 labels (PR, ER, WT1, hisype) should be predicted together might 
       depends on the nature of this research. 

3. Considering more details of this research might be helpful to do this classification more accurately. 
