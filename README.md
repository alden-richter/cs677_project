# CS 677 Final Project

## Dataset

For this project, I used a [Waste Classification dataset](https://www.kaggle.com/techsash/waste-classification-data), which consists of 25k images of garbage, labeled as either recyclable or organic. The dataset is split 85-15 into train and test subsets.

## Classifiers

To classify the data, I selected three pretrained image classification networks: ResNet, VGG, and AlexNet. I removed the final fully connected layer from each of them and replaced it with a new classification layer. I then fine-tuned each of the three models on the training set and recorded the results on the test set. Each model was fine tuned with a learning rate of .0001, Adam optimizer, binary cross entropy loss, and batch size of 12 for 2 epochs.

## Results


