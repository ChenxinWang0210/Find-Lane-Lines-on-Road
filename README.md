# **Finding Lane Lines on the Road** 


Overview
---


In this project I wrote a pipeline to detect lane lines in images, and then used it to process videos.



The Pipeline
---

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
