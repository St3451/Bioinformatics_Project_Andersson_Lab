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
* Tested the effect of increasing the size of the negative set 
* Improved evaluation
* Implemented removal of intra ATAC overlaps by rank (total CAGE scpre) approach 
* Assess the meaningfulness of the new input
* Tested the effect of using different filters on the negative set
* Added feature importance
* Implemented grid and random search for hyperparameters tuning

## Week 6
* Added weight scalers (balanced by the classifier internal function, balanced by custom function, set by the user as hyperparameter) for both RF and LGBM 
* Added LGBM peformance evaluation during training (evaluation and plot of binary error, MCC, F1, TPR and TNR)
* Extensive test of the different weight scalers on three datasets (differing by the negative and positive samples size ratio: 0.5, 1, 3)
* Added seed values on all CV chromosomes split (fairer comparison between methods) and max number of CV iterations for grid and random search (speed up the search)

## Week 7
* Enabled GPU for LGBM (issue: see warning during training) and SVM (ThunderSVM)
* Implemented prediction on test data for all models
* Polished the code


* Ideas to implement:
    * Set up the conda environment to run the scripts in the server (useful for 10+ hours jobs)
    * Run RBF SVM on final data to motivate our choice of using RF and LGBM over SVM 
    * Fast grid search with a subset of the data, validation of the optimal parameters on the full data, plot (scatter for continuous and boxplot for categorical) of each hyperparameter against the target variable 
    * Smooth the input (smooth spline)
