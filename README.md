# GardenCritterDetector

The garden critter detector is a program that allows users to detect the presence of common pests within their garden. This is done through the use of Nvidia's Jetson Nano in combination with the Resnet-18 Network. For this particular use case, the Resnet-18 Network was trained on a series of images of chipmunks and strawberry plants.

Purpose:
This program is useful for the protection of crops and other small plants. This program is by no means a finished model but instead a prototype for a possible detection device that is able to identify multiple different pests. This technology could be improved and utilized in farming practices. For the time being, the program only detects chipmunks and strawberry plants. Detecting particular plants within the garden could allow for greater specialization within detection of pests.


Directions:

1. Download the classification file. This file contains the data used to train the model as well as the trained model which can detect chipmunks and strawberry plants.
2. Navigate to jetson-inference/python/training.
3. Remove the default classification file.
4. Replace the classification file with the one downloaded from this github page.
5. In order to run a test, use the following command:
   imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/test/chipmunk/01.jpg chipmunk.jp   
7. 


How it was made:
