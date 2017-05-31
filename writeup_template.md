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

My pipeline is defined in function: process_image_in which consisted of 6 steps
  *1. converted the images to grayscale,
  *2. call the gaussian_blur with kernel_size = 3
  *3. then call the canny function to find the all the edges, with low_threhold = 50 and high_threhold = 150
  *4. defines the 4 vertices to define the region of interest, and then apply the region to the image returned by canny
  *5. Use the hough_lines to detects all the lines with following paramters:
      * rho = 1
      * theta = np.pi/180
      * threshold = 15
      * min_line_length = 40
      * max_line_gap = 20
      
  *6. call the image draw function _weighted_img_    

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![solidWhiteCurve.jpg][./test_images_output/solidWhiteCurve.jpg]
![alt text][image1]
![alt text][image1]
![alt text][image1]
![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
