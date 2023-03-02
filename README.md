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

Where: \ 
- "Animal[x]" are folders containing images of that animal (the more the better for training); \
- distractors are images not of animals that are actually in the training set (used to trick the NN)


