1_Data_Generation --> This notebook creates a dataset of face and non-face images from the FDDB dataset (http://vis-www.cs.umass.edu/fddb/)

The FDDB dataset comes with a 'FDDB-fold-xx-ellipseList.txt' for every folder of images in the dataset.

Define the FDDB dataset original path folder in imagePath variable, and set the training_path and test_path folder paths.

Input the required image size.

This notebook will crop the face and non-face images and create a training dataset (1000 face and non-face images) and
a test dataset (100 face and non-face images).



2_Babysitting_DNN --> This notebook goes step-by-step in creation of CNN for binary image classification of face and non-face images.

The training data created from 1_Data_Generation is split into training and validation data.

Model 1 --> A CNN with 3 convolutional layers.

Model is evaluated (Loss and Accuracy) for unnormalized data and normalized data, with varying learning rates and regularization values.

Manual hyperparameter tuning is done by doing coarse and fine search of learning rates and regularization values.

The best values found from the above search are used to evaluate the model and performance is measured by plotting the
loss and accuracy curves and by confusion matrix.


Model 2 --> A CNN with 3 convolutional layers, BatchNormalization and Xavier weight initialization

Model 2 is evaluated with the best learning rate and regularization value found in the above steps and 
the performance is measured by plotting the loss and accuracy curves and by confusion matrix.