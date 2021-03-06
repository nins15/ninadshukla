# Visualizing Weights of CNN Deep learning model on ISIC dataset: Project overview
* I have visualized the intermediate weights that exist between the layers of a neural network
* An image from the ISIC data set which contains Malignant and benign images fed into the network
* Output is an image representing 'weight concentrations'
## Data Collection
The dataset was obtained from kaggle.com (https://www.kaggle.com/fanconic/skin-cancer-malignant-vs-benign)
## EDA

![alt text](https://github.com/nins15/Visualizing-Weights-of-CNN-model-on-ISIC-dataset/blob/master/Disease.png "Disease")
![alt text](https://github.com/nins15/Visualizing-Weights-of-CNN-model-on-ISIC-dataset/blob/master/Height_width.png "Size")
![alt text](https://github.com/nins15/Visualizing-Weights-of-CNN-model-on-ISIC-dataset/blob/master/Sampleimages.png "sampleimages")

## Building a model
I split the data into train and validation sets with a size of 25%.I used adam as optimizer.Instead of using tranfer learning I made a small model for scratch so that it will be easier to obtain weights from all the layers.




![alt text](https://github.com/nins15/Visualizing-Weights-of-CNN-model-on-ISIC-dataset/blob/master/ISICaccuracy.png "Accuracy")
![alt text](https://github.com/nins15/Visualizing-Weights-of-CNN-model-on-ISIC-dataset/blob/master/ISICloss.png "Loss")

## Visualizing the weights between layers
The first layer acts is retaining the full shape of the image, although there are several filters that are not activated and are left blank. At that stage, the activations retain almost all of the information present in the initial picture. As we go deeper in the layers, the activations become increasingly abstract and less visually interpretable. They begin to encode higher-level features. Higher presentations carry increasingly less information about the visual contents of the image, and increasingly more information related to the class of the image. As mentioned above, the model stucture is overly complex to the point where we can see our last layers actually not activating at all, there's nothing more to learn at that point. This represent the weight of one layer of image.
![alt text](https://github.com/nins15/Visualizing-Weights-of-CNN-model-on-ISIC-dataset/blob/master/weights.png "weights")



