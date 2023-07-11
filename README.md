Read me



# BA Thesis - Code Implementation

This folder contains the implementation of the created animacy classifiers A and B and the co-training algorithm.
> **Important**: Since many files were larger than 25 MB it was not possible to store them on GitHub. If you want to run the code and a file is required which is for some reason not working here, refer to the USB stick to run the code. 

### Structure

1. Classifier A
2. Classifier B
3. CoTraining
4. Klenner&Göhring
5. Test_Set
6. Preperation_Of_Classifiers

> **NOTE**: Preperation_Of_Classifiers might not be runnable since it was performed on an older Mac OS system. I switched to Windows during the implementation and only used the prepared and pre-processed data.

#### 1. Classifier A
> Contains the implementation of BERT for token classification model

- **requirements.txt** contains the required packages and libraries
- **BaselineClassifierA.ipynb** contains the implementation of the classifier A
- **trainDfA.csv** contains the training data
- **validDfA.csv** contains the validation data
- **bert-base-german-token-classification** contains the trained model

#### 2. Classifier B
> Contains the implementation of BERT for sequence classification model

- **requirements.txt** contains the required packages and libraries
- **BaselineClassifierB.ipynb** contains the implementation of the classifier B
- **trainDfClassifierB.csv** contains the training data
- **validDfClassifierB.csv** contains the validation data
- **BERT_Model** contains the trained model

#### 3. CoTraining
> Contains the implementation of co-training algorithm on both classifiers

- **requirements.txt** contains the required packages and libraries
- **CoTrainingsImplementation.ipynb** is the main part of this thesis and stores both classifiers A and B and the co-training algorithm
- **bert-base-german-token-classification** is the saved model for classifier A
- **labeledData.csv** contains the manually labeled data
- **trainData.csv** contains 80% of the labeledData.csv file (randomly selected)
- **validData.csv** contains 20% of the labeledData.csv file (randomly selected)
- **unlabeledData.csv** contains the unlabeled data (needed for co-training)

#### 4. Klenner&Göhring
> Contains the implementation of classifier based on Klenner and Göhring´s dictionaries

- **requirements.txt** contains the required packages and libraries
- **gold_actor**, **gold_direct** and **gold_nonactor** are the dictionaries from Klenner and Göhring
- **confusion_matrix** depicts the confusion matrix of the classifier
- **metrics** depict the metrics of the classifier
- **validation_data.csv** contains the validation data from the original files of the speeches
- **originalFiles** should contain all the files from the German Bundestag (In order to reduce size, the folder is empty. If you want to execute the code, you would need to put the data in here)

#### 5. Test_Set
> Contains the implementation of a test set out of domain (on news from Tagesschau.de)

- **requirements.txt** contains the required packages and libraries
- **TestData.ipynb** contains the notebook for the test data set 
- **Feedparser.ipynb** contains the notebook for parsing the data from tagesschau.de
- **testSetData.csv** contains the manually labeled test data
- **testSetPredictionsAndTrueLabels.csv** contains the manually labeled data with the predictions of both classifiers A and B
- **trainData.csv** contains the training data for both classifiers (80%)
- **validData.csv** contains the validation data for both classifiers (20%)

#### 6. Preperation_Of_Classifiers
> Contains the implementation of pre-processing both classifiers

- **Pre-processing of Data.ipynb** contains all methods how the data was prepared for both classifiers
- **originalFiles** should contain all the files from the German Bundestag (In order to reduce size, the folder is empty. If you want to execute the code, you would need to put the data in here)
- **newRandomTSVFiles** contains the 100 randomly selected files for classifier A
- **labeledDataClassifierA** contains the manually labeled data and gets split up into animatedValidationData and animatedTrainData
- **CoNLL Format** contains the files for classifier B in CoNNL2000 format 
- **IOB Format** contains the files for classifier B in the IOB scheme
