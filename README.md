# Brain Tumor Radiogenomic Classification

Welcome to **Brain Tumor Radiogenomic Classification** project!

[Train model](https://www.kaggle.com/code/slavkoprytula/3d-resnet-train) or
[Use pretrained models](https://www.kaggle.com/datasets/slavkoprytula/rsnabraintumorclassificationmodels)

# Contributors
[Khrystyna Kokolus](https://github.com/khristinakokolus)

[Yaroslav Prytula](https://github.com/SlavkoPrytula)

# Description

The aim of this project is to determine the presence of MGMT factor, which causes the formation of glioblastoma, by MRI scan. This can help in the early stages of a medical examination.


# Pipeline

<img width="330" alt="Screenshot 2022-05-31 at 06 46 38" src="https://user-images.githubusercontent.com/60686300/171088953-73f27acb-edae-4ce1-953b-a32b317cc748.png">

# CNN model view

<img width="554" alt="Screenshot 2022-05-31 at 06 49 10" src="https://user-images.githubusercontent.com/60686300/171089085-22c8251a-c13b-4188-ade7-b95f6ab6668e.png">

# Evaluation

The results are evaluated on the area under the ROC curve between the predicted probability and the observed target

An ROC curve (receiver operating characteristic curve) is a graph showing the performance of a classification model at all classification thresholds

This curve plots two parameters:
- True Positive Rate
- False Positive Rate

----

## True Positive Rate (TPR)
True Positive Rate (TPR) is a synonym for recall and is therefore defined as follows
(proportion of samples that were correctly classified)

<img width="179" alt="image" src="https://user-images.githubusercontent.com/25413268/171037897-f6234f61-4fb1-404e-aa6a-3e85a417157a.png">


## False Positive Rate (FPR) is defined as follows

<img width="179" alt="image" src="https://user-images.githubusercontent.com/25413268/171037918-1ae6fd84-812a-4533-a525-4f0bd6f4a80c.png">

## Resulting Aggregated Metric 

<img width="768" alt="image" src="https://user-images.githubusercontent.com/25413268/171038007-4ddc426b-c403-4456-b5f1-384d6b046c14.png">
<img width="768" alt="image" src="https://user-images.githubusercontent.com/25413268/171052905-391e3223-78ef-4bc3-9ef3-61f4cee264ef.png">




# ML vs DL

The 3D CNN preserve temporal information and propagate it through the layers of the network. The tensor xi in this case is 4D and has size Ni × D × H × W, where Ni is the number of filters used in the i-th block. Each filter is 4-dimensional and it has size Ni−1 × t × d × d where t denotes the temporal extent of the filter. The filters are convolved in 3D, over space dimension

Where in the 2D case this informations is lost

----

The compared results for the [Baseline] Regression Classifier and 3D ResNet are prominent. The 3D ResNet's performance is much better for evry single scan type

<img width="768" alt="image" src="https://user-images.githubusercontent.com/25413268/171038664-c7bc4207-8027-410e-91ba-20fbba2b0d93.png">




# Conclusions

3D CNN showed better results compared to 2D classifier
- big dataset
- filters are convolved in 3D over space dimension

Improved score with “vanilla” residual blocks
