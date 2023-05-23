# Animal Classification
10 classes of animals are selected to be classified. The classes of animals are: fish, lion, turtle, whale, dolphin, tortoise, elephant, wolf, cow, goat.

![Training](/images/results.jpg)

The results from training show an accuracy of approximately 94% after 10 epochs. The accuracy of each epoch shows slight fluctuations meaning that there are some images in the validation set that are difficult for the model to predict as more training is done, potentially meaning that the model has overfit to some classes. This could be due to more images of that class or classes sharing similar low level features such as colour, shape, etc. Also, animal classes might share higher level features, e.g. turtles and tortoises sharing the shell feature.

![Confusion](/images/confusion.jpg)

The confusion matrix shows the difference in predicted classes and actual classes of the model. It is ideal to have all predictions along the top left to bottom right diagonal, therefore all animal classes are correctly predicted. From the confusion matrix, it shows that there are some class combinations that are harder for the model to predict such as: goat / cow, turtle / tortoise. Fish / elephant is likely to be a rare fish and hard to distinguish, i.e. it does not share common features with other fish in the dataset so the model is uncertain about the animal class it belongs to.

![Loss](/images/loss.png)

The top losses during training are plotted to show the combinations of animals that are hardest to predict. From this, it shows that turtle / tortoise is the hardest to predict which is likely due to the similar features that thw 2 animal classes share (shell, colour, shape). Other losses occur when the model correctly predicts the animal class but is not certain that it is correct such as the dolphin image; this is potentially due to 2 dolphins in the image whereas the model was trained with just 1 dolphin in the image. The elephant / fish combination shows an anglerfish, this is likely unseen in training and therefore difficult to predict.
