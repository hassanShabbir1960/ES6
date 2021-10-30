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

## Key Findings:
    
    * On days when there is a lot of sending messages then there is a large number of patient, and vice versa, sending messages made the patient reassured that there was someone to make him remember the session, but sometimes there was not sending SMS to a patient, so a large number did not attend the appointment. there are certainly other reasons for not attending, but this was the most common.
    * About 20% of the patients did not show up to the appointments. This is significant, considering the healthcare professionals, who anticipated the patient, and became idled for the next 30 minutes or 1 hour. Overall, a healthcare worker will be idling (not doing anything) 20% of the time, which is not productive from the finance perspective.
    * Age is significant for patients who showed up for their scheduled appointment.
    * Most of our numeric columns have binary values in them i.e 1 or 0. Except for age column.    
    * Our age variable has some erroreneous entries in it. It has some outliers present in it, which 
          are being checked and removed by looking at their standard deviation from the mean value.
    * Missing values in numeric columns are replaced by median and then standardization was 
          applied on them.
    * According to the model's predictions, most of the patients show up on the appointment date.
    * Person with some disbailities miss some of the appointments.
    * The data set is linearly seperable, which means a linear clsssifer can easily predict the boundaries of both classes.
    * Random Forest outperforms other algorithm in most of the cases.
    * AUC - ROC curve is a performance measurement for the classification problems at various threshold settings. ROC is a probability curve and AUC represents the degree or measure of separability. It tells how much the model is capable of distinguishing between classes. The data set is imabalanced, so the models are biased towards the class that has more number of rows.
    * Ensemble model reduces the spread or dispersion of the predictions and model performance is better than any single contributing model. 
    * The following table is giving comparison of all models used :
    
    | Classifier | AUC score | Accuracy |
    | --- | --- | --- |
    | RF | .5 | .79 |
    | DT | .51 | .73 |
    | Linear SVC | .5 | .80 |
    | Rbf SVC | .5 | .80 |
    | RF (With tuned parameters) | .56 | .79 |
    | DT (With tuned parameters) | .60 | .73 |
    | AdaBoost | .50 | .79 |
    | XGboost | .53 | .81 |
    | Blending | .51 | .80 |
    

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
