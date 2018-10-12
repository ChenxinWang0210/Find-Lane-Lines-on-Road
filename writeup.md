# **Finding Lane Lines on the Road** 



[//]: # (Image References)


---

### Reflection

### 1. Construct the pipeline.

My pipeline consisted of 5 steps. First, I made a copy of the image and converted the copy to grayscale,
![Original image](./test_images/solidWhiteRight.jpg)
![Grayscale](./test_images/solidWhiteRight_grayscale.jpg)

then I applied Gaussian smoothing to suppress noise and spurious gradients and used a canny function to detect edges.
![Canny edges](./test_images/solidWhiteRight_edges.jpg)

Next, I applied a mask to isolate the lane line segments. 
![Masked edges](./test_images/solidWhiteRight_masked_edges.jpg)

After that, I created a blank image and drew the lane line segements on the blank image. 
![Line images](./test_images/solidWhiteRight_line_image.jpg)
At last, I put the lane line image and the orginal image together.
![Lane Lines](./test_images/solidWhiteRight_Lane_Lines.jpg)

In order to draw a single line on the left and right lanes, I modified the draw_lines() function. First, I identified the line segments on the left or right line by using the slopes of the line segments (the line segments with small slopes were filtered out). Then I fitted the left and right lines using linear functions. At last, I specify the two endpoints for each line to draw the left and right lines on the blank image




### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when there were two lines on one side

Another shortcoming could be what would happen when the car was changing lanes




### 3. Suggest possible improvements to your pipeline

A possible improvement would be to identify line colors

Another potential improvement could be to identify whether the line is segmented or not
