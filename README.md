# Adversarial_Learning_Classifier
This model uses adversarial learning techniques to predict income and achieve equality of odds concerning the protected variable of sex, based on the paper 'Mitigating Unwanted Biases with Adversarial Learning' by Zhang et al. The main difference between the paper and this code is that this code uses the second to last output layer from the classifier to feed as input into the adversary, while the paper uses the last layer. The results compare a biased classifier trained without an adversary, against a debiased model trained with an adversary. Results show that the debiased classifier and adversary both achieve equality of odds regarding the protected variable.

### Dataset:
https://archive.ics.uci.edu/ml/datasets/Adult

### Testing:
The code can be compiled and run in Google Colab. Number of epochs can be modified in main. 

### Results:
The accuracy and confusion matrices of the biased classifier and adversary are compared to the unbiased classifier and adversary:

#### Biased Classifier Results

Accuracy of the Biased model based on the test set of 9768 x_test is: 83 %

Biased Male Subgroup Confusion Matrix

![image](https://github.com/raniau1353/Adversarial_Learning_Classifier/assets/116512493/bd175421-5f13-4404-9201-0955d133eefd)

Biased Female Subgroup Confusion Matrix

![image](https://github.com/raniau1353/Adversarial_Learning_Classifier/assets/116512493/355ffdd5-1abb-45e8-a43d-739c1477644e)

Biased Adversary correctly predicting Male: 87 % | Biased Adversary correctly predicting Female: 73 %

Biased Adversary incorrectly predicting Male: 12 % | Biased Adversary incorrectly predicting Female: 26 %

Biased Classifier False Positive income prediction on Male subgroup: 0.0840 | Biased Classifier False Positive income prediction on Female subgroup: 0.0420 

Biased Classifier False Negative income prediction on Male subgroup: 0.4647 | Biased Classifier False Negative income prediction on Female subgroup: 0.5443 

#### Debiased Classifer Results

Accuracy of the Unbiased model based on the test set of 9768 x_test is: 84 %

Debiased Male Subgroup Confusion Matrix

![image](https://github.com/raniau1353/Adversarial_Learning_Classifier/assets/116512493/c7df71c1-7615-421f-96a6-36561d4678f3)

Debiased Female Subgroup Confusion Matrix

![image](https://github.com/raniau1353/Adversarial_Learning_Classifier/assets/116512493/f9d3d46f-4eb9-4eea-80cb-d2882fde4556)

Debiased Adversary correctly predicting Male: 99 % | Debiased Adversary correctly predicting Female:  0 %

Debiased Adversary incorrectly predicting Male:  0 % | Debiased Adversary incorrectly predicting Female: 99 %

Debiased Classifier False Positive income prediction on Male subgroup: 0.0980 | Debiased Classifier False Positive income prediction on Female subgroup: 0.0743 

Debiased Classifier False Negative income prediction on Male subgroup: 0.3811 | Debiased Classifier False Negative income prediction on Female subgroup: 0.3386

### References:

https://dl.acm.org/doi/pdf/10.1145/3278721.3278779

https://learn.microsoft.com/en-us/windows/ai/windows-ml/tutorials/pytorch-analysis-data

