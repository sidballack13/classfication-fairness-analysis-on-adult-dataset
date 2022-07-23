## Classification and Fairness Analaysis on Adult Dataset

### Overview:

The objectives are as follows:
- Implement a classification task
- Diagnose the fairness properties of the classifiers
- Test few mitigation strategies

### Detailed Description:

We will use the Adults data set that contains census-based features.
The label to predict is whether an individual makes over 50K.
There are 3 parts in this assignment:

#### Part 1: Classification

The data has 13 features and one outcome. There are 32561 data points. The obiective is
to develop a classifier to predict whether an individual makes over 50K. Your classifier
should return 1 if an individual makes more than 50K and O otherwise.
For evaluation purposes (Leaderboard Ranking) we will use the simple accuracy metric
comparing the predictions submitted by you on the test set with the ground truth. Some
things to note:

Here are few guidelines that should help in developing a high accuracy classifier
Think on how vou encode and normalize the data
Explore different classes of classifiers (decision trees, random forest, boosted
classifiers, SVM, logistic regression, KNN...)
For each method that you explore, explain how you choose its hyper-parameter
In your report, show for each method you explore what is the best accuracy and
f1-score you obtain.You can use any library of your choice.

#### Part 2: Fairness Diagnosis
For each of the classifiers presented in part 1, report their demographic disparity,
inequality of odds and opportunity for two sensitive attributes: gender and race. Conclude
on the fairness properties of the various classifiers vou explore in part 1 and the likely
sources of biases.
For this part, you need to write your own functions to compute the three fairness metrics.

#### Part 3: Fairness Mitigation
For your state-of-the-art classifier in part 1 (best accuracy), try the following mitigation
strategies:
- Remove the sensitive attribute from the features
- Identify the attributes that correlate the most with the sensitive attribute and remove them from the features. Remove also the sensitive attribute.
- For both strategies, report the new accuracy, F1-score, demographic disparity, equality of
odds and opportunity. Comment on whether the mitigation strategies reduce unfair outcomes (why? why not?); and, whether you observe an accuracy-fairness trade-off.