# **Finding Lane Lines on the Road** 

## Writeup

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consited of 9 steps. 
the pipeline processings follows:

1. Convert fullcolor input image into a grayscale image.
2. Apply gaussian_blur to the grayscale image.
3. Detect edges by canny method.
4. Mask the edge image in the area of the road.
5. Detect hough lines from the masked edge images.
6. Classify the detected lines into the left lanes or the right lanes.
7. Create one left lane with the average slope of the left lines and passing the farthest line vertex.
8. Create one right lane by the same way as the left one.
9. Draw the left lane and right lane on the input image.

In order to draw a single line on the left and right lanes.
I added two functions before the draw_lines(): split_lines() and detect_line().

The split_lines() function classifies the detected lines into the left lanes or the right lanes.
In order to decide one line left lane or right lane, this function use 

![split_lines][split_lines.bmp]


The detect_line() function creates one left lane with the average slope of the left lines and
passing the farthest line vertex.


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"



### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
