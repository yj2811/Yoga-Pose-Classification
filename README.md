# Yoga-Pose-Classification

AIM: To classify images of people into their respective yoga pose’s class 

Using Jupyter Notebooks to showcase the source code and its corresponding output: 

[The 1st ipynb notebook (Yoga_Pose_Classifier_CNN)](https://github.com/yj2811/Yoga-Pose-Classification/blob/main/Yoga_Pose_Classifier_CNN.ipynb) uses a custom-made CNN model to classify the images. 

Training set : 1011 image files,
Testing set : 470 image files

Training set accuracy: 94.33%,
Validation set accuracy: 93.97%,
Test set accuracy: 88.41%

[The 2nd ipynb notebook (Yoga_Pose_Classifier_CNN_kerastuner)](https://github.com/yj2811/Yoga-Pose-Classification/blob/main/Yoga_Pose_Classifier_CNN_kerastuner.ipynb) also uses a custom-made CNN along with a scalable hyperparameter optimization framework KerasTuner. The base Tuner class is the class that manages the hyperparameter search process, including model creation, training, and evaluation. The built-in Tuner subclass RandomSearch is used as a tuning algorithm.

On the same training and testing data size as above:

Training set accuracy: 96.82%,
Validation set accuracy: 87.07%,
Test set accuracy: 81.64%

[The 3rd ipynb notebook (keypoint_identification_posenet)](https://github.com/yj2811/Yoga-Pose-Classification/blob/main/keypoint_identification_posenet_.ipynb) uses PyTorch implementation (multi-pose only) of the Google TensorFlow.js Posenet model to predicts the locations of 17 keypoints of the human body.

Currently working on: 
1. Using geometry and the key points generated (which will be extracted as a JSON object) to classify the yoga poses by finding patterns.
2. Using PoseNet for initial keypoint identification followed by CNN for classification of yoga poses by extracting features from 2D coordinates of the keypoints.

(These joint locations or keypoints are indexed by "Part ID” which is a confidence score whose value lies in the range of 0.0 and 1.0 with 1.0 being the greatest.)

[The 4th ipynb notebook (OpenPose_Yoga_Pose_Classifier)](https://github.com/yj2811/Yoga-Pose-Classification/blob/main/OpenPose_Yoga_Pose_Classifier.ipynb) has OpenPose installed and various functions defined to get keypoints.

Currently working on: Fixing errors related to file paths and seeing how well OpenPose can outline the the given pose and later training the model.
