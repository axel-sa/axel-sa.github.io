# Classifying AI Generated / Real Images
The provided CIFAKE dataset provides a large dataset to train a binary classification model to determine if an image is AI generated or real. I trialled how the ResNet pretrained models performed on the dataset:

## ResNet18

![Training results](/images/resnet18.jpg)


## ResNet34

![Training results](/images/resnet34.jpg)

## ResNet50

![Training results](/images/resnet50.jpg)

We can see that the models perform similarly and ResNet50 having the greatest accuracy after 3 epochs. The increased training time of ResNet50 compared to the other models is also minimal. However, when image transforms are applied to the training dataset to increase the resolution, the training time for ResNet50 exponentially increases (hours compared to minutes). As this is done locally on a GPU, this was not tested thoroughly as out of memory issues started to become a problem.
