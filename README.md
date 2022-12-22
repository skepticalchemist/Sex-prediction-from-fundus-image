# Sex prediction from retinal fundus image using deep learning


![fundus_image](assets/100_fundus_image.jpg)


## The problem

The examination of the optic fundus consists of observing the structures of the posterior segment of the eye (optic nerve head, retina, retinal vessels, and choroid). This exam can diagnose several diseases: ocular hypertension, arteriosclerosis, diabetes, glaucoma, vascular occlusions (both arterial and venous system), nephropathy, and brain tumors, among others.

Ophthalmologists are not trained to identify the gender from fundus images. Even though this is not as useful as predicting diseases, predicting gender from eye fundus images using deep learning can demonstrate how this technique can support the decision-making process in healthcare.

Here we'll predict gender from retinal fundus image using deep learning.


## The data

Ocular Disease Intelligent Recognition is a structured ophthalmic database formed by 10,000 fundus images from 5,000 clinical patients containing age, color fundus photographs from left and right eyes, and doctors' diagnostic keywords from doctors (ODIR-5K). 

This anonymized dataset was collected by Shanggong Medical Technology Co., Ltd. from different hospitals/medical centers in China where fundus images were captured by different leading to varied image resolutions. 

Annotations were labeled by trained professionals with quality control management which classified patients into eight labels based on both eye images and additionally patient age:
* normal (N), 
* diabetes (D), 
* glaucoma (G), 
* cataract (C), 
* AMD (A), 
* hypertension (H), 
* myopia (M) and 
* other diseases/abnormalities (O) 

The dataset can be obtained following the instructions available at this [GitHub repository](https://github.com/nkicsl/OIA-ODIR).

The dataset is splited into three parts, the training set, the off-site test set (used as validation set), and the on-site test set (used as test set) which contains 3,500, 500 and 1,000 patients, respectively.

To predict the gender we'll use only normal fundus images. In the case the left or right eye image is labeled as not normal won't use it. These images we'll be stored in a data directory with the following structure:

```bash
├── test
│   ├── female
│   └── male
├── train
│   ├── female
│   └── male
└── val
    ├── female
    └── male
```

# Modeling

1. transfer learning
* Xception
* Inception V3
* MobileNet V2

2. model architecture: 3

3. augmented images

4. adaptable learning rate (LearningRateScheduler)

5. Optimizers
* SGD
* Adam
* RMSprop

6. Autokeras

7. Cloud
* Saturn Cloud 
* Sagemaker Studio Lab
* Google Colab


