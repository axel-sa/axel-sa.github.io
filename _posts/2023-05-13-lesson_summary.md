# FastAI Lessons 1 - 3

This first post is to summarise the learning from the first 3 lessons of the Fast AI course.

## Lesson 1 - Deep Learning Introduction
The first lesson is an introduction to deep learning and the easability to implement an image classifier. There is a general process to follow: import required libraries (fastai, duckduckgo_search, etc), use duckduckgo_search to collect images of different classes to classify, verify that the images are usable, load it into a DataBlock object, train with the `vision_learner` from the fastai library using a pretrained model (resnet18, resnet34, etc) and evaluate the model performance with unseen images (validation set) and loss function (default cross entropy). This is useful to implement an image classifier to classify 10 classes of animals for the assignment.

## Lesson 2 - Deep Learning Deployment, Preprocessing and Cleaning of Data
The second lesson is about deploying deep learning models into apps using Gradio, preprocessing images for model training, cleaning data and evaluating model performance with confusion matrices and top loss predictions  . A confusion matrix allows the model to be evaluated by looking at the model prediction along the x-axis and what the image label actually was along the y-axis. Thus, it shows relationships between classes and what might be similar in features learnt by the model. It can also be used to identify classes that can potentially have incorrect images downloaded by the duckduckgo_search library. The `ImageClassifierCleaner` is another useful class in the fastai library as it allows for the removal and manual labelling of images in the dataset. This is useful as the duckduckgo_search library can return irrelevant images even though it contains the specified tag.

## Lesson 3 - Neural Network Foundations
The third lesson provides an explanation of how neural networks use hidden layers, neurons and activation functions to optimise the neuron weightings across layers by using loss functions such as mean squared error to fit to the training data. Multiple rectified linear function (ReLu) can be used to optimise the weightings. While this is all handled by functions provided by the fast ai library, it provides an explanation on how the `vision_learner` can accurately predict what the animal is in the image. This lesson also visually displays the train time versus accuracy of pretrained models to see the trade-off between wanting a fast trained model with reasonable accuracy compared to a longer trained model with greater accuracy.

## Summary
The first 3 lessons provide a solid base to start using deep learning for image processing and classification. The *00-is-it-a-bird-creating-a-model-from-your-own-data* Jupyter notebook provided by FastAI can be altered to expand the number of animal classes that can be classified.
