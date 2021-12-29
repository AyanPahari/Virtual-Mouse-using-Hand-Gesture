
# Virtual Mouse using Hand Gestures

I did this project about 4 years back during my bachelor's . I forgot to push it on github that time so doing it now ;)

## About the Project

Developed a program for controlling the mouse movement using Python and openCV with real-time camera that detects hand landmarks, tracks gesture patterns instead of a physical mouse.

There you go!! Now you can do all the cursor operations without using an actual mouse :)

We are going to recognize hand gestures from a video sequence. To recognize these gestures from a live video sequence, 
we first need to take out the hand region alone removing all the unwanted portions in the video sequence. 
After segmenting the hand region, we then count the fingers shown in the video sequence to instruct a robot based on the finger count. 
Thus, the entire problem could be solved using 2 simple step:

    1.	Find and segment the hand region from the video sequence.
    2.	Count the number of fingers from the segmented hand region in the video sequence.

#### Note

In order for the controller to detect your finger movements make sure to use two red tape or ribbons and stick it to your fingers.


## Requirements

- Python

        Python is the platform on this complete project is made. The version of this platform must be 2.7 or above.
- OpenCv 

        This is the basis library used in almost every program used in this project. Its version should be either 2.x or 3.x.
- Numpy library

        Used for type conversions, NumPy is a library for the Python programming language, adding support for large, 
        multi-dimensional arrays and matrices, along with a large collection of high-level mathematical functions to operate on these arrays.  
## Steps and Screenshots

#### 1. Implementation of Open Gesture Operation

    To implement the open gesture we need to do some calculation to find some coordinates. 
    See the below image to get the idea.We have to first calculate the centre of both detected green 
    object which we can easily do by taking the average of the bounding boxes maximum and minimum points. 
    Now we got 2 coordinate from the centre of the 2 objects we will find the average of that and we will get the red point.

#### So now if the camera detects two objects in red color then it will detect it and make a contour over each. Then it will join the centers of the two contours and the mid-point of that line will make the cursor move.

![Output Screenshot](https://github.com/AyanPahari/Virtual-Mouse-using-Hand-Gesture/blob/master/Screenshots/Screenshot1.JPG)

#### 2. Implementation of Close Gesture/ Clicking

#### Now let’s implement the close gesture where we will be clicking the object and dragging it.
    Now if the camera detects only one contour it will make the mouse’s left button as pressed and 
    if it is more than only contours then the mouse’s left button is released.

![Output Screenshot](https://github.com/AyanPahari/Virtual-Mouse-using-Hand-Gesture/blob/master/Screenshots/Screenshot2.JPG)


#### Note

The background should either be white or black to avoid any sort of outside noise.
