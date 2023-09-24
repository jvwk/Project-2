# Project 2 Part 4
## *Jaco van Wyk*

------------

**Source of data**

>  https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset

<br>

**Brief description of data**

>According to the World Health Organization (WHO) stroke is the 2nd leading cause of death globally, responsible for approximately 11% of total deaths.
>
>This dataset is used to predict whether a patient is likely to get stroke based on the input parameters like gender, age, various diseases, and smoking status. Each row in the data provides relavant information about the patient.

<br>

**Target**

>*stroke* is the target: 1 if the patient had a stroke or 0 if not
>

**Initial insights**
>The age distribution of stroke victims' ages is weighted towards older ages, while the age distribution of those who did not suffer strokes are far more evenly spread across the age range.

![age versus stroke](https://github.com/jvwk/Project-2/assets/138116044/e0888207-0b65-4fd7-a2a4-fee6bf946575)


>A larger potion of hypertensive patients fell victim to stroke than of non-hypertensive patients

![hypertension versus stroke](https://github.com/jvwk/Project-2/assets/138116044/64d8bbbd-73b9-494f-8614-f9f5520d2fe4)


**Model, description and recommendataions**

>The model is used to predict whether a person is at risk of suffering a stroke. The relative importance of high precision (avoiding false positives) and high recall (avoiding false negatives) depends on the actions taken when a person is identified as "at risk". Assuming at-risk individuals will not be subjected harsh and/or costly medical treatments, but rather advised to make health-seeking lifestyle changes (eg healthier diet, more exercise, smoking cessation, etc), recall is of relatively more importance:
- a false positive may lead to undesired alarm in a person that may not be at high risk, but possibly motivating him/her making lifestyle changes
- a false negative may lull a person into a false sense of security in terms of stroke risk, and no motivation to make lifestyle changes

>If false positives may lead to harsh or costly medical treatments, it may be advisable to consider the f1-score instead. This metric combines measures for  false negatives and false positives.

>Of all the models tested, the logistic regression classifier with PCA provided the best value for the recall measure on test data for being at risk for a stroke (0.84). The logistic regression without PCA >provided almost as good a value (0.83).

>The other models performed very pootly when considering the recall measure.

>The logistic regression classifier performed poorly when considering false positives. If the consequences of raising a false alarm is more serious than advising (at no substantial fnancial cost) serious >lifestyle changes to those classified as at-risk, other metrics need to pay a more significant role in evaluation of the models.
