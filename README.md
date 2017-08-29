# Object tracking using descriptor matching

## Description
#### Tracking of a target ROI in camera using description matching. Written in Python.
  
## Algorithm
#### 1. Detection of interest points and descriptors
* Detect the ORB features and descriptors for both the camera frames and a user selected region of interest (ROI) to be 
tracked.
#### 2. FLANN matching and tracking
* Using the Fast Library for Approximate Nearest Neighbors (FLANN) matching algorithm, if more than 4 corresponding 
descriptors are found between the frame and the ROI, the object is found.
#### 3. Visualization
* The (homography) transformation matrix that transforms the ROI coordinates to those of the camera frame is calculated 
using the corresponding points.
* Application of the homography reprojects the boundary of the object of interest to the scene and allows visualization.

## How to use
Press 's' in the main window (live video from camera) to take a screenshot. In the new window, select the ROI by 
enclosing with a rectangular bounding box, dragged with the mouse (left button). The ROI should contain distinct 
features for better results (e.g. tests using a book cover produced remarkable results). The new window shows the 
results. 'Esc' terminates the program.

## Required compilers/libraries
* Python 2.7
* OpenCV 3.0
* Numpy
