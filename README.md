## Project Overview <a name ="overview"> </a>
### The Classification Task

This classication task is focused on the question of whether or not patients show up for their appointment. The main qeustion we are trying to answer is if we can sucessfully predict whether a patient will show up on the appointment date. In this project, we trained classification models using DecisionTree, a RandomForest, a linear SVM , an SVM with a radial basis kernel , AdaBoost, XGBoost and blending models to predict the target variable. 

### Dataset Description

The dataset we used contains 110.527 medical appointments its 14 associated variables (characteristics). The most important one if the patient show-up or no-show to the appointment. A link to the dataset can be downloaded [here](https://www.kaggle.com/joniarroba/noshowappointments)
This data for a group of patients contain variables such as Gender, ScheduledDay, AppointmentDay, Age, Neighbourhood, Scholarship , Hipertension, Diabetes, Alcoholism, Handcap, SMS_received, No-show A person makes a doctor appointment, receives all the instructions and no-show. 

### Purpose

In this project we investigate a data set of appoinment records in public hospitals in Vitoria, Espirito Santo, Brazil. The data includes whether the patient showed up to the appointment, which is the main focus, as well as other attributes of the patient and the appointment. Our aim is to help to answer the question, "how likely is a patient with certain attributes, to show up to his hospital appointment?" We will explore the data and look for relationships between variables, to pave the way for more extensive modeling.


## Approach used <a name ="overview"> </a>


    The notebook in the repository contains the whole process of creating and comparing machine learning classifieres to classify the health records from input. We will be starting off with the data visualization, then we will preprocess the text annd then we will move for model training, tuning, the comparision between different models and then finally we will save our model in the disk for making predictions in future.
    
    Here are the steps that we have followed to achieve the work that needs to be done:
    
    1. Dataset loading and pre-processing:

       We started off with reading data set , checked out for the outliers and the missing values in our data set.

    2. Data visualization:

       We then did some data visualization that includes showing the data distribution, nature of the data set.
    
    
    3.Training ,comparing the models performance:
    
       For the evaluation of the classifier built we used the metric accuracy that was tested on differnt folds using k-fold cross validation. And then we plot the  confusion matrix and an accuracy plot.
    
    4. Fine tuning and saving the model:
    
       We then fine tuned our models and compared their performances with other models.
    
    5. Training ensemble models:
    
       After this we trained ensemble models as they make better predictions and achieve better performance than any single contributing model.  


## Key findings <a name ="overview"> </a>
and bad loans, and such a classifier would be used as a primary filter, for example by LendingClub itself. What we have instead, is to build models classifying on 


## Running the code <a name ="overview"> </a>
###  how to reproduce the results
such a class

#### Data processing
such a class

#### Classification models
such a class

#### Hyper parameter tuning
such a class

#### Ensemble models
such a class


## Conclusion and discussion <a name ="overview"> </a>
such a class
