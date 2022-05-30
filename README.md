# Brain Tumor Radiogenomic Classification

Welcome to **Brain Tumor Radiogenomic Classification** project!

## Contributors
[Khrystyna Kokolus](https://github.com/khristinakokolus)

[Yaroslav Prytula](https://github.com/SlavkoPrytula)

## Description

This project aims to predict the percent of MGMT factor in brain MRI.




# Evaluation

The results are evaluated on the area under the ROC curve between the predicted probability and the observed target

An ROC curve (receiver operating characteristic curve) is a graph showing the performance of a classification model at all classification thresholds

This curve plots two parameters:
- True Positive Rate
- False Positive Rate


## True Positive Rate
True Positive Rate (TPR) is a synonym for recall and is therefore defined as follows
(proportion of samples that were correctly classified)

<img width="179" alt="image" src="https://user-images.githubusercontent.com/25413268/171037897-f6234f61-4fb1-404e-aa6a-3e85a417157a.png">


## False Positive Rate (FPR) is defined as follows

<img width="179" alt="image" src="https://user-images.githubusercontent.com/25413268/171037918-1ae6fd84-812a-4533-a525-4f0bd6f4a80c.png">

## Resulting Aggregated Metric 

<img width="768" alt="image" src="https://user-images.githubusercontent.com/25413268/171038007-4ddc426b-c403-4456-b5f1-384d6b046c14.png">
<img width="768" alt="image" src="https://user-images.githubusercontent.com/25413268/171038039-19281a9a-e73e-4d27-9aaa-c771f63e2b4c.png">




# ML vs DL

The 3D CNN preserve temporal information and propagate it through the layers of the network. The tensor zi is in this case 4D and has size Ni × D × Hi × Wi, where Ni is the number of filters used in the i-th block. Each filter is 4-dimensional and it has size Ni−1 × t × d × d where t denotes the temporal extent of the filter. The filters are convolved in 3D, over space dimension

Where in the 2D case this informations is lost


The compared results for the [Baseline] Regression Classifier and 3D ResNet are prominent. The 3D ResNet's performance is much better for evry single scan type

<img width="768" alt="image" src="https://user-images.githubusercontent.com/25413268/171038664-c7bc4207-8027-410e-91ba-20fbba2b0d93.png">




# Conclusions

3D CNN showed better results compared to 2D classifier
- big dataset
- filters are convolved in 3D over space dimension

Improved score with “vanilla” residual blocks
