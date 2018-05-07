# **Finding Lane Lines on the Road** 



**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Improve the line-drawing function to create continuous lines
  with a fixed length.
* Test different parameter values to improve line detection.

[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline, programmed as a function named "refined_process_image ", consists of 6 main steps: 

1. A copy of the original image is converted to grayscale, a format which is easier
to work with.

![alt text][image1]

*Caption*


2. The Canny transform is applied to the gray image. A low threshold of 100 and 
a high threshold of 150 are selected. These values were found through trial and error.

![alt text][image1]


3. Then, a Gaussian Blur is applied to remove detail and noise. We use a kernel size of 7. ( This value
gives good results).

![alt text][image1]


4. A region of interest is cut out of the blurred image by applying a mask. This function will keep
only the region of the image defined by the polygon formed from previously specified "vertices".
The rest of the image will be set to black.

![alt text][image1]


5. We take the cropped image and apply the Hough Line Transform to it, detecting straight lines.
These lines are then processed in the "refined_draw_lines" function: horizontal and vertical lines are discarded, as well as any 
line with a slope greater than 0.5 or lower than -0.5. After this initial filter, the lines are grouped in 2 sets, one with lines with a 
positive slope(lines on the left) and another with lines with a negative slope (lines on the right).
We then calculate the mean slope and center of the lines on each of the sets. These values are then used to draw 
2 lines (one on the right and the other on the left), each with its respective mean slope value. The length of these 
lines is fixed: it spans from the lower limit of the image to the horizontal line in the center of the image. The mean center of each of these groups is used to draw the line. 

![alt text][image1]


6. Lastly, we combine the original image and the image with the drawn lines. Lines are semitransparent
in order to improve visibility.

![alt text][image1]


If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
