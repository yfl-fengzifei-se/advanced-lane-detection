## [Basic Lane Detection](./A-BASIC-LANE-DETECTION/)

# INTRODUCTION

Built an advanced lane-finding algorithm using distortion correction, image rectification, color transforms, and gradient thresholding. Identified lane curvature and vehicle displacement. Overcame environmental challenges such as shadows and pavement changes

# [MEDIUM ARTICLE](https://medium.com/@mithi/advanced-lane-finding-using-computer-vision-techniques-7f3230b6c6f2)

In this project, I have used computer vision techniques to identify lane boundaries and compute the estimate the radius of curvature given a frame of video of the road.  

To achieve this, the following steps are taken:
- Computed the camera calibration matrix and distortion coefficients of the camera lens used given a set of chessboard images taken by the same camera
- Used the aforementioned matrix and coefficient to correct the distortions given by the raw output from the camera
- Use color transforms, and sobel algorithm to create a thresholded binary image that has been filtered out of unnecessary information on the image 
- Apply perspective transform to see a “birds-eye view” of the image as if looking from the sky 
- Apply masking to get the region of interest, detect lane pixels, 
- Determine the best fit curve for each lane the curvature of the lanes
- Project the lane boundaries back onto the undistorted image of the original view 
- Output a visual display of the lane boundaries and other related information 

# HOW TO USE
- You need to setup dependencies to run a Jupyter Notebook on your computer and setup a handful of packages such as `opencv`
```
import matplotlib.pyplot as plt
%matplotlib inline
import cv2 
import numpy as np
import pickle
from scipy.misc import imread

from moviepy.editor import VideoFileClip
from IPython.display import HTML
```
- To run any notebook properly, copy the jupyter notebooks from the `/notebook` folder to the `root` directory
- This is so that each notebook sees to see relevant files, the most relevant files being the python classes. 

# Relevant Links

- My Medium article
- - https://medium.com/@mithi/advanced-lane-finding-using-computer-vision-techniques-7f3230b6c6f2
- My submitted detailed technical writeup 
- - https://github.com/mithi/advanced-lane-detection/blob/master/WRITEUP.pdf
- Udacity's project page
- - https://github.com/udacity/CarND-Advanced-Lane-Lines

# RELEVANT FILES

### Video Output
- project_video_output.mp4
- project_video_verbose_output.mp4

### Pipeline
- pipeline.ipynb
- pipeline_verbose.ipynb

### Classes
- ChessBoard - chessboard.py
- BirdsEye - birdseye.py
- LaneFilter - lanefilter.py
- Curves - curves.py
