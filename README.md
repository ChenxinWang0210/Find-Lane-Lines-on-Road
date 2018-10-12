# **Finding Lane Lines on the Road** 


Overview
---


In this project I wrote a pipeline to detect lane lines in images, and then used it to process videos.



The Pipeline
---
My pipeline consisted of 6 steps.

1. I made a copy of the image and applied a color mask to isolate white and yellow object  
![Original image](./test_images/solidYellowLeft.jpg)
![Original image](./test_images/solidYellowLeft_color_masked.jpg)
2. I converted the image to grayscale,
![Grayscale](./test_images/solidYellowLeft_grayscale.jpg)

3. I applied Gaussian smoothing to suppress noise and spurious gradients and used a canny function to detect edges.
![Canny edges](./test_images/solidYellowLeft_edges.jpg)

4. I applied a mask to isolate the lane line segments. 
![Masked edges](./test_images/solidYellowLeft_masked_edges.jpg)

5. I created a blank image and drew the lane line segements on the blank image. 
![Line images](./test_images/solidYellowLeft_line_image.jpg)

6. I put the lane line image and the orginal image together.
![Lane Lines](./test_images/solidYellowLeft_Lane_Lines.jpg)
