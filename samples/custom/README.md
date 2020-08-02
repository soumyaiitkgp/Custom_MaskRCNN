# Custom dataset training

In this folder you will find three main folders/files
1. custom.py - to train your model
2. demo.ipynb - to visualize the results
3. dataset/train and dataset/val for training and validation of the model


[This blog post](https://medium.com/@psoumyadav/a-simple-guide-to-maskrcnn-custom-dataset-implementation-27f7eab381f2) describes this sample in more detail.

## Train the custom model

Train a new model starting from pre-trained COCO weights
```
python3 balloon.py train --dataset=/path/to/balloon/dataset --weights=coco
```

Resume training a model that you had trained earlier
```
python3 balloon.py train --dataset=/path/to/balloon/dataset --weights=last
```

Train a new model starting from ImageNet weights
```
python3 balloon.py train --dataset=/path/to/balloon/dataset --weights=imagenet
```

The code in `custom.py` is set to train for 3K steps (30 epochs of 100 steps each), and using a batch size of 2. 
Update the schedule to fit your needs.
