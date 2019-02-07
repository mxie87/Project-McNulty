The goal of this project was to predict the “types” of crime, given a particular time and location in the city of San Francisco, using machine learning algorithms. The data set is a popular dataset available on Kaggle (https://www.kaggle.com/c/sf-crime). 

Data at a glance:
* SF Crime Data - Kaggle
* 2.215 Million incidents since 2003
* ~150K per year
* ~411 cases per day

The most challenging part about this project was the limited descriptions given for each incident, which required manual labeling to specific the class of crime for each incident description. There were over 900 unique descriptions across 2.2 million incidents. Because these descriptions were vague and subjective, each incident was arbitrarily appended one of 3 classes: 

•	Class 1 – serious & violent crimes / high priority
•	Class 2  - less serious but has a potential to escalate to class 1
•	Class 3 – non-violent / low priority

There was also obvious class imbalances with class 1 and class 2 crimes making up only 25% of the total. SMOTE and ADASYN were used for oversampling. 

The features used were categorical:
	Time of Day:
	Morning - 6am to 12pm
	Afternoon - 12pm to 6pm
	Night - 6pm to 12am
	Late Night - 12 am to 6am
	Day of Week: SMTWTFS
	Police Districts: 10 different districts
 
Classifiers used includes:
	Logistic Regression
	Naïve Bayes
	Gaussian
	Bernoulli
	Multinomial
	Decision Tree
	Random Forest
	Adaboost

Accuracy, Precision, Recall, F-1 score and ROC AUC was used to evaluate the models.  

Random Forest and Adaboost yielded similar and the best results, when class 1 and 2 were combined as 1 classes, giving an accuracy of .55, indicating that the model performed better than random guessing.
