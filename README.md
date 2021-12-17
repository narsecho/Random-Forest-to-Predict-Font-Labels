Data resource and selection referred to KNN

Preliminary Data Processing:
1. Check the data balancing between labels;
2. Apply PCA

1. Rebalancing data by SMOTE
1.1 Check balancing
1.2 Split train and test data by 80%/20%;
1.3 Apply SMOTE on train and test, and check the data shape;
1.4 Regroup training and testing data set.

2. Present the function of Random Forest

3. Initial Random Forest Implementation
3.1 Fix RF parameters: ntree = numbers of trees = 100; ntry == sqrt (r) =features,use only the r features Z1(n) … Zr (n) for each case “n"
3.2 Test the trained RF classifier on the test set. Display global accuracy and confusion matrix on train set and on test set;

4. Hyper parameters fine-tune
4.1 Launch again an RF classifier with ntry = sqrt (r) , but with n trees = 200 and ntrees = 300.
4.2 select the best number of trees = ntree * among 100, 200,300 by comparing accuracies on test set.

5. Discussion of Importance of Features
5.1 Let RF* be the best RF classifier; For RF* compute the importances IM1 … IM10 of features Z 1 … Z10. Explain and display these IMk
5.2 Explain what is the practical meaning of eigen value Lk /400. 
5.3 Scatterplot (Lk, IMk ) for k =1…10 and interpret this plot to evaluate the potential relation between Lk and IMPk

6. Find the worst pair of classes classification and further fine-tune by bag of RF. 
6.1 Compute the 4x4 confusion matrix of RF* on the test set.
6.2 Train a newRF classifier with ntry sqrt (r) and numbers of trees = ntree * to classify CLi versus CLj.
6.3 Run bag of RF on the 1v1 RF classifiers
