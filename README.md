# Absenteeism-Logistic-Regression-Model
The target is to develop a model that will predict the probability of an individual being excessively absent from work.
The data set consists of information about employees of a company and some information about their characteristics and life.
Like their age, body mass index, the number of children and pets, etc.
## Preprpcessong:

### "Reason for Absence" column:
consist of 28 different reasons which could be categorized into 5 groups.
group 1 represents absence because of illness.
group 2 represents absence because of pregnancy.
group 3 represents absence because of Poisoning.
group 4 represents absence because of light reasons (like visiting a doctor).
group 5 represents absence without any specific reason.
then I converted them into dummy variables.

### "Date" column:
I extracted the number of weekdays and months from these columns to see if it could be important for the final model.

### "Education" column:
by taking a look at it, I find out that almost 65% of de employees have the first level of education (high school) so I divided them into 2 groups. Group 0: high-school level and Group 1: the rest.

### "Absenteeism Time in Hours" column:
Which is the target column. by doing some statistics it will be clear that the median of absence time is equal to 3 hours. So, I split them into 2 groups with Low probability of absence = 0 and a High probability of absence with label 1.
The goal of this model would be to classify employees into one of these groups.

### The rest of the columns:
They remain unchanged because they are not categorical.
I just standardized the rest of the columns using a standard scaler from sklearn library.

### Model:
A logistic regression model is used in this case and 20 percent of the data are used as testing the model. 
The accuracy of the model is almost 78%
The prediction accuracy (on the test sample) is 74%
