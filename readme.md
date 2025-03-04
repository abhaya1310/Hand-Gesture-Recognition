Hand Gesture Recognition Project
This repository contains the code and documentation for a hand gesture recognition system. The project implements algorithms to recognize hand shapes or gestures from video frames captured by a webcam and displays the detected gesture on a graphical interface.

Project Overview
The goal of this project is to design and implement an efficient system to detect and classify various hand gestures. The system uses a combination of image processing techniques such as skin detection, binary conversion, motion detection, circularity evaluation, and template matching to identify gestures including:

Thumbs Up
Thumbs Down
Open Palm
Closed Fist
Index Finger
These gestures are captured using a webcam under controlled lighting conditions and are compared against predefined templates to compute the recognition confidence.

Features
Skin Detection:
Isolates skin regions by converting frames to the HSV color space, applying morphological operations (erosion, dilation), and blurring for smoothing.

Binary Conversion:
Converts frames to grayscale, applies Gaussian blurring and Otsu's thresholding to create binary images that highlight foreground objects.

Motion Detection:
Implements background and frame differencing to detect motion, useful for identifying changes in the video sequence.

Circularity Evaluation:
Differentiates between gestures (e.g., closed fist versus index finger) by computing circularity using the formula:
Circularity = 4 * π * Area / (Perimeter^2)

Template Matching:
Loads and processes hand gesture templates, then matches these templates against the video frames to determine the detected gesture based on correlation scores.


Experimental Results
The system was evaluated under controlled lighting conditions using a webcam. The detection accuracy for each gesture is as follows:

Thumbs Up: 100%
Thumbs Down: 100%
Open Palm: 100%
Closed Fist: 90%
Index Finger: 70%

<video width="640" height="360" controls>
  <source src="hand_shapes.avi" type="video/x-msvideo">
  Your browser does not support the video tag.
</video>

The results can be seen in the video uploaded above.

Authors
Abhaya Shukla (U42968713)
Shreyas Sudersan (U71890555)
Credits and Acknowledgements
This project was inspired by several online resources and tutorials:

PyImageSearch - Skin Detection 
Medium - Contours and Convex Hull in OpenCV 
Medium - Motion Detection Techniques 
