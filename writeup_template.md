# **Finding Lane Lines on the Road**

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I ....
2. Gaussion Smoothing to average pixels. The kernel size must not be too big to average the edges out. The kernel size must not be too small to contain big gradients everwhere.
3. Apply region selection as lane markings usually appear at the same region of camera view.
4. Apply hough transform or canny edge detector
4.1 Why prefer hough transform to canny edge detector?
5. Draw the found edges in line segments

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...

If you'd like to include images to show how the pipeline works, here is how to include an image:

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ...

When driving on curve, use yaw rate to modify the parameters for polygon and line segments
When driving under different lighting/weather conditions, apply different parameters

Another shortcoming could be ...
Some road may not have a lane marking, so need to find the edges of road

### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

When driving on curve, use yaw rate to modify the parameters for polygon and line segments
When driving under different lighting/weather conditions, apply different parameters


Another potential improvement could be to ...
Some road may not have a lane marking, so need to find the edges of road
