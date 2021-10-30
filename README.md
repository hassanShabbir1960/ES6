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
###  How to reproduce the results
The project is basically divided into three parts , the code of all those parts is concatenated in a single jupyter notebook file, and markdown headings are used
to indicate the start and end of each part. 

To ensure the reproduceability in our results, we have set the random state to a fixed number. When random_state is set to an integer, functions will return same results for each execution. when random_state set to an None, functions will return different results for each execution. 

To run the notebook successfully, one has to first install libraries that are being used in the notebook. And to install them, the following command will be used:
pip install -r requirements.txt

And then open the jupyter notebook, click on kernel-> Run all the cells.

Here is the brief description of the steps being followed in each part:

#### Part 1:

<ul> This includes: </ul>

<li>Reading in data csv file </li>

<li>Cleanup data column names </li>

<li>Removed records with erroneous entries (e.g., negative ages, look at what people have done in Kaggle) </li>

<li>Created a test set of 20k records that you won’t touch again for the reminder of this project until Part III. Use stratified sampling on the No-show variable to ensure test set and training set class proportions are the same. Save the train and test sets as csv files in the processed_data directory. </li>

<li>Plotted the No-show variable against the other variables in the dataset as part of Exploratory Data Analysis </li>

<li>Created a preprocessing pipeline using scikit to prepare the data for the ML algorithms we will use. At a minimum, standardize numerical variables, transform categorical variables into one or more numerical values. You may apply other transformations that you think would be useful (e.g., logarithmic transformations).</li>





#### Part 2:

<ul>  Here are the steps involved in this part </ul>  

<li> Using sklearn fit a DecisionTree, a RandomForest, a linear SVM and an SVM with a radial basis kernel to the transformed data. For now, use default parameters for each method. </li>

<li> Use 10 fold cross validation to estimate performance of each of the above methods using both accuracy and AUC as metrics. </li>

<li> Based on the above choose two of the ML methods and fit a model using 5 fold cross validation for model selection and 10 fold cross validation for model assessment. </li>

<li> Implemented gradient descent for a linear svm and test it on the training set. </li>


#### Part 3:

<ul>  Here are the steps involved in this part </ul>  

<li>Trained an AdaBoost classifier and compare its performance to the results obtained in Part II using 10 fold cross validation as before </li>

<li>Trained an xgBoost classifier and compare its performance to the results obtained in Part II </li>

<li>Chose a set of 5 or so classifiers, e.g., Decision Trees of diverse depths, linear SVMs over diverse subsets of features, RBF kernels with diverse bandwidths, Random Forests with diverse number of trees in their ensemble, be creative!. Write a function that given a training set does the following: </li>

        Created a validation set using 20% of the training set
        Trained each of your chosen classifiers on the training set
        Using the validation set created a new dataset where features are predictions made by each of your chosen classifiers
        Trained a logistic regression classifier to blend the predictions



## Conclusion and discussion <a name ="overview"> </a>

