# SlidingWindowObjectDetection
Given a set of images, task is to identify the objects belonging to classes : aeroplane, bottle and chair, and draw a bounding box around it.

## Methods used

### Resnet18 - 1 layer model

* Used a pretrained resnet18 model, and trained a classification network on the cropped object images from the dataset.

* While testing on an image, took sliding window of several sizes and aspect ratios, and passed them through our trained resnet18 model to get the softmax scores for each of the 3 classes, and a background class.


### Resnet18 - 2 layer model

* Have two layers of different feature map sizes. Last layer and the second last block with feature map size smaller than the last. So basically, removed the last block of resnet18 for layer 2.

* Pass the image from both the pretrained networks and obtain a feature map from each, and concatenate the features, then passes it to the feed forward network with 4 classes with Relu non linearity.


### Sample Result preview

![](https://github.com/prerit2010/SlidingWindowObjectDetection/blob/master/result.png)
