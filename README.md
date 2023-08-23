# Pneumonia Identifier from Chest X-Ray || Kaggle
### Image Sample of Pneumonia Patient
![person1_virus_6](https://github.com/ghubnerr/pneumonia-chest-xray/assets/91924667/0605377a-4449-49d2-8500-cc889f49f006)

### Collecting the Data
Data provided by Kaggle. Contains three main folders: train, test, and validation, each housing subfolders for two image categories - Pneumonia and Normal. In total, it consists of 5,863 chest X-ray images in JPEG format, focusing on pediatric patients aged one to five years old.

API command:
```kaggle datasets download -d lasaljaywardena/pneumonia-chest-x-ray-dataset```

## Using ResNet50 and Keras Tuner
ResNet50 is a pre-trained CNN able to handle complex visual recognition tasks. Find it at [Keras](https://keras.io/api/applications/resnet/).
Additionally, Keras Tuner is a hyperparameter tuner that evaluates accuracy of different optimizers, loss functions and epochs of training to output the best possible hyperparameters. Documentation can be found at [Keras](https://keras.io/keras_tuner/).

Hyperparameter trials can be found inside [this folder](./hyperparameter_tuning)
### Measuring Accuracy
![image](https://github.com/ghubnerr/pneumonia-chest-xray/assets/91924667/98f0caf5-2cf5-4b32-9871-f55662f88597)

### Loading the Model
```
import tensorflow as tf
loaded_model = tf.keras.models.load_model('./pneumonia_detector')
```
