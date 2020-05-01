---
date: "5/1/2020"
---

# Cleaning Samsumg Weareable Data

To fully understand, it is necessary to **read the information contained in the raw dataset**.
It can be seen [here](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones).

The process followed had to **answer this questions**: 

1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement.
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive variable names.
5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

## 1. Merging

The process to merged passed first by merging separatately data sets (train and test), and after that merging them together. 

First of all it was needed to **add columns to identify our observations by the subject who did them and by the kind of activity that was doing**. So two columns were added to the Xtrain.txt. The first was the subject_train.txt, named as subject, which states the subject who did the observation, and the second added was from ytrain.txt, named as label, which indicates the kind of activity he was doing. 

The same is done to the test data.

Now, we **append the test data to the train data, and order them by the first column** (by the subject). We have the complete data set with the 30 subjects of the experiment.

## 2. Mean and standard deviation

Simple process to just **select the columns containing either 'mean' or 'std'**, and our first two columns that identify our observations by subject and activity.

## 3. Descriptive activity names

**Change the numbers in the 'label' column** by the names given in the 'features.txt' file.

## 4. Variable names

**Change the names by their characteristics.** For example, changing 't' by 'time' and so on. More information about tha variable names in the file 'variableDoc'

## 5. Independent data set

Taking the tidy data set from the previous step, just **change the data to be presented by the 'label' column**, as a per unit basis. That is, each row represents one observation of a wereable characteristic from one person doing one activity. 

Then, **change that to be presented each row one person, a whole activity and one weareable characteristic.**

That data set is the tidy data set, named 'finalDT.txt'
