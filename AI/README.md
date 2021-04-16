# COLOUR DETECTOR 

## A. PROJECT SUMMARY

**Project Title:** Colour Detector

**Team Members:** 
- Nur Aisya Fatihah binti Azhar
- Nur Afiqah binti Halim
- Nur Syahirah binti Izwan Wasandan
- Afza Adawiyah binti Abdul Tahrim


- [ ] **Objectives:**
- Break out the project goal into more specific objectives
- To detector various colour on certain objects
- To show a correct name for the colour checked
- To provide RGB values of each color


##  B. ABSTRACT 

  Colour of an object depends on both the object and its environment. Objects can be said to have the colour of the light leaving their surfaces. There are a lot of colour existed in this world. Every shade of colour has different code and hex number. Even in simple picture, there are a lot of colours that might look similar but actually a different name. 
  The colour has continuous spectrum and as for now, you as a Machine Learning Engineer are going to use AI technology to recognize the colour in a picture


![Coding](https://github.com/aisyafatihah/AI-Project/blob/main/AI/figure1.png)
Figure 1 shows colour spectrum.


## C.  DATASET

In this project, we’ll discuss on how our computer vision pipeline will be implemented in order to detect the colour.

From there, we’ll review the dataset we’ll be using to train our custom colour detector.

I’ll then show you how to implement a Python script to train a colour detector on our dataset using OpenCV and Pandas.

The dataset we’ll be using here today was created by reader Mathew Brush.

This dataset consists of 865 of colour names.

Our goal is to train machine to detect the colour in a picture.


## D.   PROJECT STRUCTURE

The following directory is our structure of our project:
- $ tree --dirsfirst --filelimit 10
- .
- ├── dataset
- │   └── colors [865 entries]
- ├── examples
- │   ├── almond
- │   ├── american_rose
- │   └── blush
- ├── color_detection.py
- ├── colorpic.jpg
- └── Colors.csv

An image exampleis provided so that you can test the colour detector.

We’ll be reviewing the Python scripts in this tutorial:

- colour_detection.py: Accept image from user and use pandas to read the dataset



## E   TRAINING THE COLOUR DETECTOR

We are now ready to train our colour detector using OpenCV and Pandas.

From there, open up a terminal, and execute the following command:

- python color_detection.py -i colorpic.jpg
- [INFO] loading images...
- [INFO] compiling model...
- [INFO] training head...
- Train for 34 steps, validate on 276 samples
- Epoch 1/20
- 34/34 [==============================] - 30s 885ms/step - loss: 0.6431 - accuracy: 0.6676 - val_loss: 0.3696 - val_accuracy: 0.8242
- Epoch 2/20
- 34/34 [==============================] - 29s 853ms/step - loss: 0.3507 - accuracy: 0.8567 - val_loss: 0.1964 - val_accuracy: 0.9375
- Epoch 3/20
- 34/34 [==============================] - 27s 800ms/step - loss: 0.2792 - accuracy: 0.8820 - val_loss: 0.1383 - val_accuracy: 0.9531
- Epoch 4/20
- 34/34 [==============================] - 28s 814ms/step - loss: 0.2196 - accuracy: 0.9148 - val_loss: 0.1306 - val_accuracy: 0.9492
- Epoch 5/20
- 34/34 [==============================] - 27s 792ms/step - loss: 0.2006 - accuracy: 0.9213 - val_loss: 0.0863 - val_accuracy: 0.9688
- ...
- Epoch 16/20
- 34/34 [==============================] - 27s 801ms/step - loss: 0.0767 - accuracy: 0.9766 - val_loss: 0.0291 - val_accuracy: 0.9922
- Epoch 17/20
- 34/34 [==============================] - 27s 795ms/step - loss: 0.1042 - accuracy: 0.9616 - val_loss: 0.0243 - val_accuracy: 1.0000
- Epoch 18/20
- 34/34 [==============================] - 27s 796ms/step - loss: 0.0804 - accuracy: 0.9672 - val_loss: 0.0244 - val_accuracy: 0.9961
- Epoch 19/20
- 34/34 [==============================] - 27s 793ms/step - loss: 0.0836 - accuracy: 0.9710 - val_loss: 0.0440 - val_accuracy: 0.9883
- Epoch 20/20
- 34/34 [==============================] - 28s 838ms/step - loss: 0.0717 - accuracy: 0.9710 - val_loss: 0.0270 - val_accuracy: 0.9922
- [INFO] evaluating network...

|      |    precision    | recall| f1-score | support |
|------|-----------------|-------|----------|---------|
|with_mask|0.99|1.00|0.99|138|
|without_mask|1.00|0.99|0.99|138|
|accuracy| | |0.99|276|
|macro avg|0.99|0.99|0.99|276|
|weighted avg|0.99|0.99|0.99|276|


![Figure 4](https://www.pyimagesearch.com/wp-content/uploads/2020/04/face_mask_detector_plot.png)

Figure 4: Figure 10: COVID-19 face mask detector training accuracy/loss curves demonstrate high accuracy and little signs of overfitting on the data

As you can see, we are obtaining ~99% accuracy on our test set.

Looking at Figure 4, we can see there are little signs of overfitting, with the validation loss lower than the training loss. 

Given these results, we are hopeful that our model will generalize well to images outside our training and testing set.


## F.  RESULT AND CONCLUSION

Detecting COVID-19 face masks with OpenCV in real-time

You can then launch the mask detector in real-time video streams using the following command:
- $ python detect_mask_video.py
- [INFO] loading colour detector model...
- [INFO] starting detecting...

![Figure5](https://github.com/aisyafatihah/AI-Project/blob/main/AI/colour_detect.JPG)

Figure 5: Flow of Colour Detector in real-time 

In Figure 5, you can see that our colour detector is capable of running in real-time and is correct in its predictions as well.



## G.   PROJECT PRESENTATION 

In this project, you learned how to create a Colour Detector using OpenCV and Pandas.

To create our colour detector, we trained a two-class model of people wearing masks and people not wearing masks.

We fine-tuned MobileNetV2 on our mask/no mask dataset and obtained a classifier that is ~99% accurate.

We then took this face mask classifier and applied it to both images and real-time video streams by:

- Detecting faces in images/video
- Extracting each individual face
- Applying our face mask classifier

Our face mask detector is accurate, and since we used the MobileNetV2 architecture, it’s also computationally efficient, making it easier to deploy the model to embedded systems (Raspberry Pi, Google Coral, Jetosn, Nano, etc.).

[![demo](https://img.youtube.com/vi/JxmmOktlN6U/0.jpg)](https://www.youtube.com/watch?v=JxmmOktlN6U "demo")

