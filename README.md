# Adversarial_Learning_Classifier
This model uses adversarial learning techniques to predict income and achieve equality of odds concerning the protected variable of sex, based on the paper 'Mitigating Unwanted Biases with Adversarial Learning' by Zhang et al. The main difference between the paper and this code is that this code uses the second to last output layer from the classifier to feed as input into the adversary, while the paper uses the last layer. The results compare a biased classifier trained without an adversary, against a debiased model trained with an adversary. Results show that the debiased classifier and adversary both achieve equality of odds regarding the protected variable.

Dataset:
https://archive.ics.uci.edu/ml/datasets/Adult

Testing: 
The code can be compiled and run in Google Colab. Number of epochs can be modified in main. 

Results:
The accuracy and confusion matrices of the biased classifier and adversary are compared to the unbiased classifier and adversary:

References:
https://dl.acm.org/doi/pdf/10.1145/3278721.3278779
https://learn.microsoft.com/en-us/windows/ai/windows-ml/tutorials/pytorch-analysis-data

