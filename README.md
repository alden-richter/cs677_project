# CS 677 Final Project

## Dataset

For this project, I used a [Waste Classification dataset](https://www.kaggle.com/techsash/waste-classification-data), which consists of 25k images of garbage, labeled as either recyclable or organic. The dataset is split 85-15 into train and test subsets.

## Classifiers

To classify the data, I selected three pretrained image classification networks: ResNet, VGG, and AlexNet. I removed the final fully connected layer from each of them and replaced it with a new classification layer. I then fine-tuned each of the three models on the training set and recorded the results on the test set. Each model was fine tuned with a learning rate of .0001, Adam optimizer, binary cross entropy loss, and batch size of 12 for 2 epochs.

## Results

| Model type | Accuracy | TP   | FP  | TN   |  FN |  TPR  | TNR
|-----------|----------|------|-----|------|-----|-------|------
|    resnet | 95.3442% | 1019 | 24  | 1377 | 93  | 0.916 | 0.983
|       vgg | 90.7282% | 892 |  13 | 1388 | 220 | 0.802 | 0.991
|   alexnet | 94.1106% |  1076 | 112 | 1289 |  36 |  0.968 |   0.920

## Discussion

As you can see in the table above, the ResNet-based classifier had the best accuracy with over 95%. The next best classifier was AlexNet with over 94% accuracy. Note that AlexNet had a higher true positive rate, but a lower true negative rate. Finally, VGG had the highest true negative rate with over 99%, but had the lowest accuracy due to its lower true positive rate at just over 80%.

