# Bank Marketing

## Project Background
This project aims to build and compare two classification models for bank marketing data. The project uses a data mining approach to predict the customer response rate for a term deposit scheme.

## Methodology
This project uses the CRISP-DM methodology to guide the data mining project. \

### Dataset and Preparation
 The dataset used in this project is a bank marketing application created by Paulo Cortez and Sérgio Moro in 2012, retrieved from the UCI Machine Learning Repository. \
 It contains 41,188 instances and 21 attributes, including the client's demographics and socio-economic spectrum. \
 The dataset is imbalanced, with the number of clients subscribed to term deposit being almost 8 times less than the number of clients who did not subscribe. \
 The data was explored and cleaned, with unknown data being replaced or dropped, and redundant data being removed. \
 Categorical data was transformed into numerical data using one-hot encoding. \
 The dataset was then split into train and test datasets with a ratio of 7:3.

### Machine Learning Algorithms
Two supervised learning algorithms, Decision Tree and Naïve Bayes, are investigated and compared in terms of their performance to classify the dataset correctly.

#### Decision Tree
Decision Tree is a non-parametric algorithm that builds a tree-like structure of rules based on the features of the data. It uses splitting criteria such as gini index or entropy to measure the quality of a split. It can avoid overfitting by pruning the tree.
#### Naïve Bayes
Naïve Bayes is a parametric algorithm that applies the Bayes theorem to compute the posterior probability of a class given the features. It assumes that the features are conditionally independent given the class. It can handle categorical and numerical data.

### Parameter Tuning
Decision Tree classifier, the parameters evaluated were the splitting criterion, maximum depth of the tree, and the minimum number of samples required to be at a leaf node. \\
For the Naïve Bayes classifier, the parameters evaluated were alpha and binarize. \
The best combination of parameters was determined using GridSearchCV from the sklearn.model_selection module. \
A 10-fold cross-validation was performed during the GridSearchCV on the train dataset. \
The best combination of parameters that provided the highest F1 score was selected for the configuration of the Decision Tree and Naïve Bayes models.

## Experiment Analysis
The results show that Decision Tree achieved a higher F1-score (0.603) and accuracy (0.912) than Naïve Bayes (0.417 and 0.875 respectively) on the test data. The results also indicate that the data set is highly imbalanced, as the majority class of "no" is much more frequent than the minority class of "yes". The results suggest that Decision Tree is more suitable for the data set than Naïve Bayes, as it can better handle the imbalance and the categorical features.

## Conclusion
The evaluation results proved that Decision Tree is a better classifier compared to Naïve Bayes.
