# COLOUR DETECTOR 

## A. PROJECT SUMMARY

**Project Title:** Colour Detector

**Team Members:** 
- Nur Aisya Fatihah binti Azhar
- Nur Afiqah binti Halim
- Nur Syahirah binti Izwan Wasandan
- Afza Adawiyah binti Abdul Tahrim


- [ ] **Objectives:**
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

An image example is provided so that you can test the colour detector.

We’ll be reviewing the Python scripts in this tutorial:

- colour_detection.py: Accept image from user and use pandas to read the dataset



## E.  TRAINING THE COLOUR DETECTOR

We are now ready to train our colour detector using OpenCV and Pandas.

From there, open up a terminal, and execute the following steps:

- Open color_detection.py
- Import dataset using read_csv method
- Define global variables (r = g = b = xpos = ypos = 0)
- Create color recognition function
- Create mouse click function
- Open image file using OpenCV


![Figure 4](https://github.com/aisyafatihah/AI-Project/blob/main/AI/PLotterColour.png)

Figure 4: Testing colour 

Given these results, we are hopeful that our model will generalize well to images outside our training and testing set.


## F.  RESULT AND CONCLUSION

Detecting COVID-19 face masks with OpenCV in real-time

You can then launch the mask detector in real-time video streams using the following command and steps:
- python color_detection.py -i colorpic.jpg
- [INFO] loading image...
- [INFO] open the windows...
- Click on the colour desired

![Figure5](https://github.com/aisyafatihah/AI-Project/blob/main/AI/colour_detect.JPG)

Figure 5: Flow of Colour Detector in real-time 

In Figure 5, you can see that our colour detector is capable of running in real-time and is correct in its predictions as well.



## G.   PROJECT PRESENTATION 

In this project, you learned how to create a Colour Detector using OpenCV and Pandas.

We also  learned about how we can extract color RGB values and the color name of a pixel. 

Other than that, we learned how to handle events like double-clicking on the window and see how to read CSV files with pandas and perform operations on data.


[![demo](https://img.youtube.com/vi/JxmmOktlN6U/0.jpg)](https://www.youtube.com/watch?v=JxmmOktlN6U "demo")

