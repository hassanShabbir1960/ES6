## Project Overview <a name ="overview"> </a>
### The Classification Task
While LendingClub boasted a default rate of 3.39%, a much higher percentage of its loans were categorized as "charged off." This means that the loan was unlikely to be fully paid, and therefore it had been sold to a third-party collections agency. As a potential investor seeking to maximize returns, it would be usueful to predict ahead of time whether a loan would be charged off or not. In this project, we trained classification models using Logistic Regression, Random Forest, and XGBoost to predict charge-off status. 

### Dataset Description

The dataset we used contains over 2 million loans, with over 150 variables, spanning 2012 through 2018. A link to the dataset can be downloaded [here](https://www.kaggle.com/wordsforthewise/lending-club), and the official data dictionary for it can be downloaded [here](https://resources.lendingclub.com/LCDataDictionary.xlsx).

LendingClub periodically released its loan information on their website, but has since discontinued the practice. We used the most comprehensive LendingClub dataset we could find, which was scraped from the LendingClub website, agglomerated, and made available on [Kaggle](https://www.kaggle.com/wordsforthewise/lending-club). The dataset was described as loans from 2007 to 2018, but we only found loans from 2012 to 2018. Although LendingClub no longer provides support for its dataset online, we found a [data dictionary](https://resources.lendingclub.com/LCDataDictionary.xlsx) on their website that describes each of the variables.


### Purpose
The full dataset was only available for accepted loans, so we could only build models on loans that were accepted by LendingClub. We should clarify that this is a very different task than if we could build models on all loan applications. For the latter, it would be much easier to distinguish between good and bad loans, and such a classifier would be used as a primary filter, for example by LendingClub itself. What we have instead, is to build models classifying on the "good" loans that LendingClub deemed worthy of acceptance. This is a much harder task, so we expect performance to be much worse. A potential use would be, for example, as a secondary filter deployed by one of LendingClub's peer investors seeking any additional edge (over picking at random) to maximize their returns. 

