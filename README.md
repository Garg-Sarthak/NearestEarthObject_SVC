# Devcomm-Task1-Sarthak
Analyses a Dataset 'NASA - Nearest Earth Objects' from kaggle, plots visualisation to analyse feature interdependency/boundary using SVM classification model. Uses different kernels : "rbf","sigmoid","poly" compares them on various metrics such as precision scores, f1 scores, roc curve, etc.

Uses the Dataset : "NASA - Nearest Earth Objects" from kaggle , link = https://www.kaggle.com/datasets/sameepvani/nasa-nearest-earth-objects?select=neo.csv

Libraries used : numpy, pandas, matplotlib, sklearn, seaborn

Converted the CSV file containing dataset into a data frame

Bifurcated the dataset into two dataframes, on the basis of value of target variable , "Hazardous" and then visualised the boundary between the values of different relevant features, taking 2 at a time, using a 2D matplotlib plot
Similarly, visualised the interdependency of features on each other using correlation heatmaps using seaborn heatmaps, the correlation can be used to optimise the training model, the optimisation is not present in this code due to time constraint.

The data was then divided into training and testing data, in a 70:30 ratio,using sklearn.model_selection->train_test_split as specified in the task guidelines, and then it was scaled using sklearn.preprocessing -> StandardScaler.

The SVM model was then trained on this data, for different kernel types, and there accuracy metrics calculate and stored in an array of dictionary

The metrics were then printed in a table-like format for easy comparision between the different kernel types.

Further confusion matrices were plotted, for clear visualisation of predicted vs actual data to establish a thorough comparision between the kernel types

Finally, a ROC curve and a Precision-Recall Curve was plotted for further visualisation.
 
