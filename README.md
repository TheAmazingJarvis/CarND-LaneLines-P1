#**Finding Lane Lines on the Road** 
<img src="laneLines_thirdPass.jpg" width="480" alt="Combined Image" />


**The Challenge:**  
When we drive, we use our eyes to decide where to go.  The lines on the road that show us where the lanes are act as our constant reference for where to steer the vehicle.  Naturally, one of the first things we would like to do in developing a self-driving car is to automatically detect lane lines using an algorithm.

**The Toolkit:**  
To run this project, you will need to install the following:
- Python 3
- numpy
- matplotlib
- OpenCV 
- moviepy
- Jupyter Notebook

**The Implementation:**  
1) Convert frame to grayscale
2) Create masks for yellow and white pixels
3) Apply a Gaussian smoothing
4) Apply a Canny edge detection
5) Create an additional mask to focus on the "region of interest" in front of the vehicle
6) Convert the points(i.e. pixels) in XY space to a line in Hough space
7) Where the lines in Hough space intersect (i.e. a point) a line exists in XY space
8) Using the extrema of the lines generated, create two averaged line s 9) Create two averaged lines across frames for a smooth video playback
10) Draw the lines to each frame

**The Results:**  
I was able to achieve some nice results on the provided samples. Looking forward, a more nuanced approach will need to be taken to handle certain scenarios:  
1. The lane detection region of interest (ROI), must be flexible. When driving up or down a steep incline, the horizon will change and no longer be a product of the proportions of the frame. This is also something to consider for tight turns and bumper to bumper traffic.   
2. Driving at night. The color identification and selection process works very well in day light. Introducing shadows will create some noisy, but it will not provide as rigorous a test as driving in night, or in limited visibility conditions (e.g. heavy fog)
 
