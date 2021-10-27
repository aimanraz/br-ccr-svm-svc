# Breast Cancer Detection using Support Vector Machine.
Classify tumors malignant or benign based on several observation/features. Early diagnose could increase the chances of survival.

## Problem Statement
Fine needle aspirate (FNA) is process extracting cell from tumor of the patient. Once extracted, images of tumor is produced for observation and to collect more data about the tumor. Feature of the tumor extracted from the images such as radius, perimeter, fractal dimension and etc. This feature can be served as the independent variable of machine learning input to predict whether the tumors is malignant or benign. 

## Code and Resources Used 
**Python Version:** 3.8++

**Packages:** pandas, numpy, sklearn, matplotlib, and seaborn.

## Data collection and description
The dataset imported from sklearn.dataset libraries or can be download at [UCI Machine learning](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic)). Datasets are linearly separable using all 30 input features. Consist of 569 number of instances with a class distribution of212 Malignant, 357 Benign. The target class are Malignant(0) and Benign(1). 30 features are used, examples:

* radius (mean of distances from center to points on the perimeter)
* texture (standard deviation of gray-scale values)
* perimeter
* area
* smoothness (local variation in radius lengths)
* compactness (perimeter^2 / area - 1.0)
* concavity (severity of concave portions of the contour)
* concave points (number of concave portions of the contour)
* symmetry 
* fractal dimension ("coastline approximation" - 1)

## Data Preprocessing
Feature normalization technique was applied to the features to reduce the scale from 0 to 1. This method increased the accuracy of the machine learning model. 

## Visualization
Visualizing the correlation between all features.

![Pairplot](https://github.com/aimanraz/br-ccr-svm-svc/blob/main/img/viz.png)

![Correlation](https://github.com/aimanraz/br-ccr-svm-svc/blob/main/img/heatamap_corr.png)


## Support Vector Machine
By using GridSearchCV method, below are the best parameter used for this case  studies:
* C : 1
* gamma : 0.7
* kernel : rbf(radial basis function)

## Model performance
The confusion matrix of the model with the final accuracy of 97.368 %

![Confusion matrix](https://github.com/aimanraz/br-ccr-svm-svc/blob/main/img/cm.png)

## Conclusion

* SVM machine learning model was able to classify tumors (Benign/Malignant) with 97% accuracy.
* This model can rapidly evaluate breast masses and classify them in an automated fashion.
* By early diagnose this cancer, it can dramatically save lives in the developing world.

## Futher improvement

By combining Computer vision/Machine learning techniques to directly classify the cancer tissue images.

let the data drive you...and beyond.
