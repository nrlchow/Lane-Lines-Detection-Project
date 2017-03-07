#**Finding Lane Lines on the Road** 

When we drive, we use our eyes to decide where to go.  The lines on the road that show us where the lanes are act as our constant reference for where to steer the vehicle.  Naturally, one of the first things we would like to do in developing a self-driving car is to automatically detect lane lines using an algorithm.
In this project I will detect lane lines in images using Python and OpenCV.  



Video Reference:

### Project video

[![Alt text](https://img.youtube.com/vi/dCGB8QQdQw0/0.jpg)](https://www.youtube.com/watch?v=dCGB8QQdQw0)


### Project video

[![Alt text](https://img.youtube.com/vi/v=kpv44MqVoD8/0.jpg)](https://www.youtube.com/watch?v=v=kpv44MqVoD8)



Test on Images

** My pipeline worked well on these images before I tried the videos.**


[image1]: ./test_images/solidWhiteCurve_Lanes_Drawn.jpg "solidWhiteCurve_Lanes_Drawn"
[image2]: ./test_images/solidWhiteRight_Lanes_Drawn.jpg "solidWhiteRight_Lanes_Drawn"
[image3]: ./test_images/solidYellowCurve_Lanes_Drawn.jpg "solidYellowCurve_Lanes_Drawn"
[image4]: ./test_images/whiteCarLaneSwitch_Lanes_Drawn.jpg "whiteCarLaneSwitch_Lanes_Drawn"
[image5]: ./test_images/solidYellowLeft_Lanes_Drawn.jpg "solidYellowLeft_Lanes_Drawn"



# Solid White Curve Lanes Drawn

![alt text][image1]

# Solid White Right Lanes Drawn
![alt text][image2]

# Solid Yellow Curve Lanes Drawn
![alt text][image3]

# White Car Lane Switch Lanes Drawn
![alt text][image4]

# Solid Yellow Left Lanes Drawn
![alt text][image5]


## Reflections

The algorithm converts color image to grayscale,applies Gaussian smoothing filter to image with OpenCV, detects edges with canny edge detector,define vertices and runs Hough transform on masked edge-detected image. It then averages the line segments that are detected and maps out the full extent of the lane lines.
 
This algorithm works well on linear line segments but fails to handle low-contrast area and curved line. This is what I have seen while running the pipeline on the optional challenge video. The algorithm can be improved by adding motion detection algorithm,by processing video frame by frame and applying some smoothing filter, and by removing hard coded values so that this algorithm can perform well on any given type of lines.
 
I attempted to make my algorithm a bit more robust for optional challenge video.I think I need to explore other colour selection filters that handle well low-contrast image.I also need to explore and apply curved line detection algorithm. This project is a good starting point for an aspiring self-driving car engineer like me.




