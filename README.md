# Stefano_Project_Thesis
This is the repository for Stefano project and thesis

# Project
* Prediction of potential active open chromatin regions using CAGE data

## Week 1, 2
* Familiarize with the problem and data
* Understand dREG input and output

## Week 3 
* Implemented exploration and input profiles extraction (1 replicate) for ML models
* Implemented first ML models: random forest, lightGBM, SVM RBF
* Models evaluation

## Week 4
* Implemented profiles extraction using all replicates
* Implemented cross validation
* Implemented two SVM RBF models: SVR + logistic regression and SVC
* Modified input data by filtering the negative set
* Assessed profile extraction and models performance on new input data

## Week 5
* Implemented cross validation by chromosomes
* Increased the size of the negative set (positive to negative ratio is now 1/3)
* Added Matthews correlation coefficient (removed RMSE), classification report heatmap, ROC in log scale, precision-recall curve
* Fixed confusion matrix
* Assess the meaningfulness of the new input

