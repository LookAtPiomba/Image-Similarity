# Image-Similarity
Image Similarity using pre-trained Neural Networks (EfficientNetV2, ResNet101)

Dataset used in Training should be as follows: 

Dataset \
|__ training \
|_______ "Animal1" \
|_______ "Animal2" \
|_______ ... \
|__ validation \
|______ distractors \
|______ gallery \
|_________ "Animal1" \
|_________ "Animal2" \
|_________ ... \
|______ query \
|_________ "Animal1" \
|_________ "Animal2" \
|_________ ...

Where: 
- "Animal[x]" are folders containing images of that animal (the more the better for training); 
- distractors are images not of animals that are actually in the training set (used to trick the NN)
- gallery are images that are given to the NN to order from the most similar to the least one
- query are query images of that animal to be given to the NN to evaluate similarity with all the images in the gallery

What the Neural Network actually does is given each image query, calculate the similarity with all the images in the gallery. \
Those images are then ordered by similarity and the quality of the NN is evaluated calculating the percentage of time in which the most similar image of the same class of the query image is in Top 1, Top 5 or Top 10.
(In other words a Top 10 accuracy of 90% means 90 out of 100 at least one image of the same class is in the 10 most similar images)

#How to use
- Create your own dataset
- Train the NN you prefer by changing Hyperparameters 
- Save the model
- Load the model in the [Evalutation Notebook](/code/Evaluation.ipynb)
