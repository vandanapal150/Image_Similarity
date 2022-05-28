Flixstock Visual Search Assignment

Problem Statement: Finding Visually Similar Garments for an Input Garment
Garments in the fashion domain can be of multiple shapes, sizes, and colors. Finding garments similar to
each other is an important feature used by e-commerce websites to show recommendations to its users.
We would like to find visually similar garments for any input garment from within a given dataset of garment
images.

Implemented transfer learning model with VGG-16 and then extracted features from that model for Image Retrieval.

firstly, used ImageDataGenerator to get train and test datasets with input shape (224, 224, 3) and normalized all images with rescale=1./255. 
Then created models without last classification layer and added a fully connected layer which has 1024 neuron.
Set  lastFourTrainable as False so that only last fully connected layer of models will be trainable.

For Image Retrieval used feature extraction from VGG-16 model. For extracting features output before classification layer of models are used.
Then fed train images to model and compared its feature vector with all feature vectors. 
Used cosine distance to find similarity between feature vectors and got 10 similar images.

Screenshot of one image and its similar 10 images
