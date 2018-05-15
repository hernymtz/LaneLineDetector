# **Finding Lane Lines on the Road** 
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

<img src="examples/laneLines_thirdPass.jpg" width="480" alt="Combined Image" />

Overview
---

When we drive, we use our eyes to decide where to go.  The lines on the road that show us where the lanes are act as our constant reference for where to steer the vehicle.  Naturally, one of the first things we would like to do in developing a self-driving car is to automatically detect lane lines using an algorithm.

In this project, lane lines in images are detected using Python as the primary programming language, and OpenCV, which is a package that has many useful tools for analyzing images. Procedures to achieve this will include: grayscale conversion, canny transformation, gaussian blurring, hough transformation, region cutting and getting mean values of line slopes. 

The repository contains two main files: one containing project code (P1.ipynb) and a file containing a brief write up (writeup.md) explaining or the solution proposed. Test images, input and output videos and other files are also included.


Files and Foldersin the Repository:
---


1. "examples" folder: Contains jpg images used to understand  the different image-manipulation functions, as well as supporting png images to describe each of the ¡ 6 steps in the pipeline. It also includes mp4 videos of the expected results.
    - grayscale.jpg
    - laneLines_thirdPass.jpg
    - line-segments-example.jpg
    - P1_example.mp4
    - raw-lines-example.mp4
    - canny_img.png
    - gauss_img.png
    - hough.png
    - interest.png
    - weighted.png
    - grayscale.png

2. "test_images" folder: Contains 6 jpg images used to perform tests on them. They have different characteristics, with some having a continuous line on one of the sides while others have a curve. Lines can also differ in color, in some cases being white and in others yellow.
    - solidWhiteCurve.jpg
    - solidWhiteRight.jpg
    - solidYellowCurve.jpg
    - solidYellowCurve2.jpg
    - solidYellowLeft.jpg
    - whiteCarLaneSwitch.jpg

3. "test_videos" folder: Contains 3 mp4 videos of highway lanes: 1 with a solid white right line, 1 with a solid yellow left line and 1 with challenging lanes.
    - challenge.mp4
    - solidWhiteRight.mp4
    - solidYellowLeft.mp4

4. "test_videos_output" folder: Contains the 2 mp4 resulting videos produced by the code. Red lines  indicate where the computer is detecting the lane lines. 
    - solidWhiteRight.mp4
    - solidYellowLeft.mp4

5. "LICENSE" file: Contains the License for the project.

6. "README.md" file: Contains a brief description of the project, of the files contained in the repository and of the steps require to run the code.

7. "writeup.md" file: Contains a description of the steps taken in the code to get the required result (lane detection). Possible improvement and errors are described here. 

8. "P1.ipynb" file: Actual code that detects the lane lines in a jupyter notebook. Written in Python.

9. "P1.html" file: Basically has the same content as the "P1.ipynb" file but in the HTML format to allow an easier evaluation of the code.

Running the  Project
---

To run the project you will require (in the case of the .ipynb file):

    - Anaconda to read Jupyter Notebook files (.ipynb).
    - The following Python libraries installed: matplotlib, OpenCV, numpy, moviepy, IPython.

To run the project follow the following instructions:

    1. Be sure to have all the requirements installed.
    2. Be sure to have all the repository´s folders and files in (one exception are the output videos of the "test_videos_output" folder)
    3. Open the "P1.ipynb" file with Jupyter Notebook (you might have to call it from the terminal and run it on your browser)
    4. Run each of the cells sequentially (select each cell and press Shift+Enter, for example). Wait for the pipeline of each of the 2 videos to finish (there is a progress bar for each). 
    5. When finished, 2 videos will be displayed. Press the play button on any of them to see the results. These will also have been saved as mp4 videos in the "test_videos_output" folder.




