## Project Overview <a name ="overview"> </a>
### The Classification Task

This classication task is focused on the question of whether or not patients show up for their appointment. The main qeustion we are trying to answer is if we can sucessfully predict whether a patient will show up on the appointment date. In this project, we trained classification models using DecisionTree, a RandomForest, a linear SVM , an SVM with a radial basis kernel , AdaBoost, XGBoost and blending models to predict the target variable. 

### Dataset Description

The dataset we used contains 110.527 medical appointments its 14 associated variables (characteristics). The most important one if the patient show-up or no-show to the appointment. A link to the dataset can be downloaded [here](https://www.kaggle.com/joniarroba/noshowappointments)

The data set has the following variables:
01 - PatientId
Identification of a patient
02 - AppointmentID
Identification of each appointment
03 - Gender
Male or Female . Female is the greater proportion, woman takes way more care of they health in comparison to man.
04 - DataMarcacaoConsulta
The day of the actuall appointment, when they have to visit the doctor.
05 - DataAgendamento
The day someone called or registered the appointment, this is before appointment of course.
06 - Age
How old is the patient.
07 - Neighbourhood
Where the appointment takes place.
08 - Scholarship
True of False . Observation, this is a broad topic, consider reading this article https://en.wikipedia.org/wiki/Bolsa_Fam%C3%ADlia
09 - Hipertension
True or False
10 - Diabetes
True or False
Alcoholism
True or False
Handcap
True or False
SMS_received
1 or more messages sent to the patient.
No-show
True or False.


### Purpose
The full dataset was only available for accepted loans, so we could only build models on loans that were accepted by LendingClub. We should clarify that this is a very different task than if we could build models on all loan applications. For the latter, it would be much easier to distinguish between good and bad loans, and such a classifier would be used as a primary filter, for example by LendingClub itself. What we have instead, is to build models classifying on the "good" loans that LendingClub deemed worthy of acceptance. This is a much harder task, so we expect performance to be much worse. A potential use would be, for example, as a secondary filter deployed by one of LendingClub's peer investors seeking any additional edge (over picking at random) to maximize their returns. 



## Approach used <a name ="overview"> </a>
and bad loans, and such a classifier would be used as a primary filter, for example by LendingClub itself. What we have instead, is to build models classifying on 

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
