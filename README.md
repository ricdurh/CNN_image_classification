# CNN Image Classification

This project consists of experimenting with different neural networks for image classification. The CIFAR-10 dataset (Canadian Institute For Advanced Research) is used, which consists of 60,000 color images of 32x32 size. Each image contains one of the following ten classes: airplane, automobile, bird, cat, deer, dog, frog, horse, ship, and truck. I went through the following process:

## Methods

The data is split into 45,000 training, 5,000 validation, and 10,000 test images, with the test images containing 1,000 randomly selected images from each class. The data is rescaled to go from 0-1 by dividing each element by 255, so the 45,000 training images has a shape of (45000, 32, 32, 3).

## 16 Experiment Results
Here are the results of the 16 models testing various architectures and hyperparameters
![](/images/_16_models.png)


## Best Performing Model
The best performing model incorporated data augmentation to artificially increase the size of the dataset, and used baseline VGG blocks, similar to what was used [here](https://medium.com/analytics-vidhya/introduction-to-computer-vision-with-baseline-vgg-blocks-on-the-cifar-10-dataset-731d19439922). This is a CNN architecture that also uses multiple stacked layers.  The model achieves a validation and test accuracy of 80%. Below is the model's validation accuracy and loss, as well as the test data's confusion matrix

![](/images/_cnn_model_15_accuracy_loss.png)

![](/images/_cnn_conf_matrix.png)

### Finally, the t-SNE shows how the model is doing at correctly clustering the different categories
![](/images/_cnn_tsne.png)
