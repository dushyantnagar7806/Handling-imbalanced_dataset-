
# How to Handle Class Imbalance?

Handling class imbalance can improve the performance and robustness of machine learning models, and ensure that they generalize well to new data. It can also lead to more accurate and meaningful evaluation metrics that reflect the true performance of the model in each class.

- There are numerous techniques to handle class imbalance.

1. Undersampling
2. Oversampling (SMOTE)
3. Ensemble Method
4. Class Weights
5. Focal Loss

## 1. Undersampling 
We reduce the number of samples from the majority class to balance the class distribution in the training data.

![image](https://github.com/dushyantnagar7806/Handling-imbalanced_dataset-/assets/109071505/6ad40c30-49a1-404a-adf1-5828a7d03ccd)


It is a simple technique and since we reduce the size of the data that we push into the models, we reduce training time and memory requirements.

On the other hand, throwing away data means that we lose information. This can reduce the overall performance of the model and the quality of generalization.

We can use undersampling if the data (particularly the majority class) contains many redundant samples that do not provide much additional information to the model, and when it is difficult or expensive to collect more samples from the minority class. Additionally, we can use it if the gap between classes is not that deep. We can tune it slightly by removing some samples from the majority class.


## 2. Oversampling (SMOTE)
In the opposite way of undersampling, now we create more duplicates of the minority class. There are various ways to oversample, but the most famous one is called Synthetic Minority Over-sampling Technique (SMOTE).

![image](https://github.com/dushyantnagar7806/Handling-imbalanced_dataset-/assets/109071505/a361ff52-2ae4-43e8-928a-899631a0c6c2)


SMOTE generates synthetic samples for the minority class by interpolating new points between existing ones. For each sample in the minority class, it selects k nearest neighbors from the same class. It then selects one of these k neighbors at random and computes the difference between the feature vector of the original sample and the selected neighbor. It multiplies this difference by a random number between 0 and 1 and adds it to the feature vector of the original sample.

When we use Smote we do not lose information since this method does not remove any sample. It reduces the risk of overfitting because it generates synthetic samples that are not identical to the original samples.

On the other hand, SMOTE generates synthetic samples, which can introduce noise and outliers in the data. If the dataset is large, then applying SMOTE can be costly.

SMOTE is particularly useful when the class imbalance is severe and the minority class is significantly underrepresented. It is also useful when there is limited data available for the minority class, as it can create additional synthetic samples to improve model performance.



## 3. Ensemble Method
Ensemble techniques can be used to improve the classification accuracy of minority classes.

![image](https://github.com/dushyantnagar7806/Handling-imbalanced_dataset-/assets/109071505/74981b86-7ca9-4d9c-987a-8f513a37ff67)


These techniques can improve the performance of a model by reducing overfitting and increasing accuracy. And, they can handle imbalanced data by giving more weight to minority classes.

Using an ensemble technique can be costly and hard to interpret.



