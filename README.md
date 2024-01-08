# Apple
## IPhone Housing Defect Detection 
### Approach
Approach: Utilized a Classification-based methodology for detecting defects in images.

Model: Employed a Pretrained Resnet 50 model to extract image features.

Architecture: Incorporated additional Dense layers for binary classification.

Imbalanced Data: Faced scarcity in defected images; addressed the issue by augmenting the existing defect images and using Synthetic minority oversampling method.

Data Split: Segregated input images into an 80:20 ratio for training and testing purposes.

Validation Technique: Achieved satisfactory accuracy without implementing K-fold Cross Validation.
### Implementation
The iPhoneHousingDefectDetection.ipynb file has the complete implementation. The input data is provided in data folder. (Change the path of input data path in the ipynb)

The algorithm is implemented using Tensorflow Framework in Python.
### Metrics used to assess the algorithm
Precision, Recall and  F1-score metrics are used to assess the algorithm
### Bonus problem
To automatically locate or annotate the defect area for further analysis following can be done:
1) Instead of using classification based approach, image segmentation method can be used to automatically locate the defect area. (Since labels were not provided I have considered classification)
2) Unsupervised learning techniques like clustering can be used but needs detailed fine tuning. (Since the pixel values of the defected areas were not consistant, k-means did not perform well, so did not consider this approach)
3) Autoencoders can also be used to reconstruct the input image and then a given image can be considered as an anomaly if the reconstruction error is more.
