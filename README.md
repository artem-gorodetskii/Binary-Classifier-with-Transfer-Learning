# Transfer-Learning-Test-Project
This  project represents TensorFlow implimentation of CNN binary classifier using transfer learning technique. 
The model allows to distingwish images containing Saint George with accuracy 94.0%. It was trained on Tesla K80 GPU (Kaggle).

## Project structure
* 'load_data.ipynb' file allows to download images and separate them on training and validation datasets (70/30 %).
* 'train_classifier.ipynb' file contains TensorFlow implementation of the model and its training  process.
* 'pyproject.toml' file contains all required project dependencies.

## Model architecture and training process 
Pretrained on ImageNet dataset Xception model was used as a basis for this binary classifier. The top layer was removed and a simple Dense layer with one neuron and sigmoid activation was used instead.
In order to make the model more generalized, a data augmentation technique was used. Below you can see examples of images with augmentation:
![img1](images/images_examples.png)

During the training process the following learning rate schedule was used(learning rate vs. epoch):
<p align="center">
  <img src="images/lr_vs_epoch.png" width="300" />
</p>

The following figure display 'loss' and 'accuracy' curnes during training process:
<p align="center">
  <img src="images/training_curves.png" width="400" />
</p>

## Results
The model scores for accuracy, precision and recall are 94.0, 94.0, and 92.4, respectively.
