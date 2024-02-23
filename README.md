Gender_Classifier.py
This program is a simple gender classification algorithm based on the features of human names and their gender names.
This script contains a simple Naive Bayes classifier for gender prediction based on personal names. The model is trained and tested on a list of names obtained from a text file (name_list.txt). The feature sets are extracted from the names and used for training and testing the classifier. The trained classifier can predict the gender of a given name.

Usage:

Prepare a text file (name_list.txt) with names and their corresponding genders, separated by a comma. For example:
John,M Jane,F Porimol,M Chandro,F

Run the script:
python GenderClassifier.py

The script will train the classifier and print the accuracy.

To predict the gender of a name, call the gender_classifier method with the name as an argument:

gcf = GenderClassifier() gcf.model_train() print(gcf.gender_classifier('Porimol Chandro'))

To display the most informative features, call the informative_features method with the number of features to display:
print(gcf.informative_features(25))

Description
1.gender_features(self, name): Extracts features from a given name.

2.data_sets(self): Reads the raw data from the name_list.txt file and returns a list of tuples (name, gender).

3.feature_set(self): Shuffles the feature data sets and returns the shuffled list.

4.model_train(self, percent_to_train=0.70): Trains the Naive Bayes classifier with the given training data set and prints the accuracy.

5.informative_features(self, num_of_feature=25): Displays the most informative features based on the chi-squared statistic.

6.gender_classifier(self, name=None): Predicts the gender of a given name and returns the result as a string.

******************************************************************
Dependencies
Python 3.x
NLTK (Natural Language Toolkit)
Scikit-learn (for shuffle function)
Install dependencies:

pip install nltk scikit-learn

Note
This is a simple implementation for educational purposes. The accuracy and performance may not be suitable for real-world applications.