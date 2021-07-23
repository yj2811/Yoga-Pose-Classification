# Yoga-Pose-Classification

AIM: To classify images of people into their respective yoga pose’s class.

[The first ipynb notebook (Yoga_Pose_Classifier_CNN)](https://github.com/yj2811/Yoga-Pose-Classification/blob/main/Yoga_Pose_Classifier_CNN.ipynb) uses a CNN to classify the images.

Training set accuracy: 94.33%
Validation set accuracy: 93.97%
Test set accuracy: 88.41%

[The second ipynb notebook (Yoga_Pose_Classifier_CNN_kerastuner)](https://github.com/yj2811/Yoga-Pose-Classification/blob/main/Yoga_Pose_Classifier_CNN_kerastuner.ipynb) also uses a CNN along with a scalable hyperparameter optimization framework KerasTuner. The base Tuner class is the class that manages the hyperparameter search process, including model creation, training, and evaluation. The built-in Tuner subclass  RandomSearch is used as a tuning algorithm.

Training set accuracy: 96.82%
Validation set accuracy: 87.07%
Test set accuracy: 81.64%

[The third ipynb notebook (keypoint_identification_posenet)](https://github.com/yj2811/Yoga-Pose-Classification/blob/main/keypoint_identification_posenet_.ipynb) uses PyTorch implementation (multi-pose only) of the Google TensorFlow.js Posenet model to predicts the locations of 17 keypoints of the human body.

Currently working on: Using geometry and the key points generated (extracted to JSON) to classify the yoga poses by finding patterns.

[The fourth ipynb notebook (OpenPose_Yoga_Pose_Classifier)](https://github.com/yj2811/Yoga-Pose-Classification/blob/main/OpenPose_Yoga_Pose_Classifier.ipynb) has OpenPose installed and various functions defined to get keypoints.

Currently working on: Fixing errors related to file paths and seeing how well OpenPose can outline the the given pose and later training the model.
