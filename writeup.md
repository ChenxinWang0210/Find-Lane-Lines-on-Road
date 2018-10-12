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
At last, we put the lane line image and the orginal image together.
![Lane Lines](./test_images/solidWhiteRight_Lane_Lines.jpg)

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...

If you'd like to include images to show how the pipeline works, here is how to include an image: 






### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
