# Lead-Score-Model
## About the Problem:
Selling something is not an easy task. A business might have many potential customers, commonly referred as leads, but not enough resources to cater them all. Even most of the leads won’t turn into actual bookings. So there is a need for a system that prioritises the leads, and sorts them on the basis of a score, referred to here as lead score. So whenever a new lead is generated, this system analyses the features of the lead and gives it a score that correlates with chances of it being converted into booking. Such ranking of potential customers not only helps in saving time but also helps in increasing the conversion rate by letting the sales team figure out what leads to spend time on.

Here you have a dataset of leads with their set of features and their status. You have to build a ML model that predicts the lead score as an OUTPUT on the basis of the INPUT set of features. This lead score will range from 0-100, so more the lead score means more chances of conversion of lead to WON.

NOTE: The leads with STATUS other than ‘WON’ or ‘LOST’ can be dropped during training.

NOTE: Treat all columns as CATEGORICAL columns

NOTE: This '9b2d5b4678781e53038e91ea5324530a03f27dc1d0e5f6c9bc9d493a23be9de0' represents NaN and could be present in more than one column.

## Brief Overview of Lead Scoring Model
The task is to build a lead scoring model on a given dataset. This is a binary
classification problem. As we had to predict lead score, that can be done by
classifying status and then converting it into probability of status and then
converting that probability to lead score.

For this the dataset can be split into training and testing data and then the model
is trained by using RFE in which the estimator is a random forest classifier. Then,
to evaluate the performance of the model using metrics like accuracy, precision,
recall. A classification report can be generated to further analyze the
performance of the model on the testing data.

To built this we follow these steps:
1. Data Cleaning:

● Taking care of nan values, we drop those columns that have more than
15% of nan values and then deal with the other nan values.

● Dropping the duplicates values.

2. Data Preparation:

● Converting categorical data into numerical data by creating dummy
variables.

● Splitting the dataset into training and testing, 80% as training and
20% as testing dataset.

3. Model Building:

● This data is highly imbalanced so we had to undersample the majority
class.

● Uses the RFE (Recursive feature Elimination) to select 30 more
relevant features for the target variable.

● And, then we use the Random Forest Classifier as an estimator of
RFE.

● We got an Accuracy of 75.29% on the training dataset.

● Also, calculate the other metrics like precision score, recall score.
