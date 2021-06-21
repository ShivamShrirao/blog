# Stats Basics
> Just some basic stats concepts for quick revision.

- toc: true 
- comments: true
- hide: false
- image: images/stats/high_bias.png

# Cross Validation

- Split the training data into multiple folds, eg. Four folds of 25% each.
- For each fold as testing, and rest as training train a model each time.
- Do same with different models. Choose the one which gets the most folds correct.

# Sensitivity & Specificity

- **Sensitivity**: Percentage of positives correctly identified. (True Positive rate)
    - Eg.: Percentage of patients correctly identified to have a disease among all actually having disease.
    - Sensitivity = $\frac{TP}{TP+FN}$


- **Specificity**: Percentage of negatives correctly identified. (True Negative rate)
    - Eg.: Percentage of patients correctly identified to NOT have a disease among all actually NOT having disease.
    - Specificity = $\frac{TN}{TN+FP}$


|                   | Real Has | Real Not Has |
|-------------------|----------|--------------|
| Predicted Has     |    TP    |      FP      |
| Predicted Not Has | FN       | TN           |

# Precision & Recall

- **Precision**: Proportion of positives correctly identified.
    - Eg.: Number of patients actually having the disease among all prediicted to be having the disease.
    - Precision = $\frac{TP}{TP+FP}$


- **Recall** = [Sensitivity](#Sensitivity-&-Specificity).

# Bias & Variance

- **Bias**: "Prior assumptions" in model/algorithm preventing it to fit on data.
    - Eg: Linear regression will be a straight line so can't fit on curved data, therefore it has high bias and low variance.
    ![](images/stats/high_bias.png "https://youtu.be/EuBBz3bI-aA")  
        *Image Credit: [Machine Learning Fundamentals: Bias and Variance](https://youtu.be/EuBBz3bI-aA)*


- **Variance**: Model/algorithm is can "vary" itself alot and thus can overfit on data.
    - Eg: Lot of curves going exactly through all data points, model won't generalize, therefore it has high variance and low bias.
    ![](images/stats/high_variance.png "https://youtu.be/EuBBz3bI-aA")  
        *Image Credit: [Machine Learning Fundamentals: Bias and Variance](https://youtu.be/EuBBz3bI-aA)*


- **Bias Variance Tradeoff**: We gotta find a good comprise among the two to find best model. 


**Intersting Fact**: Check out double descent in deep learning, highly over-parameterized models can at first overfit, perform worse but then start to perform better again.  
An intuitive possible explanation: https://twitter.com/daniela_witten/status/1292293102103748609

# ROC & AUC

- __Receiver Operator Characterstic (ROC)__: Plot True Positive Rate vs False Positive Rate of model for different classification thresholds.  
    - Decide what works better for you, if you want classify positives more correctly and some false positives,
    - OR lesser true positives for no false positives.  
    ![](images/stats/roc.png "https://youtu.be/4jRBRDbJemM")  
        *Image Credit: [ROC and AUC, Clearly Explained!](https://youtu.be/4jRBRDbJemM)*


- __Area Under Curve (AUC)__: Compare ROC graphs.  
    - Graph with higher area better.  
    - False positive rate can often be replaced with Precision.  
    ![](images/stats/auc.png "https://youtu.be/4jRBRDbJemM")  
        *Image Credit: [ROC and AUC, Clearly Explained!](https://youtu.be/4jRBRDbJemM)*


# Residuals
- __Residuals__ : Vertical distance of data point from line.
- __R squared__ : $\large1 -\frac{\text{Sum of squares of Residuals}}{\text{Total sum of squares(variance)}}$.  
0 -> Worst, 1 -> Best.

$log(odds) = log(\frac{p}{1-p})$

# Logistic Regression

Probability between 0 and 1.
Convert to log(odds) on y axis to compare to linear regression.

- __Uses Maximum Likelihood__: Log adds for datapoints converted to probability.  
- __Log Likelihood__: Sum of logs of probabilities or multiplication of probabilities.  
![](images/stats/logistic_likelihood.png "https://youtu.be/BfKanl1aSG0")  
    *Image Credit: [Logistic Regression Details Pt 2: Maximum Likelihood](https://youtu.be/BfKanl1aSG0)*

# Ridge (L2) Regularization

- Test


```python

```
