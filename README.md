# Mask-Wearing Face Detection

## Outline
1. Problem Overview
2. Dataset Source
3. Methods
4. Data Processing and Result
5. Interpretation and Evaluation

## Problem Overview
- Covid-19 spreads quickly through droplets.
- Therefor, people must work or do activity using the health protocol. One of them is wearing a mask.
- But the problem is people activities in public area is too fast and too many to observe using CCTV.
- Therefore, the public system should implement AI to observe health protocol every day.
- Machine learning is part of AI that can solve this problem; classify mask-wearing face from an image (computer vision implementation).

## Dataset Source
The dataset contains 3 folders labeled as to which class they belong to. The 3 classes are "with_mask", "withou_mask", and "mask_weared_incorrect". Each folder holds 2994 images of people that belong to such a labeled class.
https://www.kaggle.com/datasets/vijaykumar1799/face-mask-detection/data

- with mask

![image](https://github.com/muhmiqbal19/mask-wearing-face-detection/assets/132751713/3358293d-49e4-41fa-b5c2-1145ebfbcf25) 

- without mask

![image](https://github.com/muhmiqbal19/mask-wearing-face-detection/assets/132751713/04506fb8-7f5e-4c8c-914c-af6d3c8566a7) 

- with mask but incorrect

![image](https://github.com/muhmiqbal19/mask-wearing-face-detection/assets/132751713/6f4b356c-f4b2-4860-b4ab-079579c6bd0a) 

## Methods
- Develop machine learning model for computer vision implementation.
- Supervise the machine learning with 8982-labelled attributes.
- Classifying images into 3 classes. Multiclass classification problem.
- The model to build is neural network for a many images problem.
- Neural network that will be used is CNN and DNN.

![image](https://github.com/muhmiqbal19/mask-wearing-face-detection/assets/132751713/bde4776e-1f85-4b1f-a6b8-c9d65161ff9d)

### DNN & CNN
- Convolution

![image](https://github.com/muhmiqbal19/mask-wearing-face-detection/assets/132751713/2d240868-bedd-49ae-b7ab-7d54705785ee)

- Max pooling

![image](https://github.com/muhmiqbal19/mask-wearing-face-detection/assets/132751713/ebcb8229-b2f8-4c62-a0e4-a2738a6a8d90)

- CNN -> DNN

![image](https://github.com/muhmiqbal19/mask-wearing-face-detection/assets/132751713/39d0e57c-0c01-4861-9d9e-d590060616e3)

## Data Processing and Result
### Data Pre-Processing and Model Building
- Split data with 80% train set and 20% validation set.
- Do image augmentation by using image data generator to rescale, rotate, flip, and shear train-image data. The purpose is to adapt with “false” various images taking.
- Model build with CNN → DNN

![image](https://github.com/muhmiqbal19/mask-wearing-face-detection/assets/132751713/f81d6915-05dc-4a6b-9cad-8389deaaee94)

### Training and Validating
- Reach more than 92% both train and test in 3 epoch.
- No overfitting and underfitting.
- A flat accuracy trend after 3 epoch extrapolated.

![image](https://github.com/muhmiqbal19/mask-wearing-face-detection/assets/132751713/ba327041-1a7e-4a66-9b13-4d6963844066)

### Prediction with a New Image

![image](https://github.com/muhmiqbal19/mask-wearing-face-detection/assets/132751713/1d408524-075c-4a52-b07b-669b5b8033e7)

## Interpretation and Evaluation
- Both training and validating reach more than 92% accuracy in 3 epoch.
- Both training and validating reach a minimum loss less than 0,2.
- Good dataset: resolution and proportion.
- It’s more difficult to different a with-mask and an incorrect wearing because of pixel map similarity.
- You should transfer a learning from other trained model that can help your model.




